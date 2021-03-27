---
title: D3DCOMPILE-Konstanten (D3DCompiler. h)
description: Die D3DCOMPILE-Konstanten geben an, wie der Compiler den HLSL-Code kompiliert.
ms.assetid: 039627DD-D6A4-4EA3-8E91-D2A20770E6FF
topic_type:
- apiref
api_name:
- D3DCOMPILE_DEBUG
- D3DCOMPILE_SKIP_VALIDATION
- D3DCOMPILE_SKIP_OPTIMIZATION
- D3DCOMPILE_PACK_MATRIX_ROW_MAJOR
- D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR
- D3DCOMPILE_PARTIAL_PRECISION
- D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT
- D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT
- D3DCOMPILE_NO_PRESHADER
- D3DCOMPILE_AVOID_FLOW_CONTROL
- D3DCOMPILE_PREFER_FLOW_CONTROL
- D3DCOMPILE_ENABLE_STRICTNESS
- D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY
- D3DCOMPILE_IEEE_STRICTNESS
- D3DCOMPILE_OPTIMIZATION_LEVEL0
- D3DCOMPILE_OPTIMIZATION_LEVEL1
- D3DCOMPILE_OPTIMIZATION_LEVEL2
- D3DCOMPILE_OPTIMIZATION_LEVEL3
- D3DCOMPILE_WARNINGS_ARE_ERRORS
- D3DCOMPILE_RESOURCES_MAY_ALIAS
- D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES
- D3DCOMPILE_ALL_RESOURCES_BOUND
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfd396eef06260ae879a3bb816d0bd89a078ea53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219453"
---
# <a name="d3dcompile-constants"></a><span data-ttu-id="9ad5e-103">D3DCOMPILE-Konstanten</span><span class="sxs-lookup"><span data-stu-id="9ad5e-103">D3DCOMPILE Constants</span></span>

<span data-ttu-id="9ad5e-104">Die D3DCOMPILE-Konstanten geben an, wie der Compiler den HLSL-Code kompiliert.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-104">The D3DCOMPILE constants specify how the compiler compiles the HLSL code.</span></span>

<dl> <dt>

