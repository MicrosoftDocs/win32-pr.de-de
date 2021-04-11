---
description: In diesem Abschnitt werden die Formate ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) -Werte) angegeben, die in der Direct3D-Funktion 10level9 9,3-Hardware unterstützt werden.
ms.assetid: B2A843D5-6A6B-4180-8B94-D032B1322798
title: Formatunterstützung für Direct3D 9 9.3-Hardware auf Featureebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79185ddb360fe9359371671e3722372c3a1615f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041164"
---
# <a name="format-support-for-direct3d-feature-10level9-93-hardware"></a><span data-ttu-id="0cbba-103">Formatunterstützung für Direct3D 9 9.3-Hardware auf Featureebene</span><span class="sxs-lookup"><span data-stu-id="0cbba-103">Format support for Direct3D Feature 10Level9 9.3 hardware</span></span>

<span data-ttu-id="0cbba-104">In diesem Abschnitt werden die Formate ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) -Werte) angegeben, die in der Direct3D-Funktion 10level9 9,3-Hardware unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="0cbba-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature 10Level9 9.3 hardware.</span></span>

<span data-ttu-id="0cbba-105">Die Tabelle enthält eine Zusammenfassung der Featureunterstützung, die den folgenden Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="0cbba-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="0cbba-106">Symbol</span><span class="sxs-lookup"><span data-stu-id="0cbba-106">Symbol</span></span>                            | <span data-ttu-id="0cbba-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0cbba-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="0cbba-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="0cbba-108">_ *-*\*</span></span>                             | <span data-ttu-id="0cbba-109">Nicht zulässig oder nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0cbba-109">Disallowed or not available.</span></span>                                                  |
| ![Erforderlich](images/letter-r.jpg)  | <span data-ttu-id="0cbba-111">Hardware Unterstützung ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0cbba-111">Hardware support is required.</span></span>                                                 |
| ![Optional](images/letter-o.jpg)  | <span data-ttu-id="0cbba-113">Hardwareunterstützung optional, das Format ist möglicherweise Hardware beschleunigt.</span><span class="sxs-lookup"><span data-stu-id="0cbba-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![lässe](images/letter-d.jpg) | <span data-ttu-id="0cbba-115">Erforderlich, wenn eine zugehörige optionale Funktion unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="0cbba-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="0cbba-116">Dieses Thema enthält einen Abschnitt Pro Format.</span><span class="sxs-lookup"><span data-stu-id="0cbba-116">This topic contains a section per format.</span></span> <span data-ttu-id="0cbba-117">Ein Format *Ziel* (die Tabellen enthalten eine Zeile pro Ziel) kann ein Ressourcentyp, eine intrinsische HLSL-Funktion oder eine bestimmte Funktionalität sein, die von einem bestimmten Format abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="0cbba-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="0cbba-118">Informationen zur programmgesteuerten Überprüfung der Formatunterstützung in D3D11 und D3D12 finden Sie unter über [Prüfen der Unterstützung von Hardwarefunktionen](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="0cbba-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="0cbba-119">Die Zahlen der Formate sind größtenteils, aber nicht alle in aufsteigender numerischer Reihenfolge, dass einige nicht in &mdash; numerischer Reihenfolge sind und neben anderen relevanten Formaten aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0cbba-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="0cbba-120">Beachten Sie auch, dass *typlose* in einem Format Namen *teilweise* typisiert und nicht streng typlos sein kann (Weitere Informationen finden Sie im Abschnitt " [Format Notizen](#format-notes) " am Ende des Themas).</span><span class="sxs-lookup"><span data-stu-id="0cbba-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="0cbba-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="0cbba-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="0cbba-122">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-122">Target</span></span> | <span data-ttu-id="0cbba-123">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-123">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-124">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-125">0</span><span class="sxs-lookup"><span data-stu-id="0cbba-125">0</span></span> |
| <span data-ttu-id="0cbba-126">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-126">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-127">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-127">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-128">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-128">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-129">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-129">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-130">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-130">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-131">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-131">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-132">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-132">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-133">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-134">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-135">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-135">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-136">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-137">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-138">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-139">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-139">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-140">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-141">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-141">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-142">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-143">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-143">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-144">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-145">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-146">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-147">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-148">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-149">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-149">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-150">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-151">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-152">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-153">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-154">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-154">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-155">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-156">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-157">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-158">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-158">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-159">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-159">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-160">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-160">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-161">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-161">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-162">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-163">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-163">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-164">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-165">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-166">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-167">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-168">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-169">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-169">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-170">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="0cbba-171">DXGI_FORMAT_R32G32B32A32 \_ Typen losen<sup>PCs</sup> (1)</span><span class="sxs-lookup"><span data-stu-id="0cbba-171">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="0cbba-172">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-172">Target</span></span> | <span data-ttu-id="0cbba-173">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-173">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-174">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-175">128</span><span class="sxs-lookup"><span data-stu-id="0cbba-175">128</span></span> |
| <span data-ttu-id="0cbba-176">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-176">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-177">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-177">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-178">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-178">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-179">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-179">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-180">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-180">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-181">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-181">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-182">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-182">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-183">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-184">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-185">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-185">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-186">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-186">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-187">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-187">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-188">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-188">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-189">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-189">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-190">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-190">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-191">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-191">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-192">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-192">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-193">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-193">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-194">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-194">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-195">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-195">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-196">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-196">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-197">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-197">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-198">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-198">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-199">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-199">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-200">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-200">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-201">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-201">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-202">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-202">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-203">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-203">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-204">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-204">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-205">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-205">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-206">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-206">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-207">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-207">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-208">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-208">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-209">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-209">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-210">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-210">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-211">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-211">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-212">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-212">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-213">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-213">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-214">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-214">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-215">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-215">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-216">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-216">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-217">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-217">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-218">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-218">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-219">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-219">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-220">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-220">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a><span data-ttu-id="0cbba-221">DXGI_FORMAT_R32G32B32A32 \_ float<sup></sup> -Datentyp (2)</span><span class="sxs-lookup"><span data-stu-id="0cbba-221">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FNS</sup> (2)</span></span>
| <span data-ttu-id="0cbba-222">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-222">Target</span></span> | <span data-ttu-id="0cbba-223">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-223">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-224">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-224">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-225">128</span><span class="sxs-lookup"><span data-stu-id="0cbba-225">128</span></span> |
| <span data-ttu-id="0cbba-226">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-226">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-228">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-228">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-229">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-229">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-231">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-232">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-233">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-234">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-234">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-236">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-236">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-238">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-238">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-240">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-240">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-242">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-242">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-243">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-243">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-244">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-244">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-245">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-245">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-246">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-246">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-247">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-247">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-249">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-249">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-251">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-251">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-253">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-253">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-254">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-254">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-255">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-255">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-256">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-256">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-257">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-257">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-258">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-258">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-259">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-259">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-260">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-260">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-261">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-261">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-262">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-262">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-263">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-263">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-264">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-264">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-265">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-265">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-266">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-266">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-267">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-267">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-269">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-269">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-271">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-271">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-273">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-273">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-275">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-275">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-277">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-277">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-278">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-278">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-279">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-279">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-280">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-280">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-281">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-281">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-282">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-282">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-283">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-283">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-284">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-284">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a><span data-ttu-id="0cbba-285">DXGI_FORMAT_R32G32B32A32 \_ uint<sup></sup> -Benutzerkonten (3)</span><span class="sxs-lookup"><span data-stu-id="0cbba-285">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FNS</sup> (3)</span></span>
| <span data-ttu-id="0cbba-286">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-286">Target</span></span> | <span data-ttu-id="0cbba-287">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-287">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-288">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-288">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-289">128</span><span class="sxs-lookup"><span data-stu-id="0cbba-289">128</span></span> |
| <span data-ttu-id="0cbba-290">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-290">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-291">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-291">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-292">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-292">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-293">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-293">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-294">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-294">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-295">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-295">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-296">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-296">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-297">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-297">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-298">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-298">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-299">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-299">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-300">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-300">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-301">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-301">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-302">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-302">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-303">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-303">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-304">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-304">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-305">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-305">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-306">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-306">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-307">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-307">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-308">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-308">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-309">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-309">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-310">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-310">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-311">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-311">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-312">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-312">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-313">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-313">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-314">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-314">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-315">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-315">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-316">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-316">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-317">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-317">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-318">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-318">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-319">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-319">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-320">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-320">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-321">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-321">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-322">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-322">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-323">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-323">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-324">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-324">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-325">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-325">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-326">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-326">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-327">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-327">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-328">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-328">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-329">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-329">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-330">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-330">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-331">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-331">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-332">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-332">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-333">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-333">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-334">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-334">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a><span data-ttu-id="0cbba-335">DXGI_FORMAT_R32G32B32A32 \_ Sint<sup></sup> (4)</span><span class="sxs-lookup"><span data-stu-id="0cbba-335">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FNS</sup> (4)</span></span>
| <span data-ttu-id="0cbba-336">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-336">Target</span></span> | <span data-ttu-id="0cbba-337">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-337">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-338">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-338">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-339">128</span><span class="sxs-lookup"><span data-stu-id="0cbba-339">128</span></span> |
| <span data-ttu-id="0cbba-340">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-340">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-341">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-341">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-342">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-342">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-343">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-343">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-344">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-344">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-345">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-345">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-346">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-346">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-347">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-347">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-348">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-349">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-349">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-350">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-350">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-351">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-351">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-352">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-352">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-353">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-353">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-354">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-354">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-355">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-355">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-356">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-356">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-357">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-357">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-358">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-358">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-359">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-359">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-360">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-360">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-361">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-361">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-362">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-362">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-363">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-363">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-364">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-364">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-365">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-365">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-366">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-366">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-367">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-367">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-368">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-368">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-369">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-369">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-370">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-370">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-371">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-371">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-372">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-372">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-373">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-373">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-374">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-374">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-375">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-375">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-376">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-376">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-377">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-377">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-378">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-378">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-379">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-379">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-380">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-380">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-381">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-381">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-382">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-382">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-383">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-383">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-384">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-384">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="0cbba-385">DXGI_FORMAT_R32G32B32 \_ Typen losen<sup>PCs</sup> (5)</span><span class="sxs-lookup"><span data-stu-id="0cbba-385">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="0cbba-386">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-386">Target</span></span> | <span data-ttu-id="0cbba-387">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-387">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-388">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-388">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-389">96</span><span class="sxs-lookup"><span data-stu-id="0cbba-389">96</span></span> |
| <span data-ttu-id="0cbba-390">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-390">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-391">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-391">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-392">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-392">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-393">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-393">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-394">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-394">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-395">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-395">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-396">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-396">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-397">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-397">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-398">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-398">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-399">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-399">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-400">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-400">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-401">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-401">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-402">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-402">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-403">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-403">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-404">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-404">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-405">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-405">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-406">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-406">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-407">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-407">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-408">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-409">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-410">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-411">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-412">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-413">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-414">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-415">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-416">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-417">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-418">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-418">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-419">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-420">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-421">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-422">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-422">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-423">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-423">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-424">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-424">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-425">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-425">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-426">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-426">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-427">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-427">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-428">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-428">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-429">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-429">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-430">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-430">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-431">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-431">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-432">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-432">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-433">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-433">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-434">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-434">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a><span data-ttu-id="0cbba-435">DXGI_FORMAT_R32G32B32 \_ float<sup></sup> -Datentyp (6)</span><span class="sxs-lookup"><span data-stu-id="0cbba-435">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FNS</sup> (6)</span></span>
| <span data-ttu-id="0cbba-436">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-436">Target</span></span> | <span data-ttu-id="0cbba-437">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-437">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-438">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-438">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-439">96</span><span class="sxs-lookup"><span data-stu-id="0cbba-439">96</span></span> |
| <span data-ttu-id="0cbba-440">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-440">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-442">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-442">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-443">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-443">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-445">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-446">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-447">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-448">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-448">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-449">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-449">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-450">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-450">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-451">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-451">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-452">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-452">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-453">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-454">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-455">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-455">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-456">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-457">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-457">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-458">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-458">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-459">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-459">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-460">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-460">Blendable RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="0cbba-462">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-462">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-463">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-463">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-464">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-464">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-465">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-465">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-466">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-466">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-467">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-467">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-468">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-468">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-469">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-469">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-470">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-470">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-471">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-471">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-472">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-472">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-473">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-473">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-474">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-474">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-475">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-475">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-476">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-476">4x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="0cbba-478">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-478">8x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="0cbba-480">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-480">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-481">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-481">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-482">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-482">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-483">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-483">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-484">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-484">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-485">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-485">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-486">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-486">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-487">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-487">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-488">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-488">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-489">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-489">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a><span data-ttu-id="0cbba-490">DXGI_FORMAT_R32G32B32 \_ uint<sup></sup> -(7)</span><span class="sxs-lookup"><span data-stu-id="0cbba-490">DXGI_FORMAT_R32G32B32\_UINT<sup>FNS</sup> (7)</span></span>
| <span data-ttu-id="0cbba-491">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-491">Target</span></span> | <span data-ttu-id="0cbba-492">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-492">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-493">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-493">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-494">96</span><span class="sxs-lookup"><span data-stu-id="0cbba-494">96</span></span> |
| <span data-ttu-id="0cbba-495">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-495">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-496">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-496">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-497">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-497">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-498">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-498">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-499">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-499">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-500">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-500">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-501">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-502">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-502">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-503">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-503">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-504">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-504">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-505">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-505">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-506">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-507">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-508">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-508">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-509">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-510">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-510">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-511">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-511">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-512">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-512">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-513">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-513">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-514">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-514">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-515">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-515">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-516">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-516">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-517">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-517">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-518">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-518">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-519">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-519">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-520">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-520">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-521">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-521">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-522">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-522">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-523">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-523">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-524">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-524">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-525">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-525">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-526">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-526">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-527">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-527">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-528">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-528">4x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="0cbba-530">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-530">8x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="0cbba-532">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-533">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-534">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-534">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-535">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-536">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-537">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-538">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-539">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-540">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-540">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-541">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a><span data-ttu-id="0cbba-542">DXGI_FORMAT_R32G32B32 \_ Sint<sup></sup> (8)</span><span class="sxs-lookup"><span data-stu-id="0cbba-542">DXGI_FORMAT_R32G32B32\_SINT<sup>FNS</sup> (8)</span></span>
| <span data-ttu-id="0cbba-543">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-543">Target</span></span> | <span data-ttu-id="0cbba-544">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-544">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-545">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-546">96</span><span class="sxs-lookup"><span data-stu-id="0cbba-546">96</span></span> |
| <span data-ttu-id="0cbba-547">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-547">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-548">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-548">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-549">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-550">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-551">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-552">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-553">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-554">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-555">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-556">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-557">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-558">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-559">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-560">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-560">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-561">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-562">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-562">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-563">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-564">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-564">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-565">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-566">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-567">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-568">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-569">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-570">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-570">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-571">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-572">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-573">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-574">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-575">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-576">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-577">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-578">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-579">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-580">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-580">4x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="0cbba-582">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-582">8x Multisample RenderTarget</span></span> | ![lässe](images/letter-d.jpg) |
| <span data-ttu-id="0cbba-584">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-584">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-585">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-585">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-586">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-586">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-587">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-587">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-588">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-588">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-589">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-589">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-590">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-590">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-591">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-591">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-592">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-592">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-593">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-593">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="0cbba-594">DXGI_FORMAT_R16G16B16A16 \_ Typen losen<sup>PCs</sup> (9)</span><span class="sxs-lookup"><span data-stu-id="0cbba-594">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="0cbba-595">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-595">Target</span></span> | <span data-ttu-id="0cbba-596">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-596">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-597">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-597">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-598">64</span><span class="sxs-lookup"><span data-stu-id="0cbba-598">64</span></span> |
| <span data-ttu-id="0cbba-599">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-599">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-600">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-600">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-601">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-601">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-602">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-602">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-603">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-603">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-604">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-604">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-605">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-605">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-606">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-606">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-607">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-607">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-608">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-608">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-609">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-609">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-610">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-610">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-611">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-611">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-612">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-612">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-613">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-613">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-614">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-614">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-615">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-615">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-616">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-616">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-617">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-617">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-618">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-618">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-619">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-619">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-620">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-620">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-621">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-621">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-622">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-622">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-623">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-623">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-624">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-624">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-625">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-625">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-626">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-626">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-627">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-627">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-628">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-628">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-629">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-629">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-630">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-630">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-631">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-631">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-632">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-632">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-633">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-633">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-634">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-634">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-635">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-635">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-636">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-636">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-637">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-637">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-638">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-638">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-639">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-639">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-640">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-640">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-641">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-641">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-642">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-642">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-643">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-643">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a><span data-ttu-id="0cbba-644">DXGI_FORMAT_R16G16B16A16 float-Dateinamen \_ (10)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="0cbba-644">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FNS</sup> (10)</span></span>
| <span data-ttu-id="0cbba-645">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-645">Target</span></span> | <span data-ttu-id="0cbba-646">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-646">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-647">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-647">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-648">64</span><span class="sxs-lookup"><span data-stu-id="0cbba-648">64</span></span> |
| <span data-ttu-id="0cbba-649">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-649">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-651">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-651">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-652">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-652">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-654">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-654">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-655">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-655">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-656">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-656">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-657">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-657">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-659">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-659">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-661">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-661">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-663">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-663">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-665">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-665">Shader sample (any filter)</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-667">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-667">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-668">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-668">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-669">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-669">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-670">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-670">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-671">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-671">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-673">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-673">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-675">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-675">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-677">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-677">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-679">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-679">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-680">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-680">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-681">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-681">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-682">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-682">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-683">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-683">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-684">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-684">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-685">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-685">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-686">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-686">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-687">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-687">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-688">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-688">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-689">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-689">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-690">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-690">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-691">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-691">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-692">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-692">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-694">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-694">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-696">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-696">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-698">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-698">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-700">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-700">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-702">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-702">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-703">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-703">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-704">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-704">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-705">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-705">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-706">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-706">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-707">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-707">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-708">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-708">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-710">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-710">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a><span data-ttu-id="0cbba-711">DXGI_FORMAT_R16G16B16A16 \_ unorm<sup></sup> -Fehler (11)</span><span class="sxs-lookup"><span data-stu-id="0cbba-711">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FNS</sup> (11)</span></span>
| <span data-ttu-id="0cbba-712">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-712">Target</span></span> | <span data-ttu-id="0cbba-713">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-713">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-714">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-714">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-715">64</span><span class="sxs-lookup"><span data-stu-id="0cbba-715">64</span></span> |
| <span data-ttu-id="0cbba-716">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-716">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-718">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-718">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-719">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-719">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-720">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-720">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-721">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-721">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-722">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-722">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-723">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-723">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-725">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-725">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-727">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-727">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-729">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-729">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-731">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-731">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-733">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-733">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-734">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-734">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-735">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-735">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-736">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-736">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-737">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-737">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-739">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-739">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-741">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-741">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-743">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-743">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-744">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-744">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-745">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-745">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-746">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-746">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-747">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-747">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-748">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-748">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-749">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-749">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-750">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-750">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-751">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-751">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-752">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-752">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-753">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-753">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-754">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-754">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-755">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-755">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-756">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-756">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-757">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-757">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-759">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-759">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-761">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-761">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-763">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-763">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-765">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-765">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-767">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-767">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-768">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-768">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-769">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-769">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-770">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-770">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-771">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-771">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-772">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-772">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-773">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-773">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-774">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-774">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a><span data-ttu-id="0cbba-775">DXGI_FORMAT_R16G16B16A16 \_ uint<sup></sup> -Benutzerkonten (12)</span><span class="sxs-lookup"><span data-stu-id="0cbba-775">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FNS</sup> (12)</span></span>
| <span data-ttu-id="0cbba-776">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-776">Target</span></span> | <span data-ttu-id="0cbba-777">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-777">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-778">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-778">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-779">64</span><span class="sxs-lookup"><span data-stu-id="0cbba-779">64</span></span> |
| <span data-ttu-id="0cbba-780">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-780">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-781">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-781">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-782">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-782">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-783">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-783">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-784">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-784">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-785">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-785">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-786">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-786">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-787">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-787">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-788">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-788">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-789">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-789">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-790">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-790">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-791">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-791">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-792">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-792">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-793">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-793">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-794">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-794">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-795">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-795">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-796">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-796">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-797">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-797">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-798">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-798">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-799">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-799">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-800">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-800">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-801">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-801">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-802">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-802">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-803">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-803">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-804">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-804">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-805">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-805">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-806">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-806">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-807">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-807">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-808">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-808">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-809">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-809">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-810">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-810">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-811">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-811">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-812">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-812">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-813">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-813">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-814">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-814">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-815">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-815">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-816">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-816">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-817">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-817">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-818">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-818">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-819">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-819">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-820">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-820">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-821">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-821">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-822">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-822">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-823">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-823">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-824">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-824">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a><span data-ttu-id="0cbba-825">DXGI_FORMAT_R16G16B16A16 \_ snorm<sup></sup> -Kenn Wort (13)</span><span class="sxs-lookup"><span data-stu-id="0cbba-825">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FNS</sup> (13)</span></span>
| <span data-ttu-id="0cbba-826">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-826">Target</span></span> | <span data-ttu-id="0cbba-827">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-827">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-828">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-828">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-829">64</span><span class="sxs-lookup"><span data-stu-id="0cbba-829">64</span></span> |
| <span data-ttu-id="0cbba-830">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-830">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-832">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-832">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-833">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-833">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-835">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-835">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-836">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-836">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-837">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-837">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-838">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-838">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-839">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-839">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-840">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-840">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-841">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-841">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-842">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-842">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-843">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-843">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-844">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-844">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-845">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-845">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-846">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-846">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-847">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-847">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-848">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-848">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-849">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-849">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-850">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-850">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-851">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-851">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-852">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-852">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-853">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-853">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-854">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-854">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-855">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-855">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-856">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-856">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-857">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-857">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-858">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-858">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-859">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-859">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-860">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-860">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-861">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-861">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-862">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-862">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-863">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-863">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-864">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-864">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-865">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-865">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-866">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-866">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-867">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-867">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-868">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-868">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-869">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-869">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-870">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-870">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-871">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-871">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-872">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-872">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-873">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-873">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-874">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-874">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-875">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-875">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-876">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-876">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a><span data-ttu-id="0cbba-877">DXGI_FORMAT_R16G16B16A16 \_ Sint<sup></sup> -nach SPT (14)</span><span class="sxs-lookup"><span data-stu-id="0cbba-877">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FNS</sup> (14)</span></span>
| <span data-ttu-id="0cbba-878">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-878">Target</span></span> | <span data-ttu-id="0cbba-879">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-879">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-880">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-880">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-881">64</span><span class="sxs-lookup"><span data-stu-id="0cbba-881">64</span></span> |
| <span data-ttu-id="0cbba-882">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-882">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-884">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-884">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-885">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-885">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-887">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-887">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-888">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-888">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-889">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-889">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-890">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-890">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-891">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-891">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-892">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-892">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-893">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-893">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-894">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-894">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-895">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-895">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-896">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-896">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-897">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-897">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-898">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-898">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-899">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-899">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-900">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-900">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-901">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-901">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-902">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-902">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-903">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-903">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-904">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-904">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-905">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-905">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-906">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-906">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-907">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-907">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-908">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-908">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-909">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-909">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-910">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-910">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-911">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-911">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-912">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-912">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-913">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-913">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-914">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-914">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-915">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-915">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-916">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-916">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-917">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-917">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-918">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-918">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-919">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-919">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-920">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-920">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-921">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-921">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-922">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-922">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-923">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-923">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-924">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-924">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-925">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-925">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-926">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-926">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-927">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-927">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-928">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="0cbba-929">DXGI_FORMAT_R32G32 \_ Typen losen<sup>PCs</sup> (15)</span><span class="sxs-lookup"><span data-stu-id="0cbba-929">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="0cbba-930">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-930">Target</span></span> | <span data-ttu-id="0cbba-931">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-931">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-932">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-933">64</span><span class="sxs-lookup"><span data-stu-id="0cbba-933">64</span></span> |
| <span data-ttu-id="0cbba-934">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-934">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-935">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-935">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-936">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-936">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-937">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-937">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-938">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-938">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-939">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-939">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-940">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-940">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-941">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-941">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-942">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-942">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-943">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-943">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-944">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-944">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-945">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-945">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-946">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-946">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-947">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-947">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-948">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-948">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-949">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-949">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-950">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-950">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-951">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-951">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-952">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-952">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-953">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-953">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-954">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-954">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-955">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-955">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-956">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-956">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-957">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-957">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-958">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-958">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-959">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-959">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-960">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-960">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-961">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-961">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-962">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-962">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-963">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-963">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-964">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-964">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-965">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-965">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-966">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-966">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-967">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-967">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-968">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-968">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-969">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-969">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-970">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-970">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-971">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-971">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-972">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-972">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-973">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-973">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-974">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-974">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-975">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-975">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-976">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-976">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-977">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-977">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-978">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-978">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a><span data-ttu-id="0cbba-979">DXGI_FORMAT_R32G32 \_ float<sup></sup> -Datentyp (16)</span><span class="sxs-lookup"><span data-stu-id="0cbba-979">DXGI_FORMAT_R32G32\_FLOAT<sup>FNS</sup> (16)</span></span>
| <span data-ttu-id="0cbba-980">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-980">Target</span></span> | <span data-ttu-id="0cbba-981">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-981">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-982">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-982">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-983">64</span><span class="sxs-lookup"><span data-stu-id="0cbba-983">64</span></span> |
| <span data-ttu-id="0cbba-984">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-984">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-986">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-986">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-987">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-987">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-989">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-990">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-991">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-992">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-992">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-994">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-994">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-996">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-996">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-998">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-998">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1000">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1000">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1001">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1001">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1002">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1002">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1003">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-1003">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-1004">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-1004">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-1005">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1005">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-1006">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1006">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-1007">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1007">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1009">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1009">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1010">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-1010">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-1011">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1011">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-1012">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1012">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1013">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1013">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1014">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1014">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-1015">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-1015">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-1016">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1016">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-1017">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-1017">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-1018">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-1018">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-1019">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1019">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-1020">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1020">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-1021">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1021">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1022">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-1022">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1023">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-1023">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1025">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1025">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-1027">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1027">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-1029">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-1029">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-1031">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1031">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1033">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1033">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-1034">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-1034">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-1035">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-1035">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-1036">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-1036">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-1037">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1037">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-1038">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1038">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-1039">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1039">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-1040">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1040">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a><span data-ttu-id="0cbba-1041">DXGI_FORMAT_R32G32 \_ uint<sup></sup> -(17)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1041">DXGI_FORMAT_R32G32\_UINT<sup>FNS</sup> (17)</span></span>
| <span data-ttu-id="0cbba-1042">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1042">Target</span></span> | <span data-ttu-id="0cbba-1043">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-1043">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-1044">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1044">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-1045">64</span><span class="sxs-lookup"><span data-stu-id="0cbba-1045">64</span></span> |
| <span data-ttu-id="0cbba-1046">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1046">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-1047">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1047">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1048">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-1048">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1049">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-1049">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1050">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1050">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1051">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1051">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-1052">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1052">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-1053">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1053">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-1054">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-1054">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-1055">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1055">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-1056">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1056">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1057">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1057">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1058">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1058">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1059">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-1059">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-1060">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-1060">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-1061">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1061">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-1062">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1062">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-1063">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1063">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1064">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1064">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1065">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-1065">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-1066">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1066">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-1067">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1067">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1068">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1068">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1069">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1069">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-1070">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-1070">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-1071">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1071">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-1072">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-1072">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-1073">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-1073">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-1074">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1074">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-1075">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1075">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-1076">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1076">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1077">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-1077">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1078">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-1078">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-1079">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1079">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1080">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1080">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1081">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-1081">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-1082">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1082">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-1083">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1083">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-1084">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-1084">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-1085">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-1085">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-1086">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-1086">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-1087">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1087">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-1088">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1088">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-1089">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1089">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-1090">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1090">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a><span data-ttu-id="0cbba-1091">DXGI_FORMAT_R32G32 \_ Sint<sup></sup> (18)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1091">DXGI_FORMAT_R32G32\_SINT<sup>FNS</sup> (18)</span></span>
| <span data-ttu-id="0cbba-1092">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1092">Target</span></span> | <span data-ttu-id="0cbba-1093">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-1093">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-1094">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1094">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-1095">64</span><span class="sxs-lookup"><span data-stu-id="0cbba-1095">64</span></span> |
| <span data-ttu-id="0cbba-1096">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1096">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-1097">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1097">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1098">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-1098">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1099">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-1099">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1100">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1100">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1101">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1101">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-1102">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1102">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-1103">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1103">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-1104">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-1104">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-1105">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1105">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-1106">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1106">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1107">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1107">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1108">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1108">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1109">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-1109">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-1110">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-1110">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-1111">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1111">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-1112">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1112">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-1113">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1113">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1114">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1114">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1115">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-1115">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-1116">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1116">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-1117">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1117">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1118">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1118">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1119">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1119">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-1120">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-1120">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-1121">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1121">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-1122">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-1122">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-1123">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-1123">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-1124">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1124">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-1125">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1125">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-1126">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1126">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1127">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-1127">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1128">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-1128">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-1129">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1129">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1130">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1130">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1131">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-1131">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-1132">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1132">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-1133">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1133">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-1134">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-1134">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-1135">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-1135">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-1136">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-1136">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-1137">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1137">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-1138">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1138">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-1139">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1139">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-1140">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1140">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="0cbba-1141">DXGI_FORMAT_R32G8X24 \_ Typen losen<sup>PCs</sup> (19)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1141">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="0cbba-1142">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1142">Target</span></span> | <span data-ttu-id="0cbba-1143">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-1143">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-1144">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1144">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-1145">64</span><span class="sxs-lookup"><span data-stu-id="0cbba-1145">64</span></span> |
| <span data-ttu-id="0cbba-1146">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1146">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-1147">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1147">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1148">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-1148">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1149">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-1149">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1150">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1150">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1151">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1151">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-1152">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1152">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-1153">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1153">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-1154">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-1154">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-1155">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1155">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-1156">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1156">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1157">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1157">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1158">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1158">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1159">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-1159">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-1160">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-1160">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-1161">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1161">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-1162">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1162">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-1163">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1163">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1164">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1164">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1165">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-1165">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-1166">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1166">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-1167">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1167">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1168">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1168">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1169">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1169">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-1170">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-1170">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-1171">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1171">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-1172">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-1172">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-1173">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-1173">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-1174">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1174">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-1175">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1175">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-1176">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1176">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1177">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-1177">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1178">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-1178">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-1179">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1179">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1180">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1180">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1181">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-1181">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-1182">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1182">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-1183">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1183">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-1184">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-1184">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-1185">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-1185">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-1186">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-1186">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-1187">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1187">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-1188">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1188">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-1189">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1189">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-1190">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1190">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a><span data-ttu-id="0cbba-1191">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup></sup> -(20)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1191">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FNS</sup> (20)</span></span>
| <span data-ttu-id="0cbba-1192">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1192">Target</span></span> | <span data-ttu-id="0cbba-1193">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-1193">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-1194">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1194">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-1195">64</span><span class="sxs-lookup"><span data-stu-id="0cbba-1195">64</span></span> |
| <span data-ttu-id="0cbba-1196">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1196">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-1197">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1197">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1198">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-1198">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1199">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-1199">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1200">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1200">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1201">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1201">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-1202">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1202">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-1203">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1203">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-1204">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-1204">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-1205">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1205">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-1206">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1206">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1207">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1207">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1208">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1208">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1209">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-1209">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-1210">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-1210">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-1211">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1211">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-1212">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1212">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-1213">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1213">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1214">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1214">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1215">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-1215">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-1216">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1216">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-1217">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1217">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1218">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1218">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1219">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1219">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-1220">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-1220">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-1221">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1221">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-1222">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-1222">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-1223">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-1223">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-1224">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1224">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-1225">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1225">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-1226">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1226">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1227">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-1227">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1228">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-1228">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-1229">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1229">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1230">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1230">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1231">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-1231">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-1232">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1232">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-1233">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1233">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-1234">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-1234">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-1235">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-1235">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-1236">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-1236">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-1237">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1237">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-1238">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1238">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-1239">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1239">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-1240">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1240">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a><span data-ttu-id="0cbba-1241">DXGI_FORMAT_R32 \_ float \_ X8X24 \_ typlose<sup></sup> Rechtschreibfehler (21)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1241">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FNS</sup> (21)</span></span>
| <span data-ttu-id="0cbba-1242">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1242">Target</span></span> | <span data-ttu-id="0cbba-1243">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-1243">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-1244">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1244">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-1245">64</span><span class="sxs-lookup"><span data-stu-id="0cbba-1245">64</span></span> |
| <span data-ttu-id="0cbba-1246">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1246">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-1247">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1247">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1248">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-1248">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1249">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-1249">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1250">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1250">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1251">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1251">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-1252">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1252">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-1253">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1253">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-1254">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-1254">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-1255">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1255">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-1256">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1256">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1257">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1257">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1258">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1258">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1259">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-1259">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-1260">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-1260">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-1261">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1261">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-1262">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1262">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-1263">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1263">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1264">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1264">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1265">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-1265">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-1266">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1266">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-1267">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1267">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1268">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1268">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1269">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1269">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-1270">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-1270">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-1271">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1271">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-1272">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-1272">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-1273">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-1273">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-1274">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1274">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-1275">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1275">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-1276">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1276">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1277">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-1277">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1278">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-1278">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-1279">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1279">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1280">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1280">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1281">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-1281">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-1282">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1282">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-1283">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1283">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-1284">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-1284">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-1285">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-1285">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-1286">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-1286">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-1287">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1287">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-1288">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1288">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-1289">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1289">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-1290">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1290">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a><span data-ttu-id="0cbba-1291">DXGI_FORMAT_X32 \_ typlose \_ G8X24 \_ uint<sup></sup> -Fehler (22)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1291">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FNS</sup> (22)</span></span>
| <span data-ttu-id="0cbba-1292">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1292">Target</span></span> | <span data-ttu-id="0cbba-1293">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-1293">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-1294">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1294">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-1295">64</span><span class="sxs-lookup"><span data-stu-id="0cbba-1295">64</span></span> |
| <span data-ttu-id="0cbba-1296">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1296">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-1297">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1297">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1298">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-1298">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1299">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-1299">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1300">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1300">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1301">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1301">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-1302">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1302">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-1303">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1303">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-1304">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-1304">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-1305">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1305">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-1306">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1306">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1307">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1307">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1308">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1308">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1309">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-1309">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-1310">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-1310">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-1311">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1311">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-1312">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1312">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-1313">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1313">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1314">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1314">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1315">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-1315">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-1316">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1316">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-1317">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1317">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1318">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1318">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1319">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1319">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-1320">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-1320">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-1321">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1321">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-1322">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-1322">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-1323">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-1323">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-1324">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1324">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-1325">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1325">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-1326">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1326">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1327">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-1327">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1328">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-1328">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-1329">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1329">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1330">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1330">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1331">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-1331">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-1332">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1332">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-1333">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1333">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-1334">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-1334">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-1335">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-1335">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-1336">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-1336">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-1337">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1337">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-1338">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1338">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-1339">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1339">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-1340">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1340">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="0cbba-1341">DXGI_FORMAT_R10G10B10A2 \_ typlosen<sup>PCs</sup> (23)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1341">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="0cbba-1342">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1342">Target</span></span> | <span data-ttu-id="0cbba-1343">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-1343">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-1344">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1344">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-1345">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-1345">32</span></span> |
| <span data-ttu-id="0cbba-1346">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1346">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-1347">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1347">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1348">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-1348">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1349">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-1349">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1350">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1350">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1351">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1351">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-1352">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1352">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-1353">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1353">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-1354">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-1354">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-1355">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1355">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-1356">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1356">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1357">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1357">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1358">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1358">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1359">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-1359">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-1360">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-1360">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-1361">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1361">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-1362">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1362">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-1363">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1363">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1364">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1364">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1365">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-1365">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-1366">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1366">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-1367">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1367">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1368">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1368">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1369">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1369">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-1370">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-1370">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-1371">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1371">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-1372">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-1372">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-1373">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-1373">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-1374">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1374">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-1375">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1375">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-1376">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1376">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1377">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-1377">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1378">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-1378">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-1379">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1379">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1380">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1380">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1381">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-1381">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-1382">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1382">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-1383">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1383">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-1384">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-1384">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-1385">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-1385">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-1386">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-1386">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-1387">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1387">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-1388">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1388">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-1389">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1389">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-1390">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1390">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a><span data-ttu-id="0cbba-1391">DXGI_FORMAT_R10G10B10A2 \_ unorm<sup></sup> -Fehler (24)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1391">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FNS</sup> (24)</span></span>
| <span data-ttu-id="0cbba-1392">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1392">Target</span></span> | <span data-ttu-id="0cbba-1393">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-1393">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-1394">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1394">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-1395">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-1395">32</span></span> |
| <span data-ttu-id="0cbba-1396">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1396">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-1397">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1397">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1398">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-1398">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1399">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-1399">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1400">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1400">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1401">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1401">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-1402">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1402">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-1403">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1403">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-1404">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-1404">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-1405">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1405">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-1406">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1406">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1407">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1407">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1408">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1408">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1409">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-1409">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-1410">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-1410">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-1411">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1411">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-1412">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1412">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-1413">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1413">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1414">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1414">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1415">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-1415">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-1416">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1416">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-1417">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1417">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1418">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1418">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1419">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1419">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-1420">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-1420">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-1421">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1421">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-1422">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-1422">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-1423">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-1423">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-1424">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1424">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-1425">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1425">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-1426">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1426">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1427">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-1427">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1428">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-1428">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-1429">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1429">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1430">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1430">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1431">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-1431">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-1432">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1432">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-1433">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1433">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-1434">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-1434">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-1435">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-1435">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-1436">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-1436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-1437">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-1438">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-1439">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1439">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1441">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a><span data-ttu-id="0cbba-1442">DXGI_FORMAT_R10G10B10A2 \_ uint<sup></sup> -(25)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1442">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FNS</sup> (25)</span></span>
| <span data-ttu-id="0cbba-1443">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1443">Target</span></span> | <span data-ttu-id="0cbba-1444">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-1444">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-1445">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-1446">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-1446">32</span></span> |
| <span data-ttu-id="0cbba-1447">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1447">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-1448">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1448">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1449">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-1449">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1450">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-1450">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1451">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1451">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1452">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1452">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-1453">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1453">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-1454">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1454">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-1455">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-1455">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-1456">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1456">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-1457">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1457">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1458">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1458">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1459">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1459">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1460">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-1460">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-1461">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-1461">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-1462">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1462">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-1463">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1463">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-1464">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1464">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1465">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1465">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1466">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-1466">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-1467">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1467">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-1468">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1468">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1469">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1469">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1470">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1470">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-1471">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-1471">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-1472">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1472">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-1473">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-1473">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-1474">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-1474">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-1475">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1475">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-1476">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1476">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-1477">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1477">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1478">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-1478">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1479">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-1479">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-1480">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1480">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1481">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1481">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1482">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-1482">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-1483">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1483">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-1484">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1484">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-1485">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-1485">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-1486">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-1486">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-1487">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-1487">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-1488">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1488">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-1489">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1489">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-1490">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1490">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-1491">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1491">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a><span data-ttu-id="0cbba-1492">DXGI_FORMAT_R10G10B10 \_ XR \_ Bias \_ a2 \_ unorm<sup></sup> -Fehler (89)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1492">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FNS</sup> (89)</span></span>
| <span data-ttu-id="0cbba-1493">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1493">Target</span></span> | <span data-ttu-id="0cbba-1494">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-1494">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-1495">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1495">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-1496">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-1496">32</span></span> |
| <span data-ttu-id="0cbba-1497">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1497">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-1498">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1498">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1499">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-1499">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1500">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-1500">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1501">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1501">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1502">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1502">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-1503">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1503">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-1504">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1504">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-1505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-1505">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-1506">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1506">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-1507">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1507">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1508">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1509">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1510">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-1510">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-1511">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-1511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-1512">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1512">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-1513">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1513">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-1514">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1514">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1515">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1515">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1516">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-1516">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-1517">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1517">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-1518">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1518">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1519">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1519">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1520">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1520">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-1521">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-1521">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-1522">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1522">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-1523">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-1523">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-1524">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-1524">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-1525">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1525">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-1526">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1526">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-1527">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1527">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1528">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-1528">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1529">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-1529">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-1530">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1530">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1531">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1531">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1532">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-1532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-1533">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-1534">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1534">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-1535">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-1535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-1536">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-1536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-1537">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-1537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-1538">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-1539">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-1540">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1540">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-1541">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="0cbba-1542">DXGI_FORMAT_R11G11B10 \_ float<sup></sup> -Datentyp (26)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1542">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="0cbba-1543">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1543">Target</span></span> | <span data-ttu-id="0cbba-1544">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-1544">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-1545">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-1546">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-1546">32</span></span> |
| <span data-ttu-id="0cbba-1547">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1547">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-1548">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1548">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1549">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-1549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1550">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-1550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1551">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1552">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-1553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1553">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-1554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1554">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-1555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-1555">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-1556">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-1557">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1558">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1559">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1560">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-1560">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-1561">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-1561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-1562">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1562">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-1563">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-1564">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1564">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1565">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1566">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-1566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-1567">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-1568">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1569">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1570">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1570">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-1571">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-1571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-1572">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-1573">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-1573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-1574">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-1574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-1575">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-1576">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-1577">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1578">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-1578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1579">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-1579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-1580">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1581">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1582">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-1582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-1583">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-1584">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1584">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-1585">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-1585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-1586">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-1586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-1587">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-1587">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-1588">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1588">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-1589">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1589">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-1590">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1590">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-1591">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1591">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="0cbba-1592">DXGI_FORMAT_R8G8B8A8 \_ typlosen<sup>PCs</sup> (27)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1592">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="0cbba-1593">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1593">Target</span></span> | <span data-ttu-id="0cbba-1594">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-1594">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-1595">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1595">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-1596">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-1596">32</span></span> |
| <span data-ttu-id="0cbba-1597">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1597">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-1598">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1598">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1599">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-1599">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1600">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-1600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1601">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1602">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-1603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1603">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-1604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1604">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-1605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-1605">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-1606">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-1607">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1608">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1609">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1610">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-1610">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-1611">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-1611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-1612">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1612">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-1613">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-1614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1614">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1615">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1616">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-1616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-1617">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-1618">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1619">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1620">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1620">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-1621">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-1621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-1622">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-1623">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-1623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-1624">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-1624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-1625">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-1626">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-1627">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1628">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-1628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1629">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-1629">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-1630">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1630">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1631">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1631">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1632">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-1632">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-1633">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1633">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-1634">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1634">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-1635">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-1635">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-1636">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-1636">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-1637">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-1637">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-1638">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1638">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-1639">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1639">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-1640">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1640">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-1641">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1641">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a><span data-ttu-id="0cbba-1642">DXGI_FORMAT_R8G8B8A8 \_ unorm<sup></sup> -Fehler (28)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1642">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FNS</sup> (28)</span></span>
| <span data-ttu-id="0cbba-1643">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1643">Target</span></span> | <span data-ttu-id="0cbba-1644">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-1644">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-1645">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1645">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-1646">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-1646">32</span></span> |
| <span data-ttu-id="0cbba-1647">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1647">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1649">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1649">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1650">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-1650">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1652">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-1652">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1653">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1653">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1654">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1654">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-1655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1655">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1657">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-1659">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1661">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1661">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1663">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1663">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1665">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1665">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1666">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1666">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1667">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-1667">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-1668">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-1668">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-1669">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1669">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1671">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1671">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1673">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1673">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1675">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1675">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1677">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-1677">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-1678">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1678">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-1679">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1679">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1680">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1680">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1681">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1681">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-1682">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-1682">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-1683">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1683">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-1684">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-1684">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-1685">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-1685">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-1686">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1686">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-1687">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1687">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-1688">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1688">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1689">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-1689">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1690">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-1690">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1692">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1692">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-1694">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1694">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-1696">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-1696">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-1698">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1698">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1700">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1700">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-1701">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-1701">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1703">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-1703">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-1704">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-1704">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-1705">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1705">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-1707">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1707">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1709">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1709">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1711">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1711">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a><span data-ttu-id="0cbba-1712">DXGI_FORMAT_R8G8B8A8 \_ unorm \_ sRGB<sup></sup> -Fehler (29)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1712">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FNS</sup> (29)</span></span>
| <span data-ttu-id="0cbba-1713">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1713">Target</span></span> | <span data-ttu-id="0cbba-1714">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-1714">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-1715">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1715">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-1716">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-1716">32</span></span> |
| <span data-ttu-id="0cbba-1717">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1717">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1719">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1719">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1720">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-1720">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1721">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-1721">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1722">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1722">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1723">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1723">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-1724">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1724">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1726">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1726">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1728">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-1728">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1730">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1730">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1732">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1732">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1734">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1734">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1735">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1735">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1736">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-1736">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-1737">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-1737">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-1738">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1738">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1740">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1740">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1742">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1742">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1744">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1744">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1746">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-1746">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-1747">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1747">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-1748">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1748">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1749">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1749">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1750">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1750">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-1751">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-1751">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-1752">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1752">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-1753">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-1753">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-1754">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-1754">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-1755">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1755">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-1756">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1756">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-1757">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1757">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1758">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-1758">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1759">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-1759">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1761">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1761">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-1763">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1763">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-1765">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-1765">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-1767">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1767">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1769">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1769">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-1770">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-1770">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1772">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-1772">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-1773">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-1773">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-1774">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1774">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-1776">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1776">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1778">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1778">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1780">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1780">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a><span data-ttu-id="0cbba-1781">DXGI_FORMAT_R8G8B8A8 \_ uint<sup></sup> -(30)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1781">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FNS</sup> (30)</span></span>
| <span data-ttu-id="0cbba-1782">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1782">Target</span></span> | <span data-ttu-id="0cbba-1783">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-1783">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-1784">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1784">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-1785">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-1785">32</span></span> |
| <span data-ttu-id="0cbba-1786">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1786">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1788">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1788">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1789">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-1789">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1791">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-1791">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1792">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1792">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1793">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1793">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-1794">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1794">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-1795">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1795">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-1796">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-1796">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-1797">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1797">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-1798">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1798">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1799">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1799">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1800">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1800">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1801">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-1801">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-1802">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-1802">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-1803">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1803">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-1804">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1804">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-1805">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1805">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1806">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1806">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1807">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-1807">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-1808">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1808">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-1809">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1809">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1810">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1810">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1811">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1811">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-1812">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-1812">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-1813">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1813">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-1814">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-1814">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-1815">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-1815">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-1816">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1816">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-1817">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1817">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-1818">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1818">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1819">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-1819">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1820">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-1820">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-1821">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1821">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1822">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1822">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1823">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-1823">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-1824">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1824">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-1825">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1825">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-1826">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-1826">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-1827">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-1827">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-1828">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-1828">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-1829">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1829">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-1830">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1830">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-1831">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1831">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-1832">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1832">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a><span data-ttu-id="0cbba-1833">\_Snorm-<sup></sup> snorm (31) DXGI_FORMAT_R8G8B8A8</span><span class="sxs-lookup"><span data-stu-id="0cbba-1833">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FNS</sup> (31)</span></span>
| <span data-ttu-id="0cbba-1834">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1834">Target</span></span> | <span data-ttu-id="0cbba-1835">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-1835">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-1836">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1836">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-1837">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-1837">32</span></span> |
| <span data-ttu-id="0cbba-1838">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1838">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1840">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1840">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1841">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-1841">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1842">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-1842">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1843">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1843">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1844">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1844">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-1845">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1845">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1847">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1847">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-1848">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-1848">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1850">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1850">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1852">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1852">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1854">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1854">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1855">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1855">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1856">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-1856">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-1857">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-1857">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-1858">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1858">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1860">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1860">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-1861">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1861">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1862">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1862">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1863">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-1863">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-1864">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1864">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-1865">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1865">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1866">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1866">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1867">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1867">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-1868">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-1868">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-1869">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1869">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-1870">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-1870">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-1871">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-1871">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-1872">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1872">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-1873">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1873">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-1874">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1874">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1875">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-1875">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1876">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-1876">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1878">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1878">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1879">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1879">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1880">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-1880">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-1881">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1881">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-1882">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1882">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-1883">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-1883">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-1884">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-1884">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-1885">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-1885">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-1886">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1886">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-1887">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1887">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-1888">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1888">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-1889">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1889">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a><span data-ttu-id="0cbba-1890">DXGI_FORMAT_R8G8B8A8 \_ Sint<sup></sup> -SPT (32)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1890">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FNS</sup> (32)</span></span>
| <span data-ttu-id="0cbba-1891">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1891">Target</span></span> | <span data-ttu-id="0cbba-1892">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-1892">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-1893">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1893">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-1894">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-1894">32</span></span> |
| <span data-ttu-id="0cbba-1895">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1895">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-1896">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1896">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1897">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-1897">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1898">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-1898">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1899">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1899">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1900">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1900">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-1901">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1901">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-1902">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1902">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-1903">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-1903">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-1904">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1904">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-1905">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1905">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1906">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1906">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1907">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1907">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1908">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-1908">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-1909">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-1909">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-1910">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1910">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-1911">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1911">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-1912">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1912">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1913">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1913">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1914">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-1914">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-1915">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1915">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-1916">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1916">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1917">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1917">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1918">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1918">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-1919">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-1919">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-1920">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1920">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-1921">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-1921">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-1922">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-1922">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-1923">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1923">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-1924">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1924">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-1925">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1925">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1926">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-1926">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1927">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-1927">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-1928">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1928">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1929">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1929">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1930">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-1930">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-1931">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1931">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-1932">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1932">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-1933">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-1933">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-1934">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-1934">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-1935">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-1935">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-1936">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1936">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-1937">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1937">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-1938">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1938">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-1939">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1939">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="0cbba-1940">DXGI_FORMAT_R16G16 \_ Typen losen<sup>PCs</sup> (33)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1940">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="0cbba-1941">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1941">Target</span></span> | <span data-ttu-id="0cbba-1942">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-1942">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-1943">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1943">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-1944">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-1944">32</span></span> |
| <span data-ttu-id="0cbba-1945">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1945">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-1946">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1946">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1947">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-1947">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1948">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-1948">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1949">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1949">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1950">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1950">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-1951">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1951">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-1952">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-1952">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-1953">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-1953">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-1954">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1954">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-1955">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1955">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1956">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1956">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1957">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1957">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-1958">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-1958">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-1959">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-1959">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-1960">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1960">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-1961">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-1961">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-1962">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1962">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1963">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1963">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1964">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-1964">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-1965">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1965">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-1966">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1966">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1967">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1967">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-1968">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-1968">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-1969">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-1969">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-1970">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1970">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-1971">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-1971">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-1972">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-1972">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-1973">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1973">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-1974">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-1974">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-1975">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1975">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1976">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-1976">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-1977">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-1977">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-1978">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1978">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1979">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-1979">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-1980">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-1980">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-1981">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1981">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-1982">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1982">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-1983">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-1983">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-1984">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-1984">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-1985">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-1985">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-1986">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1986">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-1987">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-1987">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-1988">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1988">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-1989">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-1989">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a><span data-ttu-id="0cbba-1990">DXGI_FORMAT_R16G16 \_ float-"<sup>f</sup> " (34)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1990">DXGI_FORMAT_R16G16\_FLOAT<sup>FNS</sup> (34)</span></span>
| <span data-ttu-id="0cbba-1991">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-1991">Target</span></span> | <span data-ttu-id="0cbba-1992">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-1992">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-1993">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-1993">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-1994">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-1994">32</span></span> |
| <span data-ttu-id="0cbba-1995">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-1995">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-1997">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-1997">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-1998">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-1998">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2000">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-2000">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2001">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2001">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2002">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2002">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-2003">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2003">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2005">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2005">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2007">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-2007">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2009">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2009">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2011">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2011">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2012">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2012">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2013">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2013">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2014">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-2014">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-2015">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-2015">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-2016">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2016">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2018">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2018">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2020">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2020">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2022">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2022">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2023">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-2023">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-2024">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2024">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-2025">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2025">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2026">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2026">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2027">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2027">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-2028">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-2028">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-2029">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2029">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-2030">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-2030">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-2031">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-2031">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-2032">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2032">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-2033">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2033">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-2034">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2034">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2035">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-2035">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2036">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-2036">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2038">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2038">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-2040">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2040">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-2042">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-2042">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-2044">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2044">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2046">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2046">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-2047">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-2047">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-2048">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-2048">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-2049">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-2049">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-2050">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2050">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-2051">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2051">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-2052">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2052">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-2053">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2053">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a><span data-ttu-id="0cbba-2054">DXGI_FORMAT_R16G16 \_ unorm<sup></sup> -Fehler (35)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2054">DXGI_FORMAT_R16G16\_UNORM<sup>FNS</sup> (35)</span></span>
| <span data-ttu-id="0cbba-2055">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2055">Target</span></span> | <span data-ttu-id="0cbba-2056">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-2056">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-2057">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2057">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-2058">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-2058">32</span></span> |
| <span data-ttu-id="0cbba-2059">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2059">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2061">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2061">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2062">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-2062">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2063">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-2063">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2064">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2064">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2065">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2065">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-2066">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2066">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2068">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2068">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2070">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-2070">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2072">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2072">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2074">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2074">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2076">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2076">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2077">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2077">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2078">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-2078">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-2079">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-2079">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-2080">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2080">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2082">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2082">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2084">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2084">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2086">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2086">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2087">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-2087">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-2088">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2088">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-2089">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2089">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2090">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2090">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2091">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2091">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-2092">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-2092">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-2093">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2093">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-2094">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-2094">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-2095">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-2095">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-2096">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2096">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-2097">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2097">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-2098">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2098">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2099">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-2099">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2100">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-2100">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2102">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2102">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-2104">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2104">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-2106">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-2106">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-2108">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2108">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2110">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2110">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-2111">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-2111">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-2112">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-2112">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-2113">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-2113">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-2114">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2114">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-2115">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2115">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-2116">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2116">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-2117">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2117">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a><span data-ttu-id="0cbba-2118">DXGI_FORMAT_R16G16 \_ uint<sup></sup> -Benutzerkonten (36)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2118">DXGI_FORMAT_R16G16\_UINT<sup>FNS</sup> (36)</span></span>
| <span data-ttu-id="0cbba-2119">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2119">Target</span></span> | <span data-ttu-id="0cbba-2120">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-2120">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-2121">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2121">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-2122">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-2122">32</span></span> |
| <span data-ttu-id="0cbba-2123">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2123">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-2124">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2124">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2125">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-2125">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2126">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-2126">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2127">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2127">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2128">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2128">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-2129">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2129">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-2130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2130">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-2131">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-2131">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-2132">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2132">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-2133">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2133">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2134">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2134">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2135">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2135">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2136">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-2136">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-2137">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-2137">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-2138">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2138">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-2139">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2139">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-2140">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2140">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2141">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2141">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2142">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-2142">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-2143">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2143">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-2144">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2144">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2145">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2145">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2146">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2146">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-2147">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-2147">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-2148">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2148">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-2149">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-2149">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-2150">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-2150">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-2151">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2151">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-2152">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2152">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-2153">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2153">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2154">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-2154">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2155">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-2155">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-2156">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2156">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2157">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2157">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2158">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-2158">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-2159">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2159">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-2160">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2160">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-2161">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-2161">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-2162">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-2162">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-2163">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-2163">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-2164">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2164">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-2165">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2165">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-2166">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2166">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-2167">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2167">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a><span data-ttu-id="0cbba-2168">DXGI_FORMAT_R16G16 \_ snorm<sup></sup> -Kenn Wort (37)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2168">DXGI_FORMAT_R16G16\_SNORM<sup>FNS</sup> (37)</span></span>
| <span data-ttu-id="0cbba-2169">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2169">Target</span></span> | <span data-ttu-id="0cbba-2170">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-2170">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-2171">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2171">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-2172">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-2172">32</span></span> |
| <span data-ttu-id="0cbba-2173">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2173">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2175">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2175">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2176">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-2176">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2178">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-2178">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2179">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2179">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2180">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2180">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-2181">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2181">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2183">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2185">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-2185">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2187">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2187">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2189">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2189">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2191">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2191">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2192">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2192">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2193">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-2193">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-2194">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-2194">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-2195">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2195">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2197">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2197">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-2198">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2198">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2199">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2199">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2200">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-2200">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-2201">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2201">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-2202">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2202">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2203">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2203">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2204">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2204">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-2205">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-2205">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-2206">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2206">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-2207">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-2207">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-2208">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-2208">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-2209">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2209">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-2210">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2210">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-2211">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2211">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2212">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-2212">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2213">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-2213">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2215">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2215">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2216">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2216">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2217">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-2217">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-2218">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2218">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-2219">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2219">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-2220">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-2220">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-2221">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-2221">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-2222">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-2222">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-2223">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2223">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-2224">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2224">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-2225">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2225">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-2226">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2226">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a><span data-ttu-id="0cbba-2227">DXGI_FORMAT_R16G16 \_ Sint<sup></sup> -SPT (38)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2227">DXGI_FORMAT_R16G16\_SINT<sup>FNS</sup> (38)</span></span>
| <span data-ttu-id="0cbba-2228">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2228">Target</span></span> | <span data-ttu-id="0cbba-2229">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-2229">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-2230">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2230">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-2231">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-2231">32</span></span> |
| <span data-ttu-id="0cbba-2232">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2232">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2234">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2234">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2235">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-2235">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2237">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-2237">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2238">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2238">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2239">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2239">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-2240">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2240">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-2241">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2241">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-2242">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-2242">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-2243">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2243">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-2244">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2244">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2245">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2245">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2246">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2246">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2247">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-2247">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-2248">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-2248">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-2249">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2249">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-2250">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2250">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-2251">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2251">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2252">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2252">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2253">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-2253">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-2254">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2254">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-2255">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2255">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2256">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2256">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2257">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2257">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-2258">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-2258">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-2259">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2259">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-2260">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-2260">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-2261">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-2261">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-2262">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2262">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-2263">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2263">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-2264">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2264">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2265">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-2265">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2266">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-2266">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-2267">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2267">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2268">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2268">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2269">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-2269">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-2270">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2270">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-2271">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2271">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-2272">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-2272">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-2273">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-2273">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-2274">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-2274">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-2275">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2275">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-2276">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2276">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-2277">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2277">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-2278">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2278">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="0cbba-2279">DXGI_FORMAT_R32 \_ Typen losen<sup>PCs</sup> (39)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2279">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="0cbba-2280">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2280">Target</span></span> | <span data-ttu-id="0cbba-2281">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-2281">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-2282">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2282">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-2283">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-2283">32</span></span> |
| <span data-ttu-id="0cbba-2284">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2284">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-2285">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2285">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2286">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-2286">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2287">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-2287">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2288">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2288">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2289">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2289">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-2290">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2290">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-2291">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2291">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-2292">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-2292">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-2293">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2293">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-2294">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2294">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2295">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2295">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2296">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2296">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2297">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-2297">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-2298">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-2298">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-2299">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2299">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-2300">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2300">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-2301">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2301">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2302">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2302">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2303">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-2303">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-2304">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2304">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-2305">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2305">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2306">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2306">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2307">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2307">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-2308">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-2308">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-2309">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2309">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-2310">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-2310">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-2311">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-2311">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-2312">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2312">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-2313">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2313">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-2314">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2314">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2315">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-2315">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2316">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-2316">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-2317">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2318">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2319">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-2319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-2320">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-2321">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2321">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-2322">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-2322">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-2323">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-2323">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-2324">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-2324">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-2325">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2325">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-2326">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2326">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-2327">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2327">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-2328">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2328">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a><span data-ttu-id="0cbba-2329">DXGI_FORMAT_D32 \_ float-"<sup>f</sup> " (40)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2329">DXGI_FORMAT_D32\_FLOAT<sup>FNS</sup> (40)</span></span>
| <span data-ttu-id="0cbba-2330">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2330">Target</span></span> | <span data-ttu-id="0cbba-2331">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-2331">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-2332">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2332">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-2333">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-2333">32</span></span> |
| <span data-ttu-id="0cbba-2334">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2334">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-2335">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2335">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2336">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-2336">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2337">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-2337">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2338">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2338">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2339">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2339">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-2340">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2340">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-2341">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2341">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-2342">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-2342">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-2343">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2343">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-2344">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2344">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2345">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2345">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2346">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2346">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2347">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-2347">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-2348">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-2348">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-2349">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2349">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-2350">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2350">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-2351">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2351">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2352">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2352">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2353">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-2353">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-2354">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2354">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-2355">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2355">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2356">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2356">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2357">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2357">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-2358">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-2358">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-2359">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2359">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-2360">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-2360">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-2361">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-2361">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-2362">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2362">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-2363">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2363">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-2364">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2364">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2365">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-2365">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2366">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-2366">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-2367">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2367">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2368">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2368">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2369">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-2369">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-2370">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2370">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-2371">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2371">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-2372">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-2372">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-2373">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-2373">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-2374">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-2374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-2375">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-2376">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-2377">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2377">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-2378">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a><span data-ttu-id="0cbba-2379">DXGI_FORMAT_R32 \_ float-"<sup>f</sup> " (41)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2379">DXGI_FORMAT_R32\_FLOAT<sup>FNS</sup> (41)</span></span>
| <span data-ttu-id="0cbba-2380">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2380">Target</span></span> | <span data-ttu-id="0cbba-2381">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-2381">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-2382">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-2383">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-2383">32</span></span> |
| <span data-ttu-id="0cbba-2384">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2384">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2386">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2386">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2387">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-2387">Input Assembler Vertex Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2389">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-2389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2390">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2391">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-2392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2392">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2394">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2394">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2396">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-2396">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2398">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2398">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2400">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2400">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2401">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2401">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2402">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2402">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2403">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-2403">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-2404">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-2404">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-2405">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2405">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2407">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2407">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2409">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2409">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2411">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2411">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2412">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-2412">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-2413">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2413">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-2414">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2414">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2415">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2415">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2416">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2416">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-2417">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-2417">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-2418">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2418">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-2419">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-2419">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-2420">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-2420">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-2421">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2421">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-2422">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2422">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-2423">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2423">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2424">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-2424">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2425">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-2425">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2427">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2427">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-2429">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2429">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-2431">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-2431">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-2433">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2433">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2435">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2435">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-2436">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-2436">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-2437">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-2437">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-2438">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-2438">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-2439">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2439">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-2440">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2440">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-2441">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2441">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-2442">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2442">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a><span data-ttu-id="0cbba-2443">DXGI_FORMAT_R32 \_ uint<sup></sup> -Benutzerkonten (42)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2443">DXGI_FORMAT_R32\_UINT<sup>FNS</sup> (42)</span></span>
| <span data-ttu-id="0cbba-2444">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2444">Target</span></span> | <span data-ttu-id="0cbba-2445">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-2445">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-2446">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2446">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-2447">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-2447">32</span></span> |
| <span data-ttu-id="0cbba-2448">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2448">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2450">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2450">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2451">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-2451">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2452">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-2452">Input Assembler Index Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2454">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2454">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2455">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2455">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-2456">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2456">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-2457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2457">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-2458">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-2458">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-2459">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2459">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-2460">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2460">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2461">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2461">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2462">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2462">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2463">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-2463">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-2464">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-2464">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-2465">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2465">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-2466">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2466">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-2467">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2467">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2468">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2468">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2469">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-2469">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-2470">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2470">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-2471">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2471">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2472">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2472">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2473">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2473">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-2474">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-2474">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-2475">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2475">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-2476">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-2476">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-2477">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-2477">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-2478">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2478">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-2479">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2479">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-2480">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2480">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2481">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-2481">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2482">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-2482">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-2483">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2483">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2484">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2484">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2485">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-2485">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-2486">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2486">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-2487">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2487">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-2488">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-2488">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-2489">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-2489">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-2490">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-2490">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-2491">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2491">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-2492">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2492">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-2493">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2493">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-2494">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2494">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a><span data-ttu-id="0cbba-2495">DXGI_FORMAT_R32 \_ Sint<sup></sup> -SPT (43)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2495">DXGI_FORMAT_R32\_SINT<sup>FNS</sup> (43)</span></span>
| <span data-ttu-id="0cbba-2496">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2496">Target</span></span> | <span data-ttu-id="0cbba-2497">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-2497">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-2498">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2498">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-2499">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-2499">32</span></span> |
| <span data-ttu-id="0cbba-2500">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2500">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-2501">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2501">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2502">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-2502">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2503">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-2503">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2504">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2504">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2505">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2505">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-2506">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2506">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-2507">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2507">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-2508">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-2508">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-2509">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2509">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-2510">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2510">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2511">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2511">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2512">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2512">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2513">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-2513">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-2514">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-2514">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-2515">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2515">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-2516">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2516">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-2517">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2517">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2518">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2518">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2519">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-2519">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-2520">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2520">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-2521">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2521">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2522">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2522">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2523">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2523">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-2524">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-2524">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-2525">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2525">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-2526">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-2526">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-2527">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-2527">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-2528">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2528">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-2529">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2529">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-2530">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2530">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2531">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-2531">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2532">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-2532">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-2533">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2533">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2534">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2534">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2535">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-2535">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-2536">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2536">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-2537">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2537">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-2538">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-2538">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-2539">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-2539">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-2540">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-2540">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-2541">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2541">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-2542">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2542">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-2543">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2543">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-2544">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2544">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="0cbba-2545">DXGI_FORMAT_R24G8 \_ Typen losen<sup>PCs</sup> (44)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2545">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="0cbba-2546">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2546">Target</span></span> | <span data-ttu-id="0cbba-2547">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-2547">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-2548">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2548">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-2549">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-2549">32</span></span> |
| <span data-ttu-id="0cbba-2550">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2550">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-2551">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2551">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2552">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-2552">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2553">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-2553">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2554">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2554">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2555">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2555">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-2556">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2556">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-2557">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2557">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-2558">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-2558">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-2559">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2559">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-2560">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2560">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2561">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2561">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2562">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2562">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2563">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-2563">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-2564">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-2564">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-2565">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2565">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-2566">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2566">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-2567">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2567">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2568">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2568">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2569">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-2569">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-2570">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2570">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-2571">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2571">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2572">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2572">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2573">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2573">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-2574">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-2574">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-2575">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2575">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-2576">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-2576">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-2577">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-2577">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-2578">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2578">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-2579">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2579">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-2580">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2580">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2581">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-2581">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2582">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-2582">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-2583">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2583">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2584">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2584">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2585">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-2585">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-2586">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2586">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-2587">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2587">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-2588">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-2588">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-2589">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-2589">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-2590">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-2590">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-2591">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2591">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-2592">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2592">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-2593">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2593">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-2594">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a><span data-ttu-id="0cbba-2595">DXGI_FORMAT_D24 \_ unorm \_ S8 \_ uint<sup></sup> -Fehler (45)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2595">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FNS</sup> (45)</span></span>
| <span data-ttu-id="0cbba-2596">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2596">Target</span></span> | <span data-ttu-id="0cbba-2597">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-2597">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-2598">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-2599">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-2599">32</span></span> |
| <span data-ttu-id="0cbba-2600">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2600">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2602">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2602">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2603">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-2603">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2604">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-2604">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2605">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2605">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2606">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2606">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-2607">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2607">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2609">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2609">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-2610">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-2610">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-2611">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2611">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-2612">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2612">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2613">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2614">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2615">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-2615">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-2616">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-2616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-2617">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2617">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-2618">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2618">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-2619">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2619">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2620">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2620">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2621">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-2621">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-2622">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2622">Depth/Stencil Target</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2624">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2624">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2625">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2625">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2626">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2626">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-2627">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-2627">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-2628">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2628">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-2629">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-2629">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-2630">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-2630">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-2631">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2631">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-2632">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2632">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-2633">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2633">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2634">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-2634">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2635">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-2635">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-2636">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2636">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-2638">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2638">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-2640">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-2640">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-2642">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2642">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-2643">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2643">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-2644">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-2644">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-2645">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-2645">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-2646">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-2646">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-2647">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2647">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-2648">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2648">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-2649">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2649">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-2650">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2650">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a><span data-ttu-id="0cbba-2651">DXGI_FORMAT_R24 \_ unorm \_ X8- \_ typlosen, nicht (46)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="0cbba-2651">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FNS</sup> (46)</span></span>
| <span data-ttu-id="0cbba-2652">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2652">Target</span></span> | <span data-ttu-id="0cbba-2653">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-2653">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-2654">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2654">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-2655">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-2655">32</span></span> |
| <span data-ttu-id="0cbba-2656">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2656">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-2657">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2657">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2658">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-2658">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2659">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-2659">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2660">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2660">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2661">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2661">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-2662">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2662">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-2663">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2663">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-2664">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-2664">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-2665">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2665">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-2666">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2666">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2667">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2667">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2668">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2668">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2669">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-2669">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-2670">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-2670">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-2671">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2671">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-2672">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2672">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-2673">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2673">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2674">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2674">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2675">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-2675">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-2676">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2676">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-2677">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2677">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2678">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2678">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2679">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2679">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-2680">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-2680">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-2681">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2681">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-2682">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-2682">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-2683">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-2683">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-2684">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2684">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-2685">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2685">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-2686">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2686">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2687">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-2687">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2688">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-2688">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-2689">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2689">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2690">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2690">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2691">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-2691">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-2692">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2692">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-2693">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2693">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-2694">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-2694">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-2695">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-2695">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-2696">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-2696">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-2697">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2697">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-2698">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2698">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-2699">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2699">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-2700">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2700">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a><span data-ttu-id="0cbba-2701">DXGI_FORMAT_X24 \_ typlose \_ G8 \_ uint<sup></sup> -Benutzerkonten (47)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2701">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FNS</sup> (47)</span></span>
| <span data-ttu-id="0cbba-2702">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2702">Target</span></span> | <span data-ttu-id="0cbba-2703">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-2703">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-2704">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2704">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-2705">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-2705">32</span></span> |
| <span data-ttu-id="0cbba-2706">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2706">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-2707">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2707">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2708">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-2708">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2709">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-2709">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2710">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2710">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2711">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2711">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-2712">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2712">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-2713">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2713">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-2714">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-2714">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-2715">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2715">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-2716">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2716">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2717">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2717">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2718">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2718">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2719">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-2719">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-2720">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-2720">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-2721">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2721">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-2722">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2722">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-2723">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2723">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2724">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2724">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2725">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-2725">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-2726">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2726">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-2727">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2727">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2728">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2728">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2729">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2729">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-2730">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-2730">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-2731">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2731">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-2732">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-2732">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-2733">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-2733">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-2734">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2734">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-2735">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2735">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-2736">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2736">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2737">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-2737">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2738">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-2738">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-2739">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2739">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2740">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2740">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2741">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-2741">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-2742">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-2743">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2743">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-2744">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-2744">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-2745">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-2745">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-2746">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-2746">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-2747">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2747">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-2748">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2748">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-2749">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2749">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-2750">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2750">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="0cbba-2751">DXGI_FORMAT_R8G8 \_ Typen losen<sup>PCs</sup> (48)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2751">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="0cbba-2752">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2752">Target</span></span> | <span data-ttu-id="0cbba-2753">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-2753">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-2754">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2754">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-2755">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-2755">16</span></span> |
| <span data-ttu-id="0cbba-2756">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2756">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-2757">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2757">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2758">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-2758">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2759">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-2759">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2760">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2760">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2761">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2761">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-2762">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2762">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-2763">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2763">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-2764">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-2764">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-2765">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2765">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-2766">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2766">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2767">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2767">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2768">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2768">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2769">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-2769">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-2770">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-2770">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-2771">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2771">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-2772">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2772">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-2773">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2773">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2774">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2774">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2775">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-2775">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-2776">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2776">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-2777">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2777">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2778">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2778">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2779">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2779">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-2780">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-2780">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-2781">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2781">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-2782">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-2782">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-2783">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-2783">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-2784">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2784">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-2785">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2785">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-2786">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2786">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2787">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-2787">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2788">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-2788">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-2789">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2789">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2790">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2790">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2791">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-2791">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-2792">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2792">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-2793">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2793">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-2794">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-2794">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-2795">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-2795">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-2796">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-2796">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-2797">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2797">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-2798">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2798">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-2799">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2799">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-2800">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2800">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a><span data-ttu-id="0cbba-2801">DXGI_FORMAT_R8G8 \_ unorm<sup></sup> -Fehler (49)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2801">DXGI_FORMAT_R8G8\_UNORM<sup>FNS</sup> (49)</span></span>
| <span data-ttu-id="0cbba-2802">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2802">Target</span></span> | <span data-ttu-id="0cbba-2803">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-2803">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-2804">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2804">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-2805">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-2805">16</span></span> |
| <span data-ttu-id="0cbba-2806">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2806">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2808">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2808">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2809">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-2809">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2810">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-2810">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2811">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2811">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2812">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2812">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-2813">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2813">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2815">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2815">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-2816">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-2816">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-2817">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2817">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2819">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2819">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2821">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2821">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2822">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2822">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2823">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-2823">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-2824">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-2824">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-2825">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2825">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-2826">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2826">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-2827">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2827">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2829">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2829">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2831">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-2831">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-2832">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2832">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-2833">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2833">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2834">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2834">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2835">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2835">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-2836">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-2836">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-2837">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2837">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-2838">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-2838">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-2839">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-2839">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-2840">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2840">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-2841">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2841">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-2842">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2842">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2843">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-2843">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2844">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-2844">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2846">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2846">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2847">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2847">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2848">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-2848">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-2849">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2849">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-2850">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2850">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-2851">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-2851">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-2852">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-2852">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-2853">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-2853">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-2854">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2854">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-2855">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2855">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-2856">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2856">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2858">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2858">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a><span data-ttu-id="0cbba-2859">DXGI_FORMAT_R8G8 \_ uint<sup></sup> -Benutzerkonten (50)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2859">DXGI_FORMAT_R8G8\_UINT<sup>FNS</sup> (50)</span></span>
| <span data-ttu-id="0cbba-2860">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2860">Target</span></span> | <span data-ttu-id="0cbba-2861">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-2861">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-2862">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2862">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-2863">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-2863">16</span></span> |
| <span data-ttu-id="0cbba-2864">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2864">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-2865">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2865">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2866">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-2866">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2867">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-2867">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2868">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2868">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2869">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2869">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-2870">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2870">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-2871">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2871">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-2872">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-2872">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-2873">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2873">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-2874">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2874">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2875">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2875">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2876">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2876">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2877">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-2877">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-2878">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-2878">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-2879">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2879">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-2880">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2880">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-2881">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2881">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2882">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2882">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2883">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-2883">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-2884">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2884">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-2885">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2885">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2886">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2886">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2887">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2887">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-2888">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-2888">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-2889">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2889">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-2890">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-2890">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-2891">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-2891">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-2892">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2892">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-2893">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2893">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-2894">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2894">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2895">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-2895">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2896">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-2896">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-2897">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2897">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2898">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2898">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2899">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-2899">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-2900">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2900">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-2901">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2901">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-2902">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-2902">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-2903">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-2903">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-2904">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-2904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-2905">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-2906">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-2907">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2907">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-2908">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2908">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a><span data-ttu-id="0cbba-2909">DXGI_FORMAT_R8G8 \_ snorm<sup></sup> -Kenn Wort (51)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2909">DXGI_FORMAT_R8G8\_SNORM<sup>FNS</sup> (51)</span></span>
| <span data-ttu-id="0cbba-2910">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2910">Target</span></span> | <span data-ttu-id="0cbba-2911">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-2911">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-2912">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2912">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-2913">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-2913">16</span></span> |
| <span data-ttu-id="0cbba-2914">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2914">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2916">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2916">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2917">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-2917">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2918">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-2918">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2919">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2919">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2920">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2920">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-2921">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2921">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2923">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2923">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-2924">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-2924">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-2925">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2925">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2927">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2927">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2929">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2929">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2930">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2930">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2931">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-2931">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-2932">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-2932">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-2933">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2933">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2935">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2935">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-2936">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2936">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2937">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2937">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2938">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-2938">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-2939">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2939">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-2940">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2940">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2941">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2941">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2942">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2942">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-2943">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-2943">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-2944">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2944">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-2945">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-2945">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-2946">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-2946">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-2947">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2947">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-2948">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2948">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-2949">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2949">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2950">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-2950">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-2951">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-2951">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-2953">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2953">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2954">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2954">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2955">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-2955">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-2956">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2956">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-2957">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2957">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-2958">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-2958">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-2959">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-2959">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-2960">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-2960">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-2961">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2961">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-2962">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-2962">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-2963">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2963">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-2964">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-2964">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a><span data-ttu-id="0cbba-2965">DXGI_FORMAT_R8G8 \_ Sint<sup></sup> -SPT (52)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2965">DXGI_FORMAT_R8G8\_SINT<sup>FNS</sup> (52)</span></span>
| <span data-ttu-id="0cbba-2966">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2966">Target</span></span> | <span data-ttu-id="0cbba-2967">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-2967">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-2968">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2968">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-2969">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-2969">16</span></span> |
| <span data-ttu-id="0cbba-2970">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2970">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-2971">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2971">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2972">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-2972">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2973">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-2973">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2974">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-2974">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-2975">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2975">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-2976">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2976">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-2977">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-2977">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-2978">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-2978">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-2979">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2979">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-2980">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2980">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2981">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2981">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2982">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-2982">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-2983">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-2983">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-2984">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-2984">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-2985">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2985">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-2986">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-2986">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-2987">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2987">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2988">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-2988">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-2989">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-2989">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-2990">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-2990">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-2991">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2991">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2992">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2992">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-2993">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-2993">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-2994">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-2994">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-2995">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-2995">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-2996">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-2996">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-2997">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-2997">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-2998">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2998">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-2999">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-2999">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-3000">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3000">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3001">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-3001">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3002">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-3002">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-3003">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3003">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3004">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3004">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3005">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-3005">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-3006">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3006">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-3007">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3007">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-3008">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-3008">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-3009">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-3009">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-3010">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-3010">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-3011">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3011">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-3012">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3012">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-3013">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3013">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-3014">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3014">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="0cbba-3015">DXGI_FORMAT_R16 \_ Typen losen<sup>PCs</sup> (53)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3015">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="0cbba-3016">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3016">Target</span></span> | <span data-ttu-id="0cbba-3017">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-3017">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-3018">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3018">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-3019">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-3019">16</span></span> |
| <span data-ttu-id="0cbba-3020">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3020">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-3021">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3021">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3022">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-3022">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3023">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-3023">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3024">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3024">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3025">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3025">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-3026">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3026">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-3027">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3027">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-3028">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-3028">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-3029">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3029">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-3030">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3030">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3031">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3032">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3033">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3033">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-3034">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-3034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-3035">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3035">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-3036">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3036">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-3037">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3037">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3038">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3038">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3039">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-3039">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-3040">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3040">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-3041">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3041">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3042">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3042">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3043">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3043">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-3044">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-3044">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-3045">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3045">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-3046">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-3046">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-3047">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-3047">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-3048">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3048">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-3049">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3049">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-3050">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3050">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3051">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-3051">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3052">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-3052">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-3053">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3053">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3054">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3054">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3055">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-3055">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-3056">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3056">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-3057">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3057">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-3058">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-3058">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-3059">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-3059">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-3060">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-3060">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-3061">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3061">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-3062">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3062">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-3063">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3063">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-3064">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3064">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a><span data-ttu-id="0cbba-3065">DXGI_FORMAT_R16 \_ float-"<sup>f</sup> " (54)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3065">DXGI_FORMAT_R16\_FLOAT<sup>FNS</sup> (54)</span></span>
| <span data-ttu-id="0cbba-3066">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3066">Target</span></span> | <span data-ttu-id="0cbba-3067">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-3067">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-3068">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3068">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-3069">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-3069">16</span></span> |
| <span data-ttu-id="0cbba-3070">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3070">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-3071">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3071">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3072">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-3072">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3073">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-3073">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3074">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3074">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3075">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3075">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-3076">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3076">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-3077">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3077">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-3078">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-3078">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-3079">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3079">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-3080">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3080">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3081">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3081">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3082">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3082">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3083">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3083">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-3084">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-3084">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-3085">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3085">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-3086">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3086">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-3087">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3087">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3088">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3088">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3089">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-3089">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-3090">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3090">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-3091">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3091">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3092">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3092">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3093">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3093">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-3094">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-3094">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-3095">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3095">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-3096">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-3096">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-3097">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-3097">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-3098">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3098">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-3099">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3099">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-3100">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3100">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3101">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-3101">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3102">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-3102">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-3103">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3103">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3104">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3104">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3105">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-3105">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-3106">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3106">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-3107">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3107">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-3108">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-3108">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-3109">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-3109">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-3110">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-3110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-3111">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-3112">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-3113">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3113">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-3114">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3114">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a><span data-ttu-id="0cbba-3115">DXGI_FORMAT_D16 \_ unorm<sup></sup> -Fehler (55)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3115">DXGI_FORMAT_D16\_UNORM<sup>FNS</sup> (55)</span></span>
| <span data-ttu-id="0cbba-3116">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3116">Target</span></span> | <span data-ttu-id="0cbba-3117">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-3117">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-3118">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3118">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-3119">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-3119">16</span></span> |
| <span data-ttu-id="0cbba-3120">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3120">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3122">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3122">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3123">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-3123">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3124">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-3124">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3125">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3125">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3126">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3126">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-3127">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3127">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3129">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3129">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-3130">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-3130">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-3131">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3131">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-3132">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3132">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3133">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3133">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3134">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3134">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3135">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3135">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-3136">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-3136">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-3137">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3137">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-3138">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3138">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-3139">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3139">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3140">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3140">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3141">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-3141">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-3142">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3142">Depth/Stencil Target</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3144">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3144">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3145">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3145">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3146">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3146">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-3147">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-3147">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-3148">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3148">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-3149">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-3149">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-3150">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-3150">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-3151">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3151">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-3152">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3152">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-3153">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3153">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3154">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-3154">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3155">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-3155">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-3156">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3156">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-3158">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3158">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-3160">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-3160">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-3162">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-3163">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3163">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-3164">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-3164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-3165">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-3165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-3166">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-3166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-3167">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-3168">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-3169">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3169">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-3170">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a><span data-ttu-id="0cbba-3171">DXGI_FORMAT_R16 \_ unorm<sup></sup> -Fehler (56)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3171">DXGI_FORMAT_R16\_UNORM<sup>FNS</sup> (56)</span></span>
| <span data-ttu-id="0cbba-3172">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3172">Target</span></span> | <span data-ttu-id="0cbba-3173">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-3173">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-3174">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-3175">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-3175">16</span></span> |
| <span data-ttu-id="0cbba-3176">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3176">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3178">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3178">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3179">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-3179">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3180">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-3180">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3181">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3181">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3182">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3182">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-3183">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3183">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3185">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3185">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3187">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-3187">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3189">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3189">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3191">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3191">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3193">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3193">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3194">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3194">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3195">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3195">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-3196">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-3196">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-3197">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3197">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3199">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3199">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-3200">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3200">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3201">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3201">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3202">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-3202">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-3203">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3203">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-3204">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3204">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3205">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3205">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3206">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3206">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-3207">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-3207">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-3208">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3208">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-3209">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-3209">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-3210">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-3210">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-3211">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3211">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-3212">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3212">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-3213">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3213">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3214">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-3214">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3215">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-3215">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3217">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3217">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3218">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3218">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3219">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-3219">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-3220">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3220">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-3221">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3221">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-3222">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-3222">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-3223">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-3223">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-3224">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-3224">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-3225">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3225">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-3226">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3226">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-3227">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3227">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-3228">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3228">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a><span data-ttu-id="0cbba-3229">DXGI_FORMAT_R16 \_ uint<sup></sup> -Benutzerkonten (57)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3229">DXGI_FORMAT_R16\_UINT<sup>FNS</sup> (57)</span></span>
| <span data-ttu-id="0cbba-3230">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3230">Target</span></span> | <span data-ttu-id="0cbba-3231">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-3231">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-3232">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3232">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-3233">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-3233">16</span></span> |
| <span data-ttu-id="0cbba-3234">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3234">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3236">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3236">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3237">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-3237">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3238">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-3238">Input Assembler Index Buffer</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3240">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3240">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3241">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3241">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-3242">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3242">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-3243">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3243">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-3244">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-3244">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-3245">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3245">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-3246">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3246">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3247">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3247">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3248">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3248">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3249">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3249">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-3250">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-3250">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-3251">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3251">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-3252">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3252">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-3253">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3253">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3254">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3254">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3255">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-3255">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-3256">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3256">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-3257">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3257">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3258">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3258">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3259">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3259">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-3260">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-3260">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-3261">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3261">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-3262">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-3262">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-3263">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-3263">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-3264">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3264">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-3265">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3265">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-3266">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3266">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3267">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-3267">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3268">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-3268">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-3269">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3269">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3270">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3270">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3271">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-3271">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-3272">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3272">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-3273">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3273">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-3274">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-3274">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-3275">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-3275">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-3276">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-3276">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-3277">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3277">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-3278">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3278">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-3279">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3279">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-3280">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3280">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a><span data-ttu-id="0cbba-3281">DXGI_FORMAT_R16 \_ snorm<sup></sup> -Kenn Wort (58)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3281">DXGI_FORMAT_R16\_SNORM<sup>FNS</sup> (58)</span></span>
| <span data-ttu-id="0cbba-3282">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3282">Target</span></span> | <span data-ttu-id="0cbba-3283">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-3283">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-3284">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3284">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-3285">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-3285">16</span></span> |
| <span data-ttu-id="0cbba-3286">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3286">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-3287">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3287">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3288">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-3288">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3289">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-3289">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3290">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3290">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3291">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3291">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-3292">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3292">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-3293">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3293">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-3294">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-3294">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-3295">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3295">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-3296">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3296">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3297">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3297">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3298">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3298">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3299">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3299">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-3300">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-3300">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-3301">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3301">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-3302">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3302">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-3303">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3303">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3304">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3304">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3305">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-3305">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-3306">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3306">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-3307">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3307">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3308">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3308">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3309">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3309">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-3310">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-3310">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-3311">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3311">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-3312">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-3312">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-3313">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-3313">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-3314">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3314">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-3315">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3315">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-3316">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3316">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3317">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-3317">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3318">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-3318">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-3319">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3319">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3320">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3320">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3321">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-3321">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-3322">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3322">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-3323">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3323">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-3324">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-3324">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-3325">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-3325">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-3326">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-3326">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-3327">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3327">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-3328">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3328">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-3329">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3329">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-3330">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3330">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a><span data-ttu-id="0cbba-3331">DXGI_FORMAT_R16 \_ Sint<sup></sup> -SPT (59)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3331">DXGI_FORMAT_R16\_SINT<sup>FNS</sup> (59)</span></span>
| <span data-ttu-id="0cbba-3332">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3332">Target</span></span> | <span data-ttu-id="0cbba-3333">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-3333">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-3334">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3334">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-3335">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-3335">16</span></span> |
| <span data-ttu-id="0cbba-3336">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3336">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-3337">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3337">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3338">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-3338">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3339">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-3339">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3340">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3340">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3341">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3341">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-3342">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3342">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-3343">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3343">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-3344">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-3344">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-3345">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3345">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-3346">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3346">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3347">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3347">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3348">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3348">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3349">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3349">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-3350">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-3350">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-3351">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3351">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-3352">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3352">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-3353">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3353">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3354">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3354">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3355">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-3355">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-3356">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3356">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-3357">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3357">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3358">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3358">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3359">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3359">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-3360">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-3360">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-3361">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3361">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-3362">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-3362">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-3363">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-3363">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-3364">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3364">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-3365">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3365">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-3366">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3366">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3367">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-3367">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3368">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-3368">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-3369">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3369">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3370">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3370">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3371">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-3371">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-3372">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3372">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-3373">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3373">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-3374">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-3374">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-3375">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-3375">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-3376">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-3376">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-3377">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3377">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-3378">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3378">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-3379">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3379">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-3380">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3380">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="0cbba-3381">DXGI_FORMAT_R8 \_ Typen losen<sup>PCs</sup> (60)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3381">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="0cbba-3382">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3382">Target</span></span> | <span data-ttu-id="0cbba-3383">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-3383">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-3384">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3384">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-3385">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-3385">8</span></span> |
| <span data-ttu-id="0cbba-3386">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3386">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-3387">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3387">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3388">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-3388">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3389">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-3389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3390">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3391">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-3392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3392">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-3393">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3393">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-3394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-3394">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-3395">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3395">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-3396">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3396">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3397">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3397">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3398">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3398">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3399">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3399">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-3400">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-3400">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-3401">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3401">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-3402">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3402">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-3403">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3403">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3404">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3404">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3405">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-3405">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-3406">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3406">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-3407">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3407">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3408">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3408">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3409">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3409">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-3410">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-3410">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-3411">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3411">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-3412">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-3412">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-3413">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-3413">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-3414">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3414">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-3415">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3415">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-3416">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3416">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3417">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-3417">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3418">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-3418">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-3419">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3419">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3420">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3420">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3421">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-3421">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-3422">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3422">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-3423">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3423">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-3424">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-3424">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-3425">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-3425">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-3426">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-3426">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-3427">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3427">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-3428">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3428">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-3429">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3429">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-3430">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3430">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a><span data-ttu-id="0cbba-3431">DXGI_FORMAT_R8 \_ unorm<sup></sup> -Fehler (61)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3431">DXGI_FORMAT_R8\_UNORM<sup>FNS</sup> (61)</span></span>
| <span data-ttu-id="0cbba-3432">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3432">Target</span></span> | <span data-ttu-id="0cbba-3433">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-3433">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-3434">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3434">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-3435">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-3435">8</span></span> |
| <span data-ttu-id="0cbba-3436">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3436">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3438">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3438">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3439">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-3439">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3440">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-3440">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3441">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3441">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3442">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3442">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-3443">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3443">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3445">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3445">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3447">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-3447">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3449">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3449">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3451">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3451">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3453">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3454">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3455">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3455">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-3456">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-3456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-3457">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3457">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3459">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3459">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-3460">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3460">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3462">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3462">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3464">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-3464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-3465">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-3466">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3467">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3468">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3468">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-3469">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-3469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-3470">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-3471">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-3471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-3472">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-3472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-3473">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3473">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-3474">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-3475">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3476">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-3476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3477">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-3477">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3479">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3479">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3480">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3480">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3481">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-3481">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-3482">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3482">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-3483">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3483">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-3484">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-3484">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-3485">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-3485">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-3486">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-3486">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-3487">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3487">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-3488">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3488">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-3489">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3489">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3491">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3491">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a><span data-ttu-id="0cbba-3492">DXGI_FORMAT_R8 \_ uint<sup></sup> -Benutzerkonten (62)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3492">DXGI_FORMAT_R8\_UINT<sup>FNS</sup> (62)</span></span>
| <span data-ttu-id="0cbba-3493">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3493">Target</span></span> | <span data-ttu-id="0cbba-3494">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-3494">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-3495">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3495">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-3496">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-3496">8</span></span> |
| <span data-ttu-id="0cbba-3497">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3497">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-3498">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3498">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3499">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-3499">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3500">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-3500">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3501">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3501">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3502">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3502">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-3503">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3503">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-3504">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3504">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-3505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-3505">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-3506">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3506">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-3507">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3507">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3508">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3509">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3510">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3510">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-3511">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-3511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-3512">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3512">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-3513">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3513">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-3514">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3514">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3515">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3515">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3516">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-3516">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-3517">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3517">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-3518">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3518">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3519">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3519">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3520">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3520">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-3521">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-3521">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-3522">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3522">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-3523">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-3523">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-3524">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-3524">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-3525">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3525">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-3526">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3526">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-3527">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3527">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3528">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-3528">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3529">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-3529">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-3530">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3530">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3531">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3531">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3532">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-3532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-3533">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-3534">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3534">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-3535">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-3535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-3536">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-3536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-3537">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-3537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-3538">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-3539">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-3540">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3540">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-3541">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a><span data-ttu-id="0cbba-3542">DXGI_FORMAT_R8 \_ snorm<sup></sup> -Kenn Wort (63)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3542">DXGI_FORMAT_R8\_SNORM<sup>FNS</sup> (63)</span></span>
| <span data-ttu-id="0cbba-3543">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3543">Target</span></span> | <span data-ttu-id="0cbba-3544">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-3544">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-3545">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-3546">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-3546">8</span></span> |
| <span data-ttu-id="0cbba-3547">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3547">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-3548">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3548">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3549">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-3549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3550">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-3550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3551">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3552">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-3553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3553">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-3554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3554">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-3555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-3555">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-3556">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-3557">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3558">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3559">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3560">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3560">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-3561">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-3561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-3562">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3562">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-3563">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-3564">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3564">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3565">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3566">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-3566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-3567">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-3568">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3569">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3570">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3570">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-3571">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-3571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-3572">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-3573">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-3573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-3574">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-3574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-3575">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-3576">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-3577">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3578">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-3578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3579">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-3579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-3580">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3581">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3582">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-3582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-3583">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-3584">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3584">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-3585">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-3585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-3586">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-3586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-3587">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-3587">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-3588">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3588">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-3589">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3589">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-3590">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3590">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-3591">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3591">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a><span data-ttu-id="0cbba-3592">DXGI_FORMAT_R8 \_ Sint<sup></sup> -SPT (64)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3592">DXGI_FORMAT_R8\_SINT<sup>FNS</sup> (64)</span></span>
| <span data-ttu-id="0cbba-3593">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3593">Target</span></span> | <span data-ttu-id="0cbba-3594">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-3594">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-3595">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3595">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-3596">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-3596">8</span></span> |
| <span data-ttu-id="0cbba-3597">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3597">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-3598">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3598">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3599">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-3599">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3600">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-3600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3601">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3602">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-3603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3603">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-3604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3604">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-3605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-3605">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-3606">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-3607">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3608">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3609">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3610">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3610">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-3611">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-3611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-3612">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3612">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-3613">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-3614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3614">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3615">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3616">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-3616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-3617">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-3618">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3619">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3620">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3620">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-3621">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-3621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-3622">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-3623">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-3623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-3624">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-3624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-3625">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-3626">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-3627">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3628">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-3628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3629">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-3629">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-3630">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3630">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3631">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3631">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3632">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-3632">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-3633">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3633">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-3634">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3634">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-3635">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-3635">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-3636">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-3636">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-3637">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-3637">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-3638">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3638">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-3639">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3639">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-3640">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3640">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-3641">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3641">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="0cbba-3642">DXGI_FORMAT_A8 \_ unorm<sup></sup> -Fehler (65)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3642">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="0cbba-3643">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3643">Target</span></span> | <span data-ttu-id="0cbba-3644">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-3644">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-3645">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3645">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-3646">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-3646">8</span></span> |
| <span data-ttu-id="0cbba-3647">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3647">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3649">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3649">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3650">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-3650">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3651">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-3651">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3652">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3652">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3653">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-3654">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3654">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3656">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3656">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3658">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-3658">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3660">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3660">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3662">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3662">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3664">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3665">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3666">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3666">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-3667">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-3667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-3668">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3668">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-3669">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3669">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-3670">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3670">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3672">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3672">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3674">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-3674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-3675">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-3676">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3677">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3678">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3678">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-3679">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-3679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-3680">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-3681">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-3681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-3682">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-3682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-3683">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3683">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-3684">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-3685">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3686">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-3686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3687">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-3687">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3689">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3689">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3690">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3690">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3691">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-3691">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-3692">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3692">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-3693">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3693">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-3694">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-3694">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-3695">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-3695">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-3696">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-3696">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-3697">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3697">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-3698">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3698">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-3699">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3699">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3701">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="0cbba-3702">DXGI_FORMAT_R9G9B9E5 \_ sharede XP-<sup>LNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3702">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="0cbba-3703">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3703">Target</span></span> | <span data-ttu-id="0cbba-3704">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-3704">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-3705">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-3706">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-3706">32</span></span> |
| <span data-ttu-id="0cbba-3707">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3707">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-3708">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3708">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3709">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-3709">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3710">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-3710">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3711">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3711">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3712">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3712">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-3713">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3713">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-3714">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3714">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-3715">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-3715">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-3716">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3716">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-3717">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3717">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3718">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3718">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3719">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3719">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3720">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3720">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-3721">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-3721">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-3722">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3722">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-3723">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3723">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-3724">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3724">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3725">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3725">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3726">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-3726">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-3727">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3727">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-3728">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3728">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3729">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3729">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3730">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3730">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-3731">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-3731">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-3732">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3732">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-3733">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-3733">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-3734">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-3734">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-3735">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3735">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-3736">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3736">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-3737">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3737">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3738">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-3738">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3739">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-3739">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-3740">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3740">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3741">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3741">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3742">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-3742">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-3743">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3743">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-3744">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3744">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-3745">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-3745">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-3746">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-3746">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-3747">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-3747">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-3748">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3748">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-3749">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3749">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-3750">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3750">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-3751">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3751">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="0cbba-3752">DXGI_FORMAT_R8G8 \_ B8G8 \_ unorm<sup></sup> -Fehler (68)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3752">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="0cbba-3753">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3753">Target</span></span> | <span data-ttu-id="0cbba-3754">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-3754">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-3755">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3755">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-3756">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-3756">16</span></span> |
| <span data-ttu-id="0cbba-3757">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3757">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-3758">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3758">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3759">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-3759">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3760">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-3760">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3761">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3761">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3762">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3762">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-3763">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3763">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-3764">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3764">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-3765">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-3765">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-3766">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3766">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-3767">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3767">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3768">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3768">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3769">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3769">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3770">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3770">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-3771">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-3771">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-3772">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3772">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-3773">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3773">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-3774">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3774">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3775">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3775">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3776">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-3776">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-3777">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3777">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-3778">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3778">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3779">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3779">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3780">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3780">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-3781">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-3781">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-3782">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3782">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-3783">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-3783">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-3784">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-3784">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-3785">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3785">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-3786">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3786">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-3787">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3787">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3788">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-3788">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3789">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-3789">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-3790">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3790">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3791">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3791">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3792">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-3792">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-3793">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3793">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-3794">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3794">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-3795">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-3795">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-3796">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-3796">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-3797">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-3797">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-3798">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3798">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-3799">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3799">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-3800">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3800">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-3801">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3801">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="0cbba-3802">DXGI_FORMAT_G8R8 \_ G8B8 \_ unorm<sup></sup> -Fehler (69)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3802">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="0cbba-3803">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3803">Target</span></span> | <span data-ttu-id="0cbba-3804">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-3804">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-3805">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3805">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-3806">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-3806">16</span></span> |
| <span data-ttu-id="0cbba-3807">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3807">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-3808">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3808">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3809">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-3809">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3810">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-3810">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3811">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3811">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3812">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3812">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-3813">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3813">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-3814">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3814">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-3815">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-3815">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-3816">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3816">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-3817">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3817">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3818">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3818">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3819">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3819">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3820">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3820">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-3821">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-3821">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-3822">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3822">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-3823">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3823">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-3824">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3824">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3825">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3825">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3826">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-3826">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-3827">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3827">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-3828">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3828">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3829">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3829">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3830">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3830">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-3831">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-3831">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-3832">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3832">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-3833">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-3833">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-3834">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-3834">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-3835">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3835">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-3836">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3836">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-3837">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3837">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3838">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-3838">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3839">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-3839">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-3840">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3840">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3841">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3841">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3842">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-3842">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-3843">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3843">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-3844">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3844">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-3845">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-3845">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-3846">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-3846">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-3847">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-3847">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-3848">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3848">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-3849">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3849">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-3850">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3850">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-3851">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3851">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="0cbba-3852">DXGI_FORMAT_BC1 \_ typloses<sup>PCC</sup> (70)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3852">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="0cbba-3853">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3853">Target</span></span> | <span data-ttu-id="0cbba-3854">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-3854">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-3855">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3855">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-3856">4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3856">4</span></span> |
| <span data-ttu-id="0cbba-3857">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3857">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-3858">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3858">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3859">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-3859">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3860">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-3860">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3861">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3861">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3862">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3862">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-3863">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3863">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-3864">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3864">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-3865">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-3865">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-3866">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3866">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-3867">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3867">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3868">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3868">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3869">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3869">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3870">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3870">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-3871">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-3871">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-3872">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3872">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-3873">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3873">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-3874">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3874">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3875">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3875">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3876">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-3876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-3877">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-3878">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3879">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3880">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3880">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-3881">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-3881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-3882">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-3883">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-3883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-3884">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-3884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-3885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3885">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-3886">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-3887">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3888">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-3888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3889">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-3889">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-3890">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3890">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3891">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3891">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3892">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-3892">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-3893">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3893">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-3894">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3894">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-3895">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-3895">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-3896">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-3896">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-3897">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-3897">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-3898">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3898">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-3899">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3899">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-3900">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3900">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-3901">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3901">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a><span data-ttu-id="0cbba-3902">DXGI_FORMAT_BC1 \_ unorm<sup></sup> -Fehler (71)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3902">DXGI_FORMAT_BC1\_UNORM<sup>FNC</sup> (71)</span></span>
| <span data-ttu-id="0cbba-3903">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3903">Target</span></span> | <span data-ttu-id="0cbba-3904">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-3904">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-3905">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3905">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-3906">4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3906">4</span></span> |
| <span data-ttu-id="0cbba-3907">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3907">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3909">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3909">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3910">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-3910">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3911">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-3911">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3912">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3912">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3913">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3913">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-3914">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3914">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3916">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3916">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-3917">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-3917">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3919">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3919">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3921">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3921">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3923">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3923">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3924">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3924">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3925">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3925">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-3926">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-3926">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-3927">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3927">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3929">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3929">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-3930">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3930">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3931">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3931">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3932">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-3932">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-3933">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3933">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-3934">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3934">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3935">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3935">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3936">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3936">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-3937">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-3937">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-3938">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3938">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-3939">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-3939">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-3940">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-3940">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-3941">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3941">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-3942">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3942">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-3943">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3943">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3944">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-3944">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-3945">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-3945">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3947">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3947">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3948">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3948">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3949">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-3949">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-3950">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3950">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-3951">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3951">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-3952">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-3952">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-3953">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-3953">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-3954">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-3954">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-3955">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3955">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-3956">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-3956">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-3957">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3957">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3959">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-3959">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a><span data-ttu-id="0cbba-3960">DXGI_FORMAT_BC1 \_ unorm \_ sRGB<sup></sup> -Fehler (72)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3960">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FNC</sup> (72)</span></span>
| <span data-ttu-id="0cbba-3961">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3961">Target</span></span> | <span data-ttu-id="0cbba-3962">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-3962">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-3963">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3963">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-3964">4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3964">4</span></span> |
| <span data-ttu-id="0cbba-3965">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3965">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3967">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3967">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3968">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-3968">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3969">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-3969">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3970">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-3970">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-3971">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3971">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-3972">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3972">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3974">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-3974">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-3975">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-3975">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3977">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3977">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3979">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3979">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3981">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3981">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3982">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-3982">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-3983">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-3983">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-3984">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-3984">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-3985">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3985">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-3987">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-3987">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-3988">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3988">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3989">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-3989">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-3990">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-3990">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-3991">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-3991">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-3992">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3992">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3993">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3993">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-3994">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-3994">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-3995">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-3995">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-3996">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-3996">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-3997">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-3997">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-3998">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-3998">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-3999">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-3999">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-4000">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4000">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-4001">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4001">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4002">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-4002">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4003">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-4003">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4005">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4005">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4006">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4006">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4007">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-4007">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-4008">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4008">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-4009">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4009">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-4010">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-4010">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-4011">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-4011">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-4012">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-4012">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-4013">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4013">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-4014">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4014">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-4015">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4015">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4017">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4017">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="0cbba-4018">DXGI_FORMAT_BC2 \_ typloses<sup>PCC</sup> (73)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4018">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="0cbba-4019">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4019">Target</span></span> | <span data-ttu-id="0cbba-4020">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-4020">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-4021">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4021">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-4022">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-4022">8</span></span> |
| <span data-ttu-id="0cbba-4023">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4023">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-4024">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4024">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4025">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-4025">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4026">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-4026">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4027">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4027">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4028">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4028">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-4029">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4029">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-4030">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4030">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-4031">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-4031">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-4032">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4032">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-4033">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4033">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4034">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4034">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4035">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4035">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4036">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4036">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-4037">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-4037">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-4038">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4038">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-4039">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4039">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-4040">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4040">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4041">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4041">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4042">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-4042">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-4043">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4043">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-4044">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4044">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4045">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4045">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4046">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4046">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-4047">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-4047">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-4048">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4048">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-4049">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-4049">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-4050">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-4050">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-4051">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4051">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-4052">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4052">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-4053">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4053">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4054">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-4054">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4055">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-4055">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-4056">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4056">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4057">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4057">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4058">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-4058">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-4059">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4059">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-4060">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4060">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-4061">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-4061">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-4062">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-4062">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-4063">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-4063">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-4064">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4064">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-4065">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4065">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-4066">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4066">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-4067">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4067">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a><span data-ttu-id="0cbba-4068">DXGI_FORMAT_BC2 \_ unorm<sup></sup> -Fehler (74)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4068">DXGI_FORMAT_BC2\_UNORM<sup>FNC</sup> (74)</span></span>
| <span data-ttu-id="0cbba-4069">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4069">Target</span></span> | <span data-ttu-id="0cbba-4070">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-4070">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-4071">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4071">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-4072">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-4072">8</span></span> |
| <span data-ttu-id="0cbba-4073">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4073">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4075">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4075">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4076">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-4076">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4077">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-4077">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4078">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4078">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4079">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4079">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-4080">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4080">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4082">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4082">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-4083">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-4083">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4085">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4085">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4087">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4087">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4089">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4089">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4090">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4090">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4091">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4091">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-4092">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-4092">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-4093">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4093">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4095">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4095">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-4096">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4096">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4097">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4097">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4098">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-4098">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-4099">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4099">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-4100">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4100">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4101">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4101">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4102">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4102">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-4103">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-4103">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-4104">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4104">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-4105">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-4105">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-4106">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-4106">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-4107">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4107">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-4108">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4108">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-4109">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4109">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4110">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-4110">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4111">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-4111">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4113">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4113">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4114">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4114">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4115">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-4115">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-4116">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4116">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-4117">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4117">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-4118">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-4118">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-4119">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-4119">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-4120">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-4120">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-4121">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4121">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-4122">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4122">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-4123">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4123">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4125">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4125">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a><span data-ttu-id="0cbba-4126">DXGI_FORMAT_BC2 \_ unorm \_ sRGB<sup></sup> -Fehler (75)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4126">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FNC</sup> (75)</span></span>
| <span data-ttu-id="0cbba-4127">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4127">Target</span></span> | <span data-ttu-id="0cbba-4128">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-4128">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-4129">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4129">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-4130">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-4130">8</span></span> |
| <span data-ttu-id="0cbba-4131">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4131">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4133">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4133">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4134">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-4134">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4135">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-4135">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4136">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4136">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4137">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4137">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-4138">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4138">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4140">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4140">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-4141">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-4141">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4143">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4143">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4145">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4145">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4147">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4147">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4148">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4148">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4149">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4149">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-4150">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-4150">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-4151">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4151">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4153">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4153">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-4154">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4154">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4155">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4155">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4156">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-4156">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-4157">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4157">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-4158">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4158">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4159">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4159">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4160">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4160">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-4161">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-4161">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-4162">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4162">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-4163">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-4163">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-4164">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-4164">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-4165">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4165">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-4166">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4166">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-4167">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4167">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4168">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-4168">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4169">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-4169">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4171">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4171">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4172">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4172">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4173">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-4173">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-4174">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4174">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-4175">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4175">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-4176">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-4176">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-4177">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-4177">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-4178">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-4178">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-4179">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4179">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-4180">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4180">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-4181">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4181">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4183">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4183">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="0cbba-4184">DXGI_FORMAT_BC3 \_ typloses<sup>PCC</sup> (76)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4184">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="0cbba-4185">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4185">Target</span></span> | <span data-ttu-id="0cbba-4186">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-4186">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-4187">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4187">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-4188">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-4188">8</span></span> |
| <span data-ttu-id="0cbba-4189">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4189">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-4190">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4190">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4191">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-4191">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4192">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-4192">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4193">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4193">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4194">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4194">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-4195">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4195">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-4196">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4196">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-4197">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-4197">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-4198">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4198">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-4199">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4199">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4200">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4200">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4201">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4201">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4202">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4202">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-4203">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-4203">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-4204">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4204">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-4205">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4205">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-4206">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4206">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4207">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4207">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4208">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-4208">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-4209">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4209">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-4210">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4210">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4211">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4211">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4212">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4212">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-4213">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-4213">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-4214">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4214">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-4215">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-4215">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-4216">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-4216">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-4217">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4217">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-4218">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4218">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-4219">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4219">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4220">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-4220">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4221">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-4221">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-4222">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4222">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4223">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4223">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4224">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-4224">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-4225">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4225">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-4226">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4226">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-4227">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-4227">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-4228">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-4228">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-4229">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-4229">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-4230">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4230">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-4231">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4231">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-4232">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4232">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-4233">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4233">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a><span data-ttu-id="0cbba-4234">DXGI_FORMAT_BC3 \_ unorm<sup></sup> -Fehler (77)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4234">DXGI_FORMAT_BC3\_UNORM<sup>FNC</sup> (77)</span></span>
| <span data-ttu-id="0cbba-4235">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4235">Target</span></span> | <span data-ttu-id="0cbba-4236">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-4236">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-4237">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4237">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-4238">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-4238">8</span></span> |
| <span data-ttu-id="0cbba-4239">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4239">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4241">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4241">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4242">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-4242">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4243">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-4243">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4244">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4244">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4245">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4245">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-4246">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4246">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4248">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4248">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-4249">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-4249">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4251">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4251">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4253">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4253">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4255">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4255">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4256">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4256">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4257">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4257">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-4258">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-4258">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-4259">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4259">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4261">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4261">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-4262">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4262">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4263">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4263">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4264">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-4264">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-4265">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4265">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-4266">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4266">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4267">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4267">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4268">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4268">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-4269">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-4269">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-4270">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4270">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-4271">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-4271">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-4272">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-4272">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-4273">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4273">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-4274">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4274">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-4275">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4275">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4276">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-4276">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4277">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-4277">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4279">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4279">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4280">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4280">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4281">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-4281">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-4282">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4282">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-4283">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4283">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-4284">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-4284">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-4285">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-4285">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-4286">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-4286">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-4287">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4287">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-4288">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4288">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-4289">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4289">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4291">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4291">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a><span data-ttu-id="0cbba-4292">DXGI_FORMAT_BC3 \_ unorm \_ sRGB<sup></sup> -Fehler (78)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4292">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FNC</sup> (78)</span></span>
| <span data-ttu-id="0cbba-4293">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4293">Target</span></span> | <span data-ttu-id="0cbba-4294">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-4294">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-4295">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4295">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-4296">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-4296">8</span></span> |
| <span data-ttu-id="0cbba-4297">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4297">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4299">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4299">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4300">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-4300">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4301">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-4301">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4302">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4302">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4303">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4303">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-4304">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4304">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4306">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4306">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-4307">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-4307">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4309">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4309">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4311">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4311">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4313">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4313">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4314">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4314">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4315">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4315">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-4316">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-4316">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-4317">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4317">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4319">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4319">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-4320">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4320">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4321">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4321">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4322">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-4322">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-4323">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4323">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-4324">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4324">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4325">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4325">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4326">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4326">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-4327">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-4327">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-4328">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4328">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-4329">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-4329">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-4330">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-4330">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-4331">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4331">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-4332">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4332">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-4333">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4333">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4334">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-4334">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4335">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-4335">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4337">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4337">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4338">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4338">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4339">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-4339">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-4340">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4340">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-4341">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4341">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-4342">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-4342">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-4343">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-4343">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-4344">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-4344">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-4345">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4345">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-4346">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4346">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-4347">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4347">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4349">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4349">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="0cbba-4350">DXGI_FORMAT_BC4 \_ typloses<sup>PCC</sup> (79)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4350">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="0cbba-4351">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4351">Target</span></span> | <span data-ttu-id="0cbba-4352">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-4352">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-4353">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4353">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-4354">4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4354">4</span></span> |
| <span data-ttu-id="0cbba-4355">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4355">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-4356">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4356">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4357">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-4357">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4358">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-4358">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4359">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4359">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4360">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4360">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-4361">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4361">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-4362">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4362">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-4363">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-4363">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-4364">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4364">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-4365">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4365">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4366">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4366">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4367">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4367">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4368">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4368">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-4369">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-4369">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-4370">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4370">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-4371">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4371">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-4372">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4372">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4373">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4373">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4374">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-4374">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-4375">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4375">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-4376">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4376">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4377">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4377">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4378">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4378">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-4379">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-4379">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-4380">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4380">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-4381">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-4381">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-4382">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-4382">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-4383">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4383">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-4384">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4384">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-4385">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4385">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4386">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-4386">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4387">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-4387">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-4388">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4388">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4389">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4389">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4390">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-4390">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-4391">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4391">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-4392">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4392">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-4393">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-4393">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-4394">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-4394">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-4395">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-4395">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-4396">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4396">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-4397">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4397">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-4398">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4398">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-4399">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4399">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a><span data-ttu-id="0cbba-4400">DXGI_FORMAT_BC4 \_ unorm<sup></sup> -Fehler (80)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4400">DXGI_FORMAT_BC4\_UNORM<sup>FNC</sup> (80)</span></span>
| <span data-ttu-id="0cbba-4401">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4401">Target</span></span> | <span data-ttu-id="0cbba-4402">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-4402">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-4403">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4403">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-4404">4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4404">4</span></span> |
| <span data-ttu-id="0cbba-4405">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4405">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-4406">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4406">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4407">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-4407">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4408">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-4408">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4409">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4409">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4410">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4410">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-4411">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4411">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-4412">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4412">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-4413">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-4413">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-4414">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4414">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-4415">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4415">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4416">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4416">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4417">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4417">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4418">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4418">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-4419">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-4419">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-4420">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4420">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-4421">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4421">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-4422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4422">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4423">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4423">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4424">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-4424">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-4425">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4425">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-4426">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4426">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4427">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4427">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4428">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4428">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-4429">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-4429">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-4430">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4430">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-4431">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-4431">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-4432">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-4432">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-4433">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4433">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-4434">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4434">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-4435">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4435">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4436">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-4436">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4437">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-4437">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-4438">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4438">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4439">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4439">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4440">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-4440">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-4441">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4441">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-4442">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4442">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-4443">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-4443">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-4444">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-4444">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-4445">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-4445">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-4446">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4446">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-4447">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4447">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-4448">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4448">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-4449">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4449">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a><span data-ttu-id="0cbba-4450">DXGI_FORMAT_BC4 \_ snorm<sup></sup> -snorm (81)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4450">DXGI_FORMAT_BC4\_SNORM<sup>FNC</sup> (81)</span></span>
| <span data-ttu-id="0cbba-4451">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4451">Target</span></span> | <span data-ttu-id="0cbba-4452">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-4452">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-4453">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4453">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-4454">4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4454">4</span></span> |
| <span data-ttu-id="0cbba-4455">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4455">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-4456">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4456">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4457">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-4457">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4458">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-4458">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4459">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4459">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4460">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4460">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-4461">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4461">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-4462">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4462">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-4463">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-4463">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-4464">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4464">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-4465">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4465">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4466">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4466">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4467">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4467">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4468">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4468">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-4469">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-4469">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-4470">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4470">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-4471">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4471">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-4472">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4472">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4473">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4473">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4474">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-4474">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-4475">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4475">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-4476">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4476">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4477">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4477">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4478">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4478">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-4479">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-4479">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-4480">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4480">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-4481">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-4481">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-4482">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-4482">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-4483">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4483">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-4484">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4484">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-4485">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4485">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4486">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-4486">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4487">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-4487">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-4488">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4488">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4489">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4489">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4490">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-4490">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-4491">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4491">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-4492">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4492">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-4493">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-4493">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-4494">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-4494">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-4495">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-4495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-4496">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-4497">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-4498">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4498">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-4499">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="0cbba-4500">DXGI_FORMAT_BC5 \_ typloses<sup>PCC</sup> (82)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4500">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="0cbba-4501">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4501">Target</span></span> | <span data-ttu-id="0cbba-4502">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-4502">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-4503">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-4504">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-4504">8</span></span> |
| <span data-ttu-id="0cbba-4505">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4505">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-4506">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4506">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4507">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-4507">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4508">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-4508">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4509">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4509">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4510">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4510">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-4511">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4511">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-4512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4512">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-4513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-4513">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-4514">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4514">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-4515">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4515">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4516">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4516">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4517">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4517">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4518">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4518">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-4519">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-4519">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-4520">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4520">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-4521">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4521">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-4522">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4522">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4523">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4523">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4524">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-4524">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-4525">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4525">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-4526">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4526">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4527">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4527">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4528">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4528">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-4529">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-4529">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-4530">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4530">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-4531">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-4531">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-4532">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-4532">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-4533">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4533">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-4534">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4534">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-4535">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4535">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4536">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-4536">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4537">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-4537">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-4538">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4538">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4539">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4539">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4540">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-4540">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-4541">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4541">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-4542">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4542">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-4543">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-4543">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-4544">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-4544">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-4545">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-4545">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-4546">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4546">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-4547">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4547">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-4548">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4548">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-4549">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4549">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a><span data-ttu-id="0cbba-4550">DXGI_FORMAT_BC5 \_ unorm<sup></sup> -Fehler (83)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4550">DXGI_FORMAT_BC5\_UNORM<sup>FNC</sup> (83)</span></span>
| <span data-ttu-id="0cbba-4551">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4551">Target</span></span> | <span data-ttu-id="0cbba-4552">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-4552">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-4553">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4553">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-4554">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-4554">8</span></span> |
| <span data-ttu-id="0cbba-4555">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4555">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-4556">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4556">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4557">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-4557">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4558">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-4558">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4559">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4559">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4560">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4560">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-4561">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4561">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-4562">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4562">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-4563">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-4563">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-4564">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4564">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-4565">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4565">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4566">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4566">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4567">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4567">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4568">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4568">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-4569">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-4569">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-4570">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4570">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-4571">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4571">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-4572">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4572">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4573">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4573">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4574">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-4574">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-4575">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4575">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-4576">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4576">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4577">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4577">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4578">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4578">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-4579">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-4579">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-4580">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4580">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-4581">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-4581">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-4582">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-4582">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-4583">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4583">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-4584">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4584">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-4585">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4585">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4586">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-4586">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4587">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-4587">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-4588">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4588">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4589">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4589">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4590">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-4590">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-4591">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4591">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-4592">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4592">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-4593">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-4593">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-4594">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-4594">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-4595">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-4595">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-4596">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4596">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-4597">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4597">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-4598">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4598">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-4599">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4599">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a><span data-ttu-id="0cbba-4600">DXGI_FORMAT_BC5 \_ snorm<sup></sup> -snorm (84)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4600">DXGI_FORMAT_BC5\_SNORM<sup>FNC</sup> (84)</span></span>
| <span data-ttu-id="0cbba-4601">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4601">Target</span></span> | <span data-ttu-id="0cbba-4602">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-4602">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-4603">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4603">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-4604">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-4604">8</span></span> |
| <span data-ttu-id="0cbba-4605">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4605">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-4606">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4606">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4607">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-4607">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4608">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-4608">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4609">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4609">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4610">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4610">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-4611">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4611">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-4612">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4612">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-4613">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-4613">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-4614">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4614">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-4615">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4615">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4616">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4616">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4617">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4617">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4618">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4618">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-4619">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-4619">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-4620">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4620">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-4621">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4621">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-4622">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4622">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4623">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4623">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4624">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-4624">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-4625">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4625">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-4626">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4626">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4627">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4627">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4628">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4628">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-4629">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-4629">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-4630">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4630">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-4631">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-4631">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-4632">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-4632">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-4633">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4633">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-4634">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4634">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-4635">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4635">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4636">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-4636">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4637">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-4637">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-4638">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4638">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4639">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4639">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4640">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-4640">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-4641">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4641">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-4642">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4642">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-4643">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-4643">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-4644">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-4644">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-4645">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-4645">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-4646">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4646">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-4647">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4647">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-4648">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4648">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-4649">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4649">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="0cbba-4650">DXGI_FORMAT_B5G6R5 \_ unorm<sup></sup> -Fehler (85)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4650">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="0cbba-4651">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4651">Target</span></span> | <span data-ttu-id="0cbba-4652">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-4652">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-4653">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4653">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-4654">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-4654">16</span></span> |
| <span data-ttu-id="0cbba-4655">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4655">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4657">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4657">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4658">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-4658">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4659">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-4659">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4660">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4660">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4661">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4661">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-4662">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4662">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4664">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4664">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-4665">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-4665">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4667">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4667">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4669">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4669">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4671">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4671">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4672">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4672">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4673">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4673">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-4674">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-4674">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-4675">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4675">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4677">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4677">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4679">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4679">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4681">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4681">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4683">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-4683">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-4684">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4684">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-4685">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4685">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4686">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4686">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4687">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4687">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-4688">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-4688">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-4689">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4689">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-4690">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-4690">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-4691">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-4691">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-4692">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4692">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-4693">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4693">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-4694">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4694">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4695">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-4695">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4696">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-4696">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4698">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4698">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-4700">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4700">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-4702">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-4702">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-4704">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4704">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4706">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4706">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-4707">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-4707">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-4708">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-4708">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-4709">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-4709">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-4710">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4710">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-4711">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4711">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-4712">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4712">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-4713">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4713">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="0cbba-4714">DXGI_FORMAT_B5G5R5A1 \_ unorm<sup></sup> -Fehler (86)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4714">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="0cbba-4715">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4715">Target</span></span> | <span data-ttu-id="0cbba-4716">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-4716">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-4717">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4717">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-4718">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-4718">16</span></span> |
| <span data-ttu-id="0cbba-4719">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4719">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4721">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4721">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4722">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-4722">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4723">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-4723">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4724">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4724">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4725">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4725">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-4726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4726">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4728">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-4729">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-4729">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4731">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4731">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4733">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4733">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4735">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4735">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4736">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4736">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4737">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4737">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-4738">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-4738">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-4739">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4739">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4741">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4741">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-4742">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4742">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4743">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4743">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4744">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-4744">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-4745">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4745">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-4746">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4746">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4747">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4747">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4748">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4748">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-4749">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-4749">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-4750">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4750">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-4751">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-4751">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-4752">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-4752">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-4753">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4753">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-4754">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4754">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-4755">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4755">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4756">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-4756">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4757">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-4757">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4759">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4759">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4760">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4760">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4761">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-4761">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-4762">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4762">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-4763">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4763">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-4764">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-4764">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-4765">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-4765">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-4766">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-4766">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-4767">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4767">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-4768">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4768">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-4769">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4769">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-4770">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4770">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="0cbba-4771">DXGI_FORMAT_B8G8R8A8 \_ Typen losen<sup>PCs</sup> (90)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4771">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="0cbba-4772">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4772">Target</span></span> | <span data-ttu-id="0cbba-4773">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-4773">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-4774">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4774">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-4775">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-4775">32</span></span> |
| <span data-ttu-id="0cbba-4776">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4776">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-4777">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4777">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4778">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-4778">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4779">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-4779">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4780">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4780">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4781">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4781">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-4782">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4782">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-4783">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4783">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-4784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-4784">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-4785">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4785">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-4786">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4786">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4787">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4787">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4788">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4788">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4789">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4789">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-4790">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-4790">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-4791">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4791">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-4792">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4792">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-4793">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4793">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4794">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4794">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4795">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-4795">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-4796">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4796">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-4797">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4797">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4798">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4798">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4799">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4799">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-4800">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-4800">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-4801">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4801">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-4802">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-4802">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-4803">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-4803">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-4804">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4804">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-4805">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4805">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-4806">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4806">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4807">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-4807">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4808">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-4808">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-4809">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4809">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4810">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4810">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4811">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-4811">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-4812">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4812">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-4813">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4813">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-4814">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-4814">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-4815">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-4815">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-4816">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-4816">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-4817">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4817">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-4818">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4818">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-4819">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4819">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-4820">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4820">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a><span data-ttu-id="0cbba-4821">DXGI_FORMAT_B8G8R8A8 \_ unorm<sup></sup> -Fehler (87)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4821">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FNS</sup> (87)</span></span>
| <span data-ttu-id="0cbba-4822">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4822">Target</span></span> | <span data-ttu-id="0cbba-4823">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-4823">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-4824">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4824">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-4825">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-4825">32</span></span> |
| <span data-ttu-id="0cbba-4826">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4826">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4828">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4828">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4829">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-4829">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4830">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-4830">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4831">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4831">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4832">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4832">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-4833">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4833">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4835">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4835">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4837">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-4837">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4839">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4839">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4841">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4841">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4843">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4843">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4844">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4844">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4845">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4845">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-4846">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-4846">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-4847">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4847">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4849">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4849">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4851">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4851">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4853">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4853">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4855">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-4855">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-4856">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4856">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-4857">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4857">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4858">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4858">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4859">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4859">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-4860">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-4860">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-4861">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4861">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-4862">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-4862">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-4863">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-4863">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-4864">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4864">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-4865">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4865">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-4866">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4866">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4867">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-4867">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4868">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-4868">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4870">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4870">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-4872">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4872">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-4874">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-4874">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-4876">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4876">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4878">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4878">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-4879">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-4879">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4881">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-4881">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-4882">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-4882">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-4883">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4883">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-4885">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4885">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4887">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4887">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4889">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4889">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a><span data-ttu-id="0cbba-4890">DXGI_FORMAT_B8G8R8A8 \_ unorm \_ sRGB<sup></sup> -Fehler (91)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4890">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FNS</sup> (91)</span></span>
| <span data-ttu-id="0cbba-4891">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4891">Target</span></span> | <span data-ttu-id="0cbba-4892">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-4892">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-4893">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4893">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-4894">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-4894">32</span></span> |
| <span data-ttu-id="0cbba-4895">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4895">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4897">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4897">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4898">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-4898">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4899">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-4899">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4900">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4900">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4901">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4901">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-4902">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4902">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4904">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4904">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4906">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-4906">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4908">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4908">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4910">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4910">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4912">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4912">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4913">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4913">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4914">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4914">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-4915">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-4915">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-4916">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4916">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4918">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4918">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4920">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4920">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4922">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4922">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4924">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-4924">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-4925">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4925">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-4926">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4926">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4927">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4927">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4928">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4928">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-4929">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-4929">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-4930">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4930">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-4931">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-4931">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-4932">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-4932">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-4933">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4933">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-4934">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4934">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-4935">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4935">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4936">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-4936">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4937">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-4937">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4939">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4939">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-4941">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4941">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-4943">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-4943">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-4945">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4945">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4947">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4947">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-4948">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-4948">Display Scan-Out</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4950">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-4950">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-4951">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-4951">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-4952">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4952">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-4954">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-4954">Video Processor Output</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4956">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4956">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-4958">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-4958">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="0cbba-4959">DXGI_FORMAT_B8G8R8X8 \_ Typen losen<sup>PCs</sup> (92)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4959">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="0cbba-4960">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4960">Target</span></span> | <span data-ttu-id="0cbba-4961">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-4961">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-4962">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4962">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-4963">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-4963">32</span></span> |
| <span data-ttu-id="0cbba-4964">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4964">Format Support</span></span> | \- |
| <span data-ttu-id="0cbba-4965">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4965">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4966">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-4966">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4967">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-4967">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4968">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-4968">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-4969">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4969">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-4970">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4970">Texture2D</span></span> | \- |
| <span data-ttu-id="0cbba-4971">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-4971">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-4972">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-4972">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-4973">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4973">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-4974">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4974">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4975">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4975">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4976">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4976">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-4977">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-4977">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-4978">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-4978">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-4979">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4979">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-4980">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-4980">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-4981">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4981">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4982">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4982">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4983">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-4983">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-4984">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-4984">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-4985">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4985">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4986">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4986">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-4987">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-4987">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-4988">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-4988">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-4989">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-4989">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-4990">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-4990">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-4991">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-4991">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-4992">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4992">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-4993">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-4993">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-4994">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-4994">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4995">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-4995">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-4996">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-4996">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-4997">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4997">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4998">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-4998">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-4999">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-4999">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-5000">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5000">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-5001">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5001">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-5002">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-5002">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-5003">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-5003">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-5004">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-5004">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-5005">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5005">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-5006">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5006">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-5007">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5007">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-5008">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5008">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a><span data-ttu-id="0cbba-5009">DXGI_FORMAT_B8G8R8X8 \_ unorm<sup></sup> -Fehler (88)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5009">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FNS</sup> (88)</span></span>
| <span data-ttu-id="0cbba-5010">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5010">Target</span></span> | <span data-ttu-id="0cbba-5011">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-5011">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-5012">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5012">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-5013">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-5013">32</span></span> |
| <span data-ttu-id="0cbba-5014">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5014">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5016">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5016">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5017">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-5017">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5018">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-5018">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5019">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5019">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5020">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5020">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-5021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5021">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5023">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-5025">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5027">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5027">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5029">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5029">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5031">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5032">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5033">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-5033">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-5034">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-5034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-5035">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5035">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5037">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5037">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5039">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5039">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5041">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5041">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5043">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-5043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-5044">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-5045">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5046">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5047">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5047">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-5048">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-5048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-5049">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-5050">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-5050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-5051">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-5051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-5052">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5052">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-5053">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-5054">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5055">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-5055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5056">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-5056">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5058">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5058">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5060">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5060">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5062">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-5062">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5064">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5064">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5066">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5066">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-5067">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-5067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-5068">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-5068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-5069">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-5069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-5070">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5070">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5072">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5072">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5074">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5074">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5076">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5076">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a><span data-ttu-id="0cbba-5077">DXGI_FORMAT_B8G8R8X8 \_ unorm \_ sRGB<sup></sup> -Fehler (93)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5077">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FNS</sup> (93)</span></span>
| <span data-ttu-id="0cbba-5078">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5078">Target</span></span> | <span data-ttu-id="0cbba-5079">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-5079">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-5080">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5080">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-5081">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-5081">32</span></span> |
| <span data-ttu-id="0cbba-5082">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5082">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5084">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5084">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5085">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-5085">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5086">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-5086">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5087">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5087">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5088">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5088">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-5089">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5089">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5091">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5091">Texture3D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5093">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-5093">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5095">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5095">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5097">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5097">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5099">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5099">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5100">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5100">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5101">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-5101">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-5102">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-5102">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-5103">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5103">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5105">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5105">Mipmap Auto-Generation</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5107">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5107">RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5109">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5109">Blendable RenderTarget</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5111">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-5111">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-5112">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5112">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-5113">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5113">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5114">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5114">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5115">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5115">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-5116">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-5116">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-5117">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5117">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-5118">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-5118">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-5119">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-5119">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-5120">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5120">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-5121">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5121">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-5122">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5122">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5123">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-5123">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5124">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-5124">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5126">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5126">4x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5128">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5128">8x Multisample RenderTarget</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5130">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-5130">Other Multisample Count RT</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5132">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5132">Multisample Resolve</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5134">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5134">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-5135">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-5135">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-5136">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-5136">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-5137">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-5137">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-5138">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5138">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-5139">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5139">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-5140">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5140">Shared Resource</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5142">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5142">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="0cbba-5143">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5143">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="0cbba-5144">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5144">Target</span></span> | <span data-ttu-id="0cbba-5145">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-5145">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-5146">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5146">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-5147">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-5147">32</span></span> |
| <span data-ttu-id="0cbba-5148">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5148">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5150">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5150">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5151">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-5151">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5152">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-5152">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5153">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5153">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5154">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5154">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-5155">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5155">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5157">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5157">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-5158">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-5158">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-5159">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5159">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-5160">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5160">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5161">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5161">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5162">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5162">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5163">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-5163">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-5164">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-5164">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-5165">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5165">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-5166">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5166">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-5167">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5167">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5168">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5168">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5169">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-5169">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-5170">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5170">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-5171">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5171">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5172">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5172">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5173">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5173">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-5174">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-5174">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-5175">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5175">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-5176">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-5176">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-5177">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-5177">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-5178">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5178">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-5179">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5179">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-5180">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5180">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5181">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-5181">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5182">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-5182">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5184">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5184">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5185">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5185">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5186">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-5186">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-5187">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5187">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-5188">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5188">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-5189">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-5189">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-5190">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-5190">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-5191">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-5191">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5193">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5193">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5195">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5195">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5197">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5197">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-5198">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5198">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="0cbba-5199">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5199">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="0cbba-5200">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5200">Target</span></span> | <span data-ttu-id="0cbba-5201">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-5201">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-5202">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5202">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-5203">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-5203">32</span></span> |
| <span data-ttu-id="0cbba-5204">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5204">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5206">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5206">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5207">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-5207">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5208">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-5208">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5209">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5209">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5210">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5210">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-5211">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5211">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5213">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5213">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-5214">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-5214">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-5215">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5215">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-5216">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5216">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5217">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5217">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5218">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5218">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5219">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-5219">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-5220">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-5220">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-5221">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5221">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-5222">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5222">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-5223">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5223">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5224">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5224">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5225">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-5225">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-5226">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5226">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-5227">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5227">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5228">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5228">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5229">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5229">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-5230">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-5230">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-5231">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5231">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-5232">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-5232">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-5233">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-5233">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-5234">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5234">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-5235">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5235">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-5236">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5236">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5237">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-5237">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5238">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-5238">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5240">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5240">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5241">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5241">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5242">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-5242">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-5243">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5243">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-5244">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5244">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-5245">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-5245">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-5246">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-5246">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-5247">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-5247">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5249">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5249">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5251">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5251">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5253">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5253">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-5254">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5254">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="0cbba-5255">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5255">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="0cbba-5256">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5256">Target</span></span> | <span data-ttu-id="0cbba-5257">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-5257">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-5258">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5258">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-5259">64</span><span class="sxs-lookup"><span data-stu-id="0cbba-5259">64</span></span> |
| <span data-ttu-id="0cbba-5260">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5260">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5262">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5262">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5263">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-5263">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5264">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-5264">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5265">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5265">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5266">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5266">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-5267">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5267">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5269">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5269">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-5270">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-5270">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-5271">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5271">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-5272">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5272">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5273">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5273">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5274">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5274">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5275">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-5275">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-5276">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-5276">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-5277">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5277">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-5278">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5278">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-5279">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5279">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5280">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5280">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5281">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-5281">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-5282">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-5283">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5284">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5285">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5285">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-5286">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-5286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-5287">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-5288">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-5288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-5289">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-5289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-5290">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5290">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-5291">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-5292">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5293">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-5293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5294">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-5294">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5296">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5296">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5297">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5297">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5298">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-5298">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-5299">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5299">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-5300">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5300">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-5301">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-5301">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-5302">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-5302">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-5303">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-5303">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5305">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5305">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5307">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5307">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5309">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5309">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-5310">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5310">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="0cbba-5311">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5311">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="0cbba-5312">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5312">Target</span></span> | <span data-ttu-id="0cbba-5313">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-5313">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-5314">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5314">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-5315">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-5315">8</span></span> |
| <span data-ttu-id="0cbba-5316">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5316">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5318">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5318">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5319">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-5319">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5320">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-5320">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5321">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5321">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5322">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5322">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-5323">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5323">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5325">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5325">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-5326">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-5326">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-5327">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5327">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-5328">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5328">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5329">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5329">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5330">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5330">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5331">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-5331">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-5332">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-5332">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-5333">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5333">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-5334">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5334">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-5335">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5335">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5336">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5336">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5337">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-5337">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-5338">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5338">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-5339">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5339">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5340">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5340">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5341">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5341">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-5342">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-5342">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-5343">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5343">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-5344">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-5344">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-5345">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-5345">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-5346">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5346">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-5347">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5347">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-5348">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5348">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5349">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-5349">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5350">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-5350">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5352">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5352">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5353">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5353">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5354">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-5354">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-5355">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5355">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-5356">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5356">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-5357">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-5357">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-5358">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-5358">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-5359">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-5359">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5361">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5361">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5363">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5363">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5365">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5365">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-5366">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5366">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="0cbba-5367">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5367">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="0cbba-5368">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5368">Target</span></span> | <span data-ttu-id="0cbba-5369">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-5369">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-5370">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5370">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-5371">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-5371">16</span></span> |
| <span data-ttu-id="0cbba-5372">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5372">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5374">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5374">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5375">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-5375">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5376">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-5376">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5377">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5377">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5378">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5378">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-5379">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5379">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5381">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5381">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-5382">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-5382">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-5383">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5383">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-5384">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5384">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5385">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5385">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5386">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5386">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5387">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-5387">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-5388">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-5388">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-5389">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5389">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-5390">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5390">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-5391">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5391">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5392">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5392">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5393">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-5393">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-5394">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5394">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-5395">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5395">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5396">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5396">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5397">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5397">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-5398">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-5398">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-5399">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5399">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-5400">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-5400">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-5401">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-5401">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-5402">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5402">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-5403">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5403">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-5404">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5404">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5405">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-5405">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5406">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-5406">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5408">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5408">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5409">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5409">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5410">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-5410">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-5411">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5411">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-5412">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5412">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-5413">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-5413">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-5414">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-5414">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-5415">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-5415">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5417">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5417">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5419">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5419">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5421">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5421">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-5422">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5422">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="0cbba-5423">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5423">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="0cbba-5424">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5424">Target</span></span> | <span data-ttu-id="0cbba-5425">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-5425">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-5426">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5426">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-5427">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-5427">16</span></span> |
| <span data-ttu-id="0cbba-5428">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5428">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5430">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5430">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5431">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-5431">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5432">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-5432">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5433">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5433">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5434">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5434">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-5435">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5435">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5437">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5437">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-5438">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-5438">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-5439">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5439">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-5440">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5440">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5441">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5442">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5443">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-5443">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-5444">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-5444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-5445">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5445">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-5446">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5446">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-5447">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5447">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5448">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5448">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5449">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-5449">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-5450">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5450">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-5451">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5451">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5452">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5452">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5453">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5453">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-5454">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-5454">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-5455">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5455">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-5456">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-5456">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-5457">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-5457">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-5458">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5458">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-5459">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5459">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-5460">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5460">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5461">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-5461">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5462">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-5462">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5464">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5464">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5465">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5465">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5466">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-5466">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-5467">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5467">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-5468">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5468">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-5469">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-5469">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-5470">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-5470">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-5471">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-5471">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5473">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5473">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5475">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5475">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5477">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5477">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-5478">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5478">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="0cbba-5479">DXGI_FORMAT_420 nicht transparent \_ <sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5479">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="0cbba-5480">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5480">Target</span></span> | <span data-ttu-id="0cbba-5481">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-5481">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-5482">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5482">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-5483">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-5483">8</span></span> |
| <span data-ttu-id="0cbba-5484">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5484">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5486">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5486">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5487">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-5487">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5488">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-5488">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5489">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5489">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5490">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5490">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-5491">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5491">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5493">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5493">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-5494">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-5494">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-5495">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5495">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-5496">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5496">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5497">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5497">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5498">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5498">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5499">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-5499">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-5500">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-5500">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-5501">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5501">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-5502">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5502">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-5503">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5503">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5504">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5504">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5505">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-5505">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-5506">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5506">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-5507">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5507">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5508">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5508">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5509">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5509">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-5510">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-5510">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-5511">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5511">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-5512">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-5512">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-5513">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-5513">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-5514">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5514">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-5515">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5515">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-5516">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5516">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5517">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-5517">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5518">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-5518">CPU Lockable</span></span> | \- |
| <span data-ttu-id="0cbba-5519">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5519">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5520">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5520">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5521">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-5521">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-5522">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5522">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-5523">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5523">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-5524">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-5524">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-5525">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-5525">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-5526">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-5526">Video Decoder Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5528">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5528">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5530">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5530">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5532">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5532">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-5533">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5533">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="0cbba-5534">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5534">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="0cbba-5535">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5535">Target</span></span> | <span data-ttu-id="0cbba-5536">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-5536">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-5537">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5537">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-5538">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-5538">16</span></span> |
| <span data-ttu-id="0cbba-5539">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5539">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5541">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5541">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5542">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-5542">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5543">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-5543">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5544">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5544">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5545">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5545">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-5546">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5546">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5548">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5548">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-5549">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-5549">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-5550">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5550">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-5551">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5551">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5552">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5552">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5553">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5553">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5554">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-5554">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-5555">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-5555">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-5556">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5556">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-5557">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5557">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-5558">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5558">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5559">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5559">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5560">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-5560">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-5561">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5561">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-5562">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5562">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5563">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5563">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5564">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5564">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-5565">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-5565">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-5566">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5566">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-5567">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-5567">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-5568">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-5568">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-5569">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5569">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-5570">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5570">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-5571">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5571">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5572">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-5572">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5573">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-5573">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5575">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5575">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5576">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5576">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5577">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-5577">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-5578">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5578">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-5579">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5579">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-5580">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-5580">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-5581">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-5581">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-5582">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-5582">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5584">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5584">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5586">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5586">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5588">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5588">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-5589">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5589">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="0cbba-5590">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5590">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="0cbba-5591">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5591">Target</span></span> | <span data-ttu-id="0cbba-5592">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-5592">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-5593">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5593">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-5594">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-5594">32</span></span> |
| <span data-ttu-id="0cbba-5595">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5595">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5597">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5597">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5598">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-5598">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5599">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-5599">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5600">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5600">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5601">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5601">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-5602">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5602">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5604">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-5605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-5605">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-5606">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-5607">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5608">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5609">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5610">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-5610">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-5611">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-5611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-5612">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5612">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-5613">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-5614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5614">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5615">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5616">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-5616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-5617">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-5618">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5619">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5620">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5620">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-5621">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-5621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-5622">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-5623">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-5623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-5624">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-5624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-5625">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-5626">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-5627">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5628">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-5628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5629">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-5629">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5631">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5631">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5632">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5632">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5633">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-5633">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-5634">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5634">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-5635">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5635">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-5636">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-5636">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-5637">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-5637">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-5638">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-5638">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5640">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5640">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5642">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5642">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5644">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5644">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-5645">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5645">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="0cbba-5646">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5646">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="0cbba-5647">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5647">Target</span></span> | <span data-ttu-id="0cbba-5648">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-5648">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-5649">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5649">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-5650">32</span><span class="sxs-lookup"><span data-stu-id="0cbba-5650">32</span></span> |
| <span data-ttu-id="0cbba-5651">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5651">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5653">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5653">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5654">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-5654">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5655">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-5655">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5656">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5656">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5657">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5657">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-5658">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5658">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5660">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5660">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-5661">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-5661">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-5662">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5662">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-5663">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5664">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5665">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5666">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-5666">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-5667">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-5667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-5668">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5668">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-5669">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5669">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-5670">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5670">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5671">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5671">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5672">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-5672">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-5673">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5673">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-5674">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5674">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5675">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5675">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5676">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5676">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-5677">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-5677">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-5678">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5678">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-5679">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-5679">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-5680">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-5680">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-5681">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5681">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-5682">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5682">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-5683">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5683">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5684">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-5684">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5685">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-5685">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5687">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5687">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5688">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5688">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5689">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-5689">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-5690">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5690">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-5691">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5691">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-5692">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-5692">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-5693">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-5693">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-5694">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-5694">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5696">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5696">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5698">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5698">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5700">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5700">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-5701">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="0cbba-5702">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5702">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="0cbba-5703">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5703">Target</span></span> | <span data-ttu-id="0cbba-5704">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-5704">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-5705">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-5706">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-5706">8</span></span> |
| <span data-ttu-id="0cbba-5707">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5707">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5709">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5709">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5710">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-5710">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5711">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-5711">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5712">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5712">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5713">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5713">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-5714">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5714">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5716">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5716">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-5717">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-5717">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-5718">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5718">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-5719">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5719">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5720">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5720">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5721">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5721">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5722">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-5722">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-5723">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-5723">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-5724">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5724">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-5725">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5725">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-5726">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5726">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5727">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5727">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5728">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-5728">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-5729">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5729">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-5730">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5730">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5731">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5731">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5732">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5732">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-5733">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-5733">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-5734">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5734">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-5735">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-5735">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-5736">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-5736">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-5737">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5737">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-5738">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5738">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-5739">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5739">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5740">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-5740">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5741">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-5741">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5743">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5743">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5744">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5744">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5745">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-5745">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-5746">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5746">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-5747">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5747">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-5748">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-5748">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-5749">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-5749">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-5750">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-5750">Video Decoder Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5752">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5752">Video Processor Input</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5754">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5754">Video Processor Output</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5756">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5756">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-5757">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5757">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="0cbba-5758">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5758">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="0cbba-5759">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5759">Target</span></span> | <span data-ttu-id="0cbba-5760">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-5760">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-5761">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5761">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-5762">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-5762">8</span></span> |
| <span data-ttu-id="0cbba-5763">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5763">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5765">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5765">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5766">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-5766">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5767">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-5767">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5768">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5768">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5769">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5769">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-5770">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5770">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5772">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5772">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-5773">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-5773">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-5774">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5774">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-5775">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5775">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5776">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5776">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5777">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5777">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5778">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-5778">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-5779">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-5779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-5780">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5780">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-5781">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5781">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-5782">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5782">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5783">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5783">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5784">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-5784">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-5785">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5785">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-5786">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5786">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5787">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5787">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5788">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5788">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-5789">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-5789">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-5790">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5790">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-5791">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-5791">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-5792">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-5792">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-5793">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5793">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-5794">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5794">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-5795">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5795">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5796">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-5796">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5797">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-5797">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5799">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5799">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5800">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5800">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5801">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-5801">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-5802">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5802">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-5803">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5803">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-5804">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-5804">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-5805">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-5805">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-5806">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-5806">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-5807">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5807">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5809">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5809">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-5810">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5810">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-5811">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="0cbba-5812">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5812">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="0cbba-5813">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5813">Target</span></span> | <span data-ttu-id="0cbba-5814">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-5814">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-5815">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-5816">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-5816">8</span></span> |
| <span data-ttu-id="0cbba-5817">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5817">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5819">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5819">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5820">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-5820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5821">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-5821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5822">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5823">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-5824">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5824">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5826">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5826">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-5827">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-5827">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-5828">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5828">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-5829">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5829">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5830">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5830">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5831">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5831">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5832">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-5832">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-5833">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-5833">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-5834">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5834">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-5835">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5835">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-5836">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5836">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5837">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5837">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5838">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-5838">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-5839">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5839">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-5840">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5840">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5841">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5841">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5842">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5842">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-5843">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-5843">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-5844">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5844">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-5845">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-5845">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-5846">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-5846">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-5847">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5847">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-5848">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5848">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-5849">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5849">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5850">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-5850">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5851">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-5851">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5853">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5853">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5854">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5854">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5855">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-5855">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-5856">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5856">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-5857">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5857">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-5858">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-5858">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-5859">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-5859">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-5860">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-5860">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-5861">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5861">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5863">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5863">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-5864">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5864">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-5865">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5865">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="0cbba-5866">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5866">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="0cbba-5867">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5867">Target</span></span> | <span data-ttu-id="0cbba-5868">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-5868">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-5869">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5869">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-5870">8</span><span class="sxs-lookup"><span data-stu-id="0cbba-5870">8</span></span> |
| <span data-ttu-id="0cbba-5871">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5871">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5873">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5873">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5874">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-5874">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5875">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-5875">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5876">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5876">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5877">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5877">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-5878">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5878">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5880">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5880">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-5881">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-5881">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-5882">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5882">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-5883">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5883">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5884">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5884">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5885">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5885">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5886">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-5886">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-5887">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-5887">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-5888">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5888">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-5889">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5889">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-5890">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5890">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5891">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5891">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5892">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-5892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-5893">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-5894">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5895">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5896">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5896">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-5897">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-5897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-5898">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-5899">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-5899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-5900">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-5900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-5901">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5901">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-5902">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-5903">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5904">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-5904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5905">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-5905">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5907">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5907">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5908">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5908">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5909">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-5909">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-5910">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5910">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-5911">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5911">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-5912">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-5912">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-5913">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-5913">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-5914">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-5914">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-5915">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5915">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5917">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5917">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-5918">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5918">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-5919">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5919">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="0cbba-5920">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5920">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="0cbba-5921">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5921">Target</span></span> | <span data-ttu-id="0cbba-5922">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-5922">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-5923">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5923">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-5924">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-5924">16</span></span> |
| <span data-ttu-id="0cbba-5925">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5925">Format Support</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-5927">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5927">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5928">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-5928">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5929">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-5929">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5930">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5930">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5931">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5931">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-5932">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5932">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5934">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5934">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-5935">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-5935">TextureCube</span></span> | \- |
| <span data-ttu-id="0cbba-5936">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5936">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="0cbba-5937">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5937">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5938">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5938">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5939">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5939">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5940">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-5940">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-5941">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-5941">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-5942">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5942">Mipmap</span></span> | \- |
| <span data-ttu-id="0cbba-5943">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5943">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="0cbba-5944">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5944">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5945">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5945">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5946">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-5946">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-5947">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5947">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-5948">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5948">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5949">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5949">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-5950">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-5950">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-5951">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-5951">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-5952">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5952">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-5953">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-5953">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-5954">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-5954">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-5955">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5955">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-5956">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-5956">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-5957">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5957">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5958">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-5958">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-5959">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-5959">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5961">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5961">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5962">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-5962">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-5963">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-5963">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-5964">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5964">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-5965">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5965">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-5966">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-5966">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-5967">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-5967">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-5968">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-5968">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-5969">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5969">Video Processor Input</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5971">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-5971">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-5972">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5972">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-5973">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-5973">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="0cbba-5974">DXGI_FORMAT_B4G4R4A4 \_ unorm<sup></sup> -Fehler (115)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5974">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="0cbba-5975">Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-5975">Target</span></span> | <span data-ttu-id="0cbba-5976">Support</span><span class="sxs-lookup"><span data-stu-id="0cbba-5976">Support</span></span> |
| - | - |
| <span data-ttu-id="0cbba-5977">Bits pro Element (BPE)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5977">Bits Per Element (BPE)</span></span> | <span data-ttu-id="0cbba-5978">16</span><span class="sxs-lookup"><span data-stu-id="0cbba-5978">16</span></span> |
| <span data-ttu-id="0cbba-5979">Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0cbba-5979">Format Support</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5981">Buffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5981">Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5982">Vertex-Puffer des Eingabe Assemblers</span><span class="sxs-lookup"><span data-stu-id="0cbba-5982">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5983">Index Puffer für Eingabe Assembler</span><span class="sxs-lookup"><span data-stu-id="0cbba-5983">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5984">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="0cbba-5984">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="0cbba-5985">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5985">Texture1D</span></span> | \- |
| <span data-ttu-id="0cbba-5986">Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5986">Texture2D</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5988">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0cbba-5988">Texture3D</span></span> | \- |
| <span data-ttu-id="0cbba-5989">TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cbba-5989">TextureCube</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5991">Shader-Beispiel (nur Punkt Stichprobe)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5991">Shader sample (point sample only)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5993">Shader-Beispiel (beliebiger Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5993">Shader sample (any filter)</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-5995">Shader-Beispiel \_ c (Vergleichs Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5995">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5996">Shader-Beispiel (mono-1-Bit-Filter)</span><span class="sxs-lookup"><span data-stu-id="0cbba-5996">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="0cbba-5997">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="0cbba-5997">Shader gather4</span></span> | \- |
| <span data-ttu-id="0cbba-5998">Shader gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="0cbba-5998">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="0cbba-5999">MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-5999">Mipmap</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-6001">Automatische Generierung von MipMap</span><span class="sxs-lookup"><span data-stu-id="0cbba-6001">Mipmap Auto-Generation</span></span> | ![Optional](images/letter-o.jpg) |
| <span data-ttu-id="0cbba-6003">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-6003">RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-6004">Blendable renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-6004">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-6005">Ausgabe der Zusammenführungs Logik op</span><span class="sxs-lookup"><span data-stu-id="0cbba-6005">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="0cbba-6006">Tiefen-/Stencil-Ziel</span><span class="sxs-lookup"><span data-stu-id="0cbba-6006">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="0cbba-6007">Unformatierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-6007">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-6008">Strukturierte UAV und SRV</span><span class="sxs-lookup"><span data-stu-id="0cbba-6008">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="0cbba-6009">Typisierte UAV</span><span class="sxs-lookup"><span data-stu-id="0cbba-6009">Typed UAV</span></span> | \- |
| <span data-ttu-id="0cbba-6010">Mit UAV typisierter Speicher</span><span class="sxs-lookup"><span data-stu-id="0cbba-6010">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="0cbba-6011">UAV-typisierte Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-6011">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="0cbba-6012">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="0cbba-6012">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="0cbba-6013">Atomarische UAV-OPS</span><span class="sxs-lookup"><span data-stu-id="0cbba-6013">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="0cbba-6014">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="0cbba-6014">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="0cbba-6015">Atomarer UAV-Austausch</span><span class="sxs-lookup"><span data-stu-id="0cbba-6015">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="0cbba-6016">UAV-atomarischer Mindestwert (min oder max)</span><span class="sxs-lookup"><span data-stu-id="0cbba-6016">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-6017">UAV-atomarer unsigniertes Minimum oder Maximum</span><span class="sxs-lookup"><span data-stu-id="0cbba-6017">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="0cbba-6018">CPU-Sperr fähig</span><span class="sxs-lookup"><span data-stu-id="0cbba-6018">CPU Lockable</span></span> | ![Erforderlich](images/letter-r.jpg) |
| <span data-ttu-id="0cbba-6020">4X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-6020">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-6021">8X-Multisample-renderTarget</span><span class="sxs-lookup"><span data-stu-id="0cbba-6021">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="0cbba-6022">Andere Multisample count RT</span><span class="sxs-lookup"><span data-stu-id="0cbba-6022">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="0cbba-6023">Multisample-Auflösung</span><span class="sxs-lookup"><span data-stu-id="0cbba-6023">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="0cbba-6024">Multisample-Auslastung</span><span class="sxs-lookup"><span data-stu-id="0cbba-6024">Multisample Load</span></span> | \- |
| <span data-ttu-id="0cbba-6025">Anzeige Scan-Out</span><span class="sxs-lookup"><span data-stu-id="0cbba-6025">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="0cbba-6026">Umwandlung in bitlayout</span><span class="sxs-lookup"><span data-stu-id="0cbba-6026">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="0cbba-6027">Unterstützung für Video Decoder</span><span class="sxs-lookup"><span data-stu-id="0cbba-6027">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="0cbba-6028">Eingabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-6028">Video Processor Input</span></span> | \- |
| <span data-ttu-id="0cbba-6029">Ausgabe des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="0cbba-6029">Video Processor Output</span></span> | \- |
| <span data-ttu-id="0cbba-6030">Gemeinsam genutzte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-6030">Shared Resource</span></span> | \- |
| <span data-ttu-id="0cbba-6031">Gekachelte Ressource</span><span class="sxs-lookup"><span data-stu-id="0cbba-6031">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="0cbba-6032">Notizen formatieren</span><span class="sxs-lookup"><span data-stu-id="0cbba-6032">Format notes</span></span>

<span data-ttu-id="0cbba-6033">Der Zweck des-Formats kann sich von einer Hardware Funktionsebene zur nächsten ändern.</span><span class="sxs-lookup"><span data-stu-id="0cbba-6033">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="0cbba-6034"><sup>L</sup> : typloses Format</span><span class="sxs-lookup"><span data-stu-id="0cbba-6034"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="0cbba-6035"><sup>PCs</sup> : teilweise typisiertes, castbares und einfaches Layout</span><span class="sxs-lookup"><span data-stu-id="0cbba-6035"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="0cbba-6036"><sup>FCS</sup> : vollständig typisiertes, castbares und einfaches Layout</span><span class="sxs-lookup"><span data-stu-id="0cbba-6036"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="0cbba-6037"><sup>FNS</sup> : vollständig typisiertes, nicht-castbares und einfaches Layout</span><span class="sxs-lookup"><span data-stu-id="0cbba-6037"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="0cbba-6038"><sup>PCC</sup> : teilweise typisiertes, castbares und komplexes Layout</span><span class="sxs-lookup"><span data-stu-id="0cbba-6038"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="0cbba-6039"><sup>FCC</sup> : vollständig typisiertes, castbares und komplexes Layout</span><span class="sxs-lookup"><span data-stu-id="0cbba-6039"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="0cbba-6040"><sup>FNC</sup> : vollständig typisiertes, nicht-castbares und komplexes Layout</span><span class="sxs-lookup"><span data-stu-id="0cbba-6040"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="0cbba-6041"><sup>V</sup> : Videoformat</span><span class="sxs-lookup"><span data-stu-id="0cbba-6041"><sup>V</sup> : video format</span></span>
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="0cbba-6042">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0cbba-6042">Related topics</span></span>

[<span data-ttu-id="0cbba-6043">D3D12-Hardware Funktionsebenen</span><span class="sxs-lookup"><span data-stu-id="0cbba-6043">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

<span data-ttu-id="0cbba-6044">[Implementieren von Schatten Puffern für Direct3D Feature Level 9](/previous-versions/windows/apps/jj262110(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="0cbba-6044">[Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10))</span></span>

[<span data-ttu-id="0cbba-6045">Mapping von Legacy Formaten</span><span class="sxs-lookup"><span data-stu-id="0cbba-6045">Mapping Legacy Formats</span></span>](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[<span data-ttu-id="0cbba-6046">Programmier Handbuch für DXGI</span><span class="sxs-lookup"><span data-stu-id="0cbba-6046">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
