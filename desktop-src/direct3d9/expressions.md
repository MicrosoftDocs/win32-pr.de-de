---
description: Ausdrücke sind mathematische oder logische Anweisungen, die auf der rechten Seite eines Gleichheitszeichens verwendet werden. Es gibt viele Arten von Ausdrücken.
ms.assetid: 642aa188-5dd7-49fc-b6cc-845f8fc22530
title: Ausdrücke (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa574069094853eb506f7a1b38cdb6cd4379d3b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342541"
---
# <a name="expressions-direct3d-9"></a><span data-ttu-id="29f89-104">Ausdrücke (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="29f89-104">Expressions (Direct3D 9)</span></span>

<span data-ttu-id="29f89-105">Ausdrücke sind mathematische oder logische Anweisungen, die auf der rechten Seite eines Gleichheitszeichens verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29f89-105">Expressions are mathematical or logical statements that are used on the right hand side of an equals sign.</span></span> <span data-ttu-id="29f89-106">Es gibt viele Arten von Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="29f89-106">There are many types of expressions.</span></span>

## <a name="expressions"></a><span data-ttu-id="29f89-107">Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="29f89-107">Expressions</span></span>

1.  <span data-ttu-id="29f89-108">Variablen Verweis</span><span class="sxs-lookup"><span data-stu-id="29f89-108">Variable Reference</span></span>
    ```
    ( variable ) or<variable >
    ```

    

2.  <span data-ttu-id="29f89-109">Numerischer Skalar</span><span class="sxs-lookup"><span data-stu-id="29f89-109">Numeric Scalar</span></span>
    ```
    scalar 
    ```

    

3.  <span data-ttu-id="29f89-110">Numerischer Ausdruck</span><span class="sxs-lookup"><span data-stu-id="29f89-110">Numeric Expression</span></span>

    ```
    ( numeric expression )
    ```

    

    <span data-ttu-id="29f89-111">Alle standardmäßigen numerischen HLL-Ausdrücke werden hier unterstützt.</span><span class="sxs-lookup"><span data-stu-id="29f89-111">All standard numeric HLL expressions are supported here.</span></span>

4.  <span data-ttu-id="29f89-112">Konstruktor</span><span class="sxs-lookup"><span data-stu-id="29f89-112">Constructor</span></span>
    ```
    type ( constructor arguments )
    ```

    

5.  <span data-ttu-id="29f89-113">Liste der Initialisierer</span><span class="sxs-lookup"><span data-stu-id="29f89-113">List of Initializers</span></span>

    ```
    { scalar value [, scalar value ...  ] }
    
    ```

    

    <span data-ttu-id="29f89-114">Die skalare müssen literalskalare Werte sein.</span><span class="sxs-lookup"><span data-stu-id="29f89-114">The scalars must be literal scalar values.</span></span>

    <span data-ttu-id="29f89-115">Die Anzahl der Initialisierer muss mit der Variablen (State) auf der linken Seite des Gleichheitszeichens kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="29f89-115">The number of initializers must be compatible with the variable (state) on the left hand side of the equals sign.</span></span>

6.  <span data-ttu-id="29f89-116">OR-Ausdruck</span><span class="sxs-lookup"><span data-stu-id="29f89-116">OR Expression</span></span>

    ```
    token [ | token ... ]
    ```

    

    <span data-ttu-id="29f89-117">Die Token müssen mit der Variablen (State) auf der linken Seite des Gleichheitszeichens kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="29f89-117">The tokens must be compatible with the variable (state) on the left hand side of the equals sign.</span></span>

    <span data-ttu-id="29f89-118">Beim Token wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="29f89-118">The tokens are not case sensitive.</span></span>

7.  <span data-ttu-id="29f89-119">NULL</span><span class="sxs-lookup"><span data-stu-id="29f89-119">NULL</span></span>

    ```
    NULL
    ```

    

    <span data-ttu-id="29f89-120">NULL kann nur einem Shader, einem Sampler oder einem Textur Objekt zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="29f89-120">NULL can only be assigned to a shader, sampler, or a texture object.</span></span>

8.  <span data-ttu-id="29f89-121">Assemblyblock</span><span class="sxs-lookup"><span data-stu-id="29f89-121">Assembly Block</span></span>

    ```
    asm { code }
    ```

    

    <span data-ttu-id="29f89-122">PS-assemblyblöcke müssen dem Pixelshader-Zustand zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="29f89-122">PS Assembly Blocks must be assigned to the PIXELSHADER state.</span></span>

    <span data-ttu-id="29f89-123">VS-assemblyblöcke müssen dem Vertexshader-Zustand zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="29f89-123">VS Assembly Blocks must be assigned to the VERTEXSHADER state.</span></span>

9.  <span data-ttu-id="29f89-124">Sampler-Zustands Block</span><span class="sxs-lookup"><span data-stu-id="29f89-124">Sampler State Block</span></span>

    ```
    sampler_state { [ state = expression ; [ state = ... ] ] }
    ```

    

    <span data-ttu-id="29f89-125">Samplerstatusblöcke sind Sequenzen von nicht indizierten samplingstatus-oder Textur Zuweisungen.</span><span class="sxs-lookup"><span data-stu-id="29f89-125">Sampler state blocks are sequences of un-indexed sampler stage state or texture assignments.</span></span>

    <span data-ttu-id="29f89-126">Samplerstatusblöcke müssen dem samplereffekts-Zustand zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="29f89-126">Sampler state blocks must be assigned to the SAMPLER effect state.</span></span>

10. <span data-ttu-id="29f89-127">Zustands Block des Effekt Zustands</span><span class="sxs-lookup"><span data-stu-id="29f89-127">Effect State State Block</span></span>

    ```
    stateblock_state { [ state [ [index] ] = expression; 
        [ state [ [index] ] = ... ] ] }
    ```

    

    <span data-ttu-id="29f89-128">Zustands Blöcke sind Sequenzen des allgemeinen Zustands.</span><span class="sxs-lookup"><span data-stu-id="29f89-128">State blocks are sequences of general state.</span></span> <span data-ttu-id="29f89-129">Zustands Blöcke können eingebettet werden, aber keine Zirkel Verweise enthalten.</span><span class="sxs-lookup"><span data-stu-id="29f89-129">State blocks can be nested, but cannot contain circular references.</span></span>

    <span data-ttu-id="29f89-130">Zustands Blöcke müssen dem Status des stateblock-Effekts zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="29f89-130">State blocks must be assigned to the STATEBLOCK effect state.</span></span>

11. <span data-ttu-id="29f89-131">HLSL-Kompilierung</span><span class="sxs-lookup"><span data-stu-id="29f89-131">HLSL Compile</span></span>

    ```
    compile target entrypoint ( [ arguments ] )
    ```

    

    <span data-ttu-id="29f89-132">Der Vertex-Shader im Vergleich zu \_ m \_ n-Ziel gibt die \_ Vertexshader-Version von D3DVS Version (m, n) an.</span><span class="sxs-lookup"><span data-stu-id="29f89-132">The vertex shader vs\_m\_n target indicates D3DVS\_VERSION(m, n) vertex shader version.</span></span> <span data-ttu-id="29f89-133">Das Pixel-Shader PS \_ m \_ n-Ziel gibt die Pixel- \_ Shader-Version von D3DPS Version (m, n) an.</span><span class="sxs-lookup"><span data-stu-id="29f89-133">The pixel shader ps\_m\_n target indicates D3DPS\_VERSION(m, n) pixel shader version.</span></span>

    <span data-ttu-id="29f89-134">Die sprach Kompilierungs Ausdrücke auf hoher Ebene des Vertex-Shaders können nur dem Vertexshader-Effekt Zustand zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="29f89-134">Vertex shader high-level language compile expressions can only be assigned to the VERTEXSHADER effect state.</span></span> <span data-ttu-id="29f89-135">Der Pixel-Shader auf hoher Ebene kompilierte sprach Kompilierungs Ausdrücke können nur dem Pixelshader-Effekt Zustand zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="29f89-135">Pixel shader high-level language compile expressions can only be assigned to the PIXELSHADER effect state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29f89-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="29f89-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29f89-137">Effekt Format</span><span class="sxs-lookup"><span data-stu-id="29f89-137">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