<span data-ttu-id="9ad5e-105"><span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**D3DCOMPILE \_ Debuggen**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-105"><span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**D3DCOMPILE\_DEBUG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-106">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-106">(1 << 0)</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-107">Weist den Compiler an, Debugdateien/Zeilen-/Typ-/Symbolinformationen in den Ausgabe Code einzufügen.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-107">Directs the compiler to insert debug file/line/type/symbol information into the output code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-108"><span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE \_ über \_ Prüfung überspringen**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-108"><span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE\_SKIP\_VALIDATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-109">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-109">(1 << 1)</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-110">Weist den Compiler an, den generierten Code nicht anhand bekannter Funktionen und Einschränkungen zu validieren.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-110">Directs the compiler not to validate the generated code against known capabilities and constraints.</span></span> <span data-ttu-id="9ad5e-111">Es wird empfohlen, diese Konstante nur mit Shadern zu verwenden, die in der Vergangenheit erfolgreich kompiliert wurden.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-111">We recommend that you use this constant only with shaders that have been successfully compiled in the past.</span></span> <span data-ttu-id="9ad5e-112">DirectX überprüft Shader immer, bevor Sie auf ein Gerät festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-112">DirectX always validates shaders before it sets them to a device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-113"><span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**D3DCOMPILE \_ Skip- \_ Optimierung**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-113"><span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**D3DCOMPILE\_SKIP\_OPTIMIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-114">(1 << 2)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-114">(1 << 2)</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-115">Weist den Compiler an, während der Codegenerierung Optimierungsschritte zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-115">Directs the compiler to skip optimization steps during code generation.</span></span> <span data-ttu-id="9ad5e-116">Es wird empfohlen, diese Konstante nur für Debugzwecke festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-116">We recommend that you set this constant for debug purposes only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-117"><span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**D3DCOMPILE \_ Paket \_ Matrix \_ Zeile \_ Hauptversion**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-117"><span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**D3DCOMPILE\_PACK\_MATRIX\_ROW\_MAJOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-118">(1 << 3)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-118">(1 << 3)</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-119">Weist den Compiler an, Matrizen in der Zeilen Hauptreihenfolge für die Eingabe und Ausgabe aus dem Shader zu verpacken.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-119">Directs the compiler to pack matrices in row-major order on input and output from the shader.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-120"><span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**D3DCOMPILE \_ Paket- \_ Matrix \_ Spalte \_ Hauptversion**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-120"><span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**D3DCOMPILE\_PACK\_MATRIX\_COLUMN\_MAJOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-121">(1 << 4)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-121">(1 << 4)</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-122">Weist den Compiler an, Matrizen in der Spalte-Haupt Reihenfolge für die Eingabe und Ausgabe aus dem Shader zu verpacken.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-122">Directs the compiler to pack matrices in column-major order on input and output from the shader.</span></span> <span data-ttu-id="9ad5e-123">Diese Art von Verpackung ist in der Regel effizienter, da eine Reihe von Punkt Produkten dann eine Vektor Matrix Multiplikation durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-123">This type of packing is generally more efficient because a series of dot-products can then perform vector-matrix multiplication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-124"><span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**D3DCOMPILE \_ partielle \_ Genauigkeit**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-124"><span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**D3DCOMPILE\_PARTIAL\_PRECISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-125">(1 << 5)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-125">(1 << 5)</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-126">Weist den Compiler an, alle Berechnungen mit teilweiser Genauigkeit auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-126">Directs the compiler to perform all computations with partial precision.</span></span> <span data-ttu-id="9ad5e-127">Wenn Sie diese Konstante festlegen, kann der kompilierte Code auf Hardware möglicherweise schneller ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-127">If you set this constant, the compiled code might run faster on some hardware.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-128"><span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE \_ Force \_ vs \_ Software \_ No \_ Opt**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-128"><span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE\_FORCE\_VS\_SOFTWARE\_NO\_OPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-129">(1 << 6)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-129">(1 << 6)</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-130">Weist den Compiler an, einen Vertex-Shader für das nächsthöhere Shader-Profil zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-130">Directs the compiler to compile a vertex shader for the next highest shader profile.</span></span> <span data-ttu-id="9ad5e-131">Diese Konstante schaltet Debuggen und Optimierungen aus.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-131">This constant turns debugging on and optimizations off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-132"><span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE \_ Erzwingen von \_ PS- \_ Software \_ Nein \_ Opt**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-132"><span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE\_FORCE\_PS\_SOFTWARE\_NO\_OPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-133">(1 << 7)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-133">(1 << 7)</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-134">Weist den Compiler an, einen PixelShader für das nächste höchste Shader-Profil zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-134">Directs the compiler to compile a pixel shader for the next highest shader profile.</span></span> <span data-ttu-id="9ad5e-135">Diese Konstante schaltet auch Debuggen und Optimierungen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-135">This constant also turns debugging on and optimizations off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-136"><span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE \_ kein \_ preshader**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-136"><span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE\_NO\_PRESHADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-137">(1 << 8)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-137">(1 << 8)</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-138">Weist den Compiler an, preshaders zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-138">Directs the compiler to disable Preshaders.</span></span> <span data-ttu-id="9ad5e-139">Wenn Sie diese Konstante festlegen, führt der Compiler keinen statischen Ausdruck für die Auswertung aus.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-139">If you set this constant, the compiler does not pull out static expression for evaluation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-140"><span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE \_ Vermeidung der \_ Fluss \_ Steuerung**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-140"><span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE\_AVOID\_FLOW\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-141">(1 << 9)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-141">(1 << 9)</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-142">Weist den Compiler an, keine Flow-steuerungskonstrukte zu verwenden, sofern möglich.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-142">Directs the compiler to not use flow-control constructs where possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-143"><span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE \_ bevorzugen der \_ Fluss \_ Steuerung**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-143"><span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE\_PREFER\_FLOW\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-144">(1 << 10)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-144">(1 << 10)</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-145">Weist den Compiler an, Fluss Steuerungs Konstrukte zu verwenden, sofern möglich.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-145">Directs the compiler to use flow-control constructs where possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-146"><span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE \_ Aktivieren von \_ strictivität**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-146"><span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE\_ENABLE\_STRICTNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-147">(1 << 11)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-147">(1 << 11)</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-148">Erzwingt eine strikte Kompilierung, die möglicherweise keine Legacy Syntax zulässt.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-148">Forces strict compile, which might not allow for legacy syntax.</span></span>

