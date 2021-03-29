---
title: ASM-Shader-Referenz
description: Shader steuern die programmierbare Grafik Pipeline.
ms.assetid: 2c58815c-83b5-4ae8-a192-ba865b485bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2941f4c32d03187ce08266bf1382cd1d94301ce0
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2019
ms.locfileid: "104976544"
---
# <a name="asm-shader-reference"></a><span data-ttu-id="3d164-103">ASM-Shader-Referenz</span><span class="sxs-lookup"><span data-stu-id="3d164-103">Asm Shader Reference</span></span>

<span data-ttu-id="3d164-104">Shader steuern die programmierbare Grafik Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3d164-104">Shaders drive the programmable graphics pipeline.</span></span>

## <a name="vertex-shader-reference"></a><span data-ttu-id="3d164-105">Vertex-Shader-Referenz</span><span class="sxs-lookup"><span data-stu-id="3d164-105">Vertex Shader Reference</span></span>

-   [<span data-ttu-id="3d164-106">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3d164-106">vs\_1\_1</span></span>](dx9-graphics-reference-asm-vs-1-1.md)
-   [<span data-ttu-id="3d164-107">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3d164-107">vs\_2\_0</span></span>](dx9-graphics-reference-asm-vs-2-0.md)
-   [<span data-ttu-id="3d164-108">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3d164-108">vs\_2\_x</span></span>](dx9-graphics-reference-asm-vs-2-x.md)
-   [<span data-ttu-id="3d164-109">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3d164-109">vs\_3\_0</span></span>](dx9-graphics-reference-asm-vs-3-0.md)

<span data-ttu-id="3d164-110">[Scheitelpunkt-Shader-Unterschiede](dx9-graphics-reference-asm-vs-differences.md) fassen die Unterschiede zwischen Scheitelpunkt-shaderversionen zusammen</span><span class="sxs-lookup"><span data-stu-id="3d164-110">[Vertex Shader Differences](dx9-graphics-reference-asm-vs-differences.md) summarizes the differences between vertex shader versions.</span></span>

## <a name="pixel-shader-reference"></a><span data-ttu-id="3d164-111">Pixel-Shader-Referenz</span><span class="sxs-lookup"><span data-stu-id="3d164-111">Pixel Shader Reference</span></span>

-   [<span data-ttu-id="3d164-112">PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="3d164-112">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4</span></span>](dx9-graphics-reference-asm-ps-1-x.md)
-   [<span data-ttu-id="3d164-113">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3d164-113">ps\_2\_0</span></span>](dx9-graphics-reference-asm-ps-2-0.md)
-   [<span data-ttu-id="3d164-114">PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3d164-114">ps\_2\_x</span></span>](dx9-graphics-reference-asm-ps-2-x.md)
-   [<span data-ttu-id="3d164-115">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3d164-115">ps\_3\_0</span></span>](dx9-graphics-reference-asm-ps-3-0.md)

<span data-ttu-id="3d164-116">[Pixel-shaderunterschiede](dx9-graphics-reference-asm-ps-differences.md) fasst die Unterschiede zwischen den Pixel-Shader-Versionen zusammen.</span><span class="sxs-lookup"><span data-stu-id="3d164-116">[Pixel Shader Differences](dx9-graphics-reference-asm-ps-differences.md) summarizes the differences between pixel shader versions.</span></span>

## <a name="shader-model-4-and-5-reference"></a><span data-ttu-id="3d164-117">Referenz zu Shadermodell 4 und 5</span><span class="sxs-lookup"><span data-stu-id="3d164-117">Shader Model 4 and 5 Reference</span></span>

<span data-ttu-id="3d164-118">In den Abschnitten [Shader Model 4 Assembly](dx-graphics-hlsl-sm4-asm.md) und [Shader Model 5 Assembly](shader-model-5-assembly--directx-hlsl-.md) werden die Anweisungen beschrieben, die Shader Model 4 und 5 unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3d164-118">The [Shader Model 4 Assembly](dx-graphics-hlsl-sm4-asm.md) and [Shader Model 5 Assembly](shader-model-5-assembly--directx-hlsl-.md) sections describe the instructions that shader model 4 and 5 support.</span></span>

## <a name="behavior-of-constant-registers-in-assembly-shaders"></a><span data-ttu-id="3d164-119">Verhalten konstanter Register in assemblyshader</span><span class="sxs-lookup"><span data-stu-id="3d164-119">Behavior of Constant Registers in Assembly Shaders</span></span>

<span data-ttu-id="3d164-120">Es gibt zwei Möglichkeiten, Konstante Register in einem assemblyshader festzulegen:</span><span class="sxs-lookup"><span data-stu-id="3d164-120">There are two ways to set constant registers in an assembly shader:</span></span>

-   <span data-ttu-id="3d164-121">Deklarieren Sie eine shaderkonstante in Assemblycode, indem Sie eine der DEF- \* Anweisungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="3d164-121">Declare a shader constant in assembly code using one of the def\* instructions.</span></span>
-   <span data-ttu-id="3d164-122">Verwenden Sie eine der Set \* \* \* shaderconstant \* API-Methoden.</span><span class="sxs-lookup"><span data-stu-id="3d164-122">Use one of the Set\*\*\*ShaderConstant\* API methods.</span></span>

### <a name="direct3d-9-shader-constants"></a><span data-ttu-id="3d164-123">Direct3D 9-Shader-Konstanten</span><span class="sxs-lookup"><span data-stu-id="3d164-123">Direct3D 9 Shader Constants</span></span>

<span data-ttu-id="3d164-124">In Direct3D 9 ist die Lebensdauer der definierten Konstanten in einem bestimmten Shader auf die Ausführung dieses Shaders beschränkt (und ist nicht über schreibbar).</span><span class="sxs-lookup"><span data-stu-id="3d164-124">In Direct3D 9 the lifetime of defined constants in a given shader is confined to the execution of that shader only (and is non-overridable).</span></span> <span data-ttu-id="3d164-125">Definierte Konstanten in Direct3D 9 haben keine Nebeneffekte außerhalb des Shader.</span><span class="sxs-lookup"><span data-stu-id="3d164-125">Defined constants in Direct3D 9 have no side effects outside of the shader.</span></span>

<span data-ttu-id="3d164-126">Hier ist ein Beispiel für die Verwendung von Direct3D 9:</span><span class="sxs-lookup"><span data-stu-id="3d164-126">Here's an example using Direct3D 9:</span></span>


```
Given: 
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1:
    Call Set***Shader shader1
    Call Set***ShaderConstant* to set c4
    Call Draw
    Result: The shader will see the def'd value in c4

    
Given: 
    Scenario 1 has just completed
    Create shader2 (which references c4 but does not use the def instruction
      to define it) 

Scenario 2: 
    Call Set***Shader shader2
    Call Draw
    Result: The shader will see the value last set in c4 by 
     Set***ShaderConstant* in scenario 1. This is because shader 2 
     didn't def c4.
```



<span data-ttu-id="3d164-127">In Direct3D 9 ruft der Aufruf von "get \* \* \* shaderconstant" \* nur konstante Werte ab, die über Set \* \* \* shaderconstant festgelegt werden \* .</span><span class="sxs-lookup"><span data-stu-id="3d164-127">In Direct3D 9, calling Get\*\*\*ShaderConstant\* will only retrieve constant values set via Set\*\*\*ShaderConstant\*.</span></span>

### <a name="direct3d-8-shader-constants"></a><span data-ttu-id="3d164-128">Direct3D 8-Shader-Konstanten</span><span class="sxs-lookup"><span data-stu-id="3d164-128">Direct3D 8 Shader Constants</span></span>

<span data-ttu-id="3d164-129">Dieses Verhalten unterscheidet sich in Direct3D 8. x.</span><span class="sxs-lookup"><span data-stu-id="3d164-129">This behavior is different in Direct3D 8.x.</span></span>


```
Given:
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1 (repeated with Direct3D 8):
    Call Set***Shader with shader1
    Call Set***ShaderConstant to set c4
    Call Draw
    Result: The shader will see the value in c4 from Set***ShaderConstant
```



<span data-ttu-id="3d164-130">In Direct3D 8. x wird \* \* \* shaderconstant sofort wirksam.</span><span class="sxs-lookup"><span data-stu-id="3d164-130">In Direct3D 8.x Set\*\*\*ShaderConstant takes effect immediately.</span></span> <span data-ttu-id="3d164-131">Betrachten Sie folgendes Szenario:</span><span class="sxs-lookup"><span data-stu-id="3d164-131">Consider this scenario:</span></span>


```
Given:
    Create shader1 which references c4 and defines it with the def instruction
    
Scenario 3:
    Call Set***Shader with shader1
    Call Draw
    Result: The shader will see the def'd value in c4

Given:
    Scenario 3 has just completed
    Create shader2 (which references c4 but does not use the def instruction 
      to define it)     
    
Scenario 4 :    
    Call Set***Shader with shader2
    Call Draw
    Result: The shader will see the def'd value in c4 (set by def in shader 1)
```



<span data-ttu-id="3d164-132">Das unerwünschte Ergebnis ist, dass die Reihenfolge, in der die Shader festgelegt werden, das beobachtete Verhalten einzelner Shader beeinflussen könnte.</span><span class="sxs-lookup"><span data-stu-id="3d164-132">The undesirable result is that the order in which the shaders are set could affect the observed behavior of individual shaders.</span></span>

## <a name="shader-driver-model-requirements"></a><span data-ttu-id="3d164-133">Anforderungen an das Shader-Treibermodell</span><span class="sxs-lookup"><span data-stu-id="3d164-133">Shader Driver Model Requirements</span></span>

<span data-ttu-id="3d164-134">Direct3D 9-Schnittstellen sind auf Gerätetreiber Schnittstellen-Treiber (DDI) beschränkt, die DirectX 7-Level und höher sind.</span><span class="sxs-lookup"><span data-stu-id="3d164-134">Direct3D 9 interfaces are restricted to device driver interface (DDI) drivers that are DirectX 7-level and above.</span></span> <span data-ttu-id="3d164-135">Führen Sie zum Überprüfen der DDI-Ebene das [DirectX-Diagnose Tool](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) aus, und untersuchen Sie die gespeicherte Textdatei.</span><span class="sxs-lookup"><span data-stu-id="3d164-135">To check the DDI level, run the [DirectX Diagnostic Tool](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) and examine the saved text file.</span></span>

<span data-ttu-id="3d164-136">Für den Verweis funktionieren Direct3D 8-Schnittstellen nur für DDI-Treiber, die DirectX 6-Level und höher sind.</span><span class="sxs-lookup"><span data-stu-id="3d164-136">For reference, Direct3D 8 interfaces work only on DDI drivers that are DirectX 6-level and above.</span></span>

## <a name="shader-binary-format"></a><span data-ttu-id="3d164-137">Binäres shaderformat</span><span class="sxs-lookup"><span data-stu-id="3d164-137">Shader Binary Format</span></span>

<span data-ttu-id="3d164-138">Das bitweise Layout des Shader-Anweisungs Datenstroms wird in D3d9types. h definiert.</span><span class="sxs-lookup"><span data-stu-id="3d164-138">The bitwise layout of the shader instruction stream is defined in D3d9types.h.</span></span> <span data-ttu-id="3d164-139">Wenn Sie Ihren eigenen Shader-Compiler oder die Konstruktions Tools entwerfen möchten und weitere Informationen zum Shader-Tokenstream benötigen, lesen Sie das Direct3D 9 Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="3d164-139">If you want to design your own shader compiler or construction tools and you want more information about the shader token stream, refer to the Direct3D 9 Driver Development Kit (DDK).</span></span>

## <a name="c-like-shader-language"></a><span data-ttu-id="3d164-140">C-ähnliche Shader-Sprache</span><span class="sxs-lookup"><span data-stu-id="3d164-140">C-like Shader Language</span></span>

<span data-ttu-id="3d164-141">Weitere Informationen finden Sie in der [HLSL-Referenz](dx-graphics-hlsl-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="3d164-141">See [HLSL Reference](dx-graphics-hlsl-reference.md) to experience a C-like shader language.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d164-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3d164-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d164-143">Verweis für HLSL</span><span class="sxs-lookup"><span data-stu-id="3d164-143">Reference for HLSL</span></span>](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 