<span data-ttu-id="9ad5e-149">Standardmäßig deaktiviert der Compiler die strenge in der veralteten Syntax.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-149">By default, the compiler disables strictness on deprecated syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-150"><span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE-abwärts \_ \_ \_ Kompatibilität aktivieren**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-150"><span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE\_ENABLE\_BACKWARDS\_COMPATIBILITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-151">(1 << 12)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-151">(1 << 12)</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-152">Weist den Compiler an, ältere Shader für die Kompilierung in 5-0-Ziele zu aktivieren \_ .</span><span class="sxs-lookup"><span data-stu-id="9ad5e-152">Directs the compiler to enable older shaders to compile to 5\_0 targets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-153"><span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**D3DCOMPILE \_ IEEE- \_ strenge**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-153"><span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**D3DCOMPILE\_IEEE\_STRICTNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-154">(1 << 13)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-154">(1 << 13)</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-155">Erzwingt die IEEE Strict-Kompilierung.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-155">Forces the IEEE strict compile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-156"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**D3DCOMPILE- \_ Optimierung \_ LEVEL0**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-156"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL0**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-157">(1 << 14)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-157">(1 << 14)</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-158">Weist den Compiler an, die niedrigste Optimierungs Ebene zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-158">Directs the compiler to use the lowest optimization level.</span></span> <span data-ttu-id="9ad5e-159">Wenn Sie diese Konstante festlegen, erzeugt der Compiler möglicherweise langsameren Code, erzeugt den Code aber schneller.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-159">If you set this constant, the compiler might produce slower code but produces the code more quickly.</span></span> <span data-ttu-id="9ad5e-160">Legen Sie diese Konstante fest, wenn Sie den Shader iterativ entwickeln.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-160">Set this constant when you develop the shader iteratively.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-161"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**D3DCOMPILE- \_ Optimierung \_ Level1**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-161"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-162">0</span><span class="sxs-lookup"><span data-stu-id="9ad5e-162">0</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-163">Weist den Compiler an, die zweite niedrigste Optimierungs Ebene zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-163">Directs the compiler to use the second lowest optimization level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-164"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**D3DCOMPILE- \_ Optimierung \_ Level2**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-164"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-165">((1 << 14) \| (1 << 15))</span><span class="sxs-lookup"><span data-stu-id="9ad5e-165">((1 << 14) \| (1 << 15))</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-166">Weist den Compiler an, die zweithöchste Optimierungs Ebene zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-166">Directs the compiler to use the second highest optimization level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-167"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**D3DCOMPILE- \_ Optimierung \_ LEVEL3**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-167"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-168">(1 << 15)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-168">(1 << 15)</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-169">Weist den Compiler an, die höchste Optimierungs Ebene zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-169">Directs the compiler to use the highest optimization level.</span></span> <span data-ttu-id="9ad5e-170">Wenn Sie diese Konstante festlegen, erzeugt der Compiler den bestmöglichen Code, kann aber erheblich länger dauern.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-170">If you set this constant, the compiler produces the best possible code but might take significantly longer to do so.</span></span> <span data-ttu-id="9ad5e-171">Legen Sie diese Konstante für endgültige Builds einer Anwendung fest, wenn die Leistung der wichtigste Faktor ist.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-171">Set this constant for final builds of an application when performance is the most important factor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-172"><span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**D3DCOMPILE- \_ Warnungen \_ sind \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-172"><span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**D3DCOMPILE\_WARNINGS\_ARE\_ERRORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-173">(1 << 18)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-173">(1 << 18)</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-174">Weist den Compiler an, alle Warnungen als Fehler zu behandeln, wenn der Shader-Code kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-174">Directs the compiler to treat all warnings as errors when it compiles the shader code.</span></span> <span data-ttu-id="9ad5e-175">Es wird empfohlen, diese Konstante für neuen Shader-Code zu verwenden, damit Sie alle Warnungen auflösen und die Anzahl von schwer zu suchenden Code Fehlern verringern können.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-175">We recommend that you use this constant for new shader code, so that you can resolve all warnings and lower the number of hard-to-find code defects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-176"><span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**D3DCOMPILE \_ - \_ Ressourcen \_ Alias**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-176"><span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**D3DCOMPILE\_RESOURCES\_MAY\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-177">(1 << 19)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-177">(1 << 19)</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-178">Weist den Compiler an, davon auszugehen, dass für CS 5 0 ein Alias für nicht geordnete Zugriffs Sichten (UAVs) und Shader-Ressourcen Sichten (Srvs) möglich ist \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9ad5e-178">Directs the compiler to assume that unordered access views (UAVs) and shader resource views (SRVs) may alias for cs\_5\_0.</span></span>

> [!Note]  
> <span data-ttu-id="9ad5e-179">Diese Compilerkonstante ist neu, beginnend mit dem D3dcompiler- \_47.dll.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-179">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-180"><span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE \_ Aktivieren von \_ ungebundenen \_ \_ deskriptortabellen**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-180"><span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE\_ENABLE\_UNBOUNDED\_DESCRIPTOR\_TABLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-181">(1 << 20)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-181">(1 << 20)</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-182">Weist den Compiler an, ungebundene deskriptortabellen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-182">Directs the compiler to enable unbounded descriptor tables.</span></span>

> [!Note]  
> <span data-ttu-id="9ad5e-183">Diese Compilerkonstante ist neu, beginnend mit dem D3dcompiler- \_47.dll.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-183">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ad5e-184"><span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE \_ alle \_ Ressourcen \_ gebunden**</span><span class="sxs-lookup"><span data-stu-id="9ad5e-184"><span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE\_ALL\_RESOURCES\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad5e-185">(1 << 21)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-185">(1 << 21)</span></span>
</dt> <dt>



<span data-ttu-id="9ad5e-186">Weist den Compiler an, sicherzustellen, dass alle Ressourcen gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-186">Directs the compiler to ensure all resources are bound.</span></span>

> [!Note]  
> <span data-ttu-id="9ad5e-187">Diese Compilerkonstante ist neu, beginnend mit dem D3dcompiler- \_47.dll.</span><span class="sxs-lookup"><span data-stu-id="9ad5e-187">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ad5e-188">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9ad5e-188">Requirements</span></span>



| <span data-ttu-id="9ad5e-189">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ad5e-189">Requirement</span></span> | <span data-ttu-id="9ad5e-190">Wert</span><span class="sxs-lookup"><span data-stu-id="9ad5e-190">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ad5e-191">Header</span><span class="sxs-lookup"><span data-stu-id="9ad5e-191">Header</span></span><br/> | <dl> <span data-ttu-id="9ad5e-192"><dt>D3DCompiler. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ad5e-192"><dt>D3DCompiler.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ad5e-193">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9ad5e-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ad5e-194">D3DCompiler-Konstanten</span><span class="sxs-lookup"><span data-stu-id="9ad5e-194">D3DCompiler Constants</span></span>](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

 





