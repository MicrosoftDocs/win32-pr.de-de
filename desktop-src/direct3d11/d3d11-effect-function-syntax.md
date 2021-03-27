---
title: Effekt Funktions Syntax (Direct3D 11)
description: Eine Effekt Funktion ist in HLSL geschrieben und wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.
ms.assetid: 5e12ba65-98bf-4f21-be75-602687157eb1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f569211d5f178b96cf7415478010285e7a836b58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727377"
---
# <a name="effect-function-syntax-direct3d-11"></a><span data-ttu-id="6a6e8-103">Effekt Funktions Syntax (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="6a6e8-103">Effect Function Syntax (Direct3D 11)</span></span>

<span data-ttu-id="6a6e8-104">Eine Effekt Funktion ist in HLSL geschrieben und wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="6a6e8-104">An effect function is written in HLSL and is declared with the syntax described in this section.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a6e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a6e8-105">Syntax</span></span>

<span data-ttu-id="6a6e8-106">*ReturnType* *FunctionName* (Argument \[ *List* \] )</span><span class="sxs-lookup"><span data-stu-id="6a6e8-106">*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )</span></span>

<span data-ttu-id="6a6e8-107">{</span><span class="sxs-lookup"><span data-stu-id="6a6e8-107">{</span></span>

<dl> <span data-ttu-id="6a6e8-108">\[ *Anweisungen* \]</span><span class="sxs-lookup"><span data-stu-id="6a6e8-108">\[ *Statements* \]</span></span>
</dl>

<span data-ttu-id="6a6e8-109">};</span><span class="sxs-lookup"><span data-stu-id="6a6e8-109">};</span></span>



| <span data-ttu-id="6a6e8-110">Name</span><span class="sxs-lookup"><span data-stu-id="6a6e8-110">Name</span></span>         | <span data-ttu-id="6a6e8-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a6e8-111">Description</span></span>                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a6e8-112">ReturnType</span><span class="sxs-lookup"><span data-stu-id="6a6e8-112">ReturnType</span></span>   | <span data-ttu-id="6a6e8-113">Beliebiger [HLSL-Typ](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)</span><span class="sxs-lookup"><span data-stu-id="6a6e8-113">Any [HLSL type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="6a6e8-114">FunctionName</span><span class="sxs-lookup"><span data-stu-id="6a6e8-114">FunctionName</span></span> | <span data-ttu-id="6a6e8-115">Eine ASCII-Zeichenfolge, die den Namen der Shader-Funktion eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6a6e8-115">An ASCII string that uniquely identifies the name of the shader function.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="6a6e8-116">Argument List</span><span class="sxs-lookup"><span data-stu-id="6a6e8-116">ArgumentList</span></span> | <span data-ttu-id="6a6e8-117">Mindestens ein durch Kommas getrenntes Argument (siehe [Funktionsargumente (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).</span><span class="sxs-lookup"><span data-stu-id="6a6e8-117">One or more arguments, separated by commas (see [Function Arguments (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).</span></span>                                                                                                                             |
| <span data-ttu-id="6a6e8-118">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="6a6e8-118">Statements</span></span>   | <span data-ttu-id="6a6e8-119">Mindestens eine-Anweisung (siehe [Anweisungen (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)), die den Hauptteil der Funktion bilden.</span><span class="sxs-lookup"><span data-stu-id="6a6e8-119">One or more statements (see [Statements (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)) that make up the body of the function.</span></span> <span data-ttu-id="6a6e8-120">Wenn eine Funktion ohne Text definiert ist, wird Sie als Prototyp betrachtet. und müssen vor der Verwendung mit einem Text neu definiert werden.</span><span class="sxs-lookup"><span data-stu-id="6a6e8-120">If a function is defined without a body, it is considered to be a prototype; and must be redefined with a body before use.</span></span> |



 

<span data-ttu-id="6a6e8-121">Eine Effekt Funktion kann ein Shader sein, oder es kann sich einfach um eine Funktion handeln, die von einem Shader aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6a6e8-121">An effect function may be a shader or it may simply be a function called by a shader.</span></span> <span data-ttu-id="6a6e8-122">Eine Funktion wird durch ihren Namen, die Typen ihrer Parameter und die Zielplattform eindeutig identifiziert. Daher können Funktionen überladen werden.</span><span class="sxs-lookup"><span data-stu-id="6a6e8-122">A function is uniquely identified by its name, the types of its parameters, and the target platform; therefore, functions can be overloaded.</span></span> <span data-ttu-id="6a6e8-123">Jede gültige HLSL-Funktion sollte diesem Format entsprechen. eine ausführlichere Liste der Syntax für HLSL-Funktionen finden Sie unter [Functions (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).</span><span class="sxs-lookup"><span data-stu-id="6a6e8-123">Any valid HLSL function should fit this format; for a more detailed list of syntax for HLSL functions, see [Functions (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).</span></span>

## <a name="example"></a><span data-ttu-id="6a6e8-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6a6e8-124">Example</span></span>

<span data-ttu-id="6a6e8-125">Im folgenden finden Sie ein Beispiel für eine Pixel-Shader-Funktion.</span><span class="sxs-lookup"><span data-stu-id="6a6e8-125">The following is an example of a pixel shader function.</span></span>


```
       
PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    // Lookup mesh texture and modulate it with diffuse
    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) *  
                              In.Diffuse;
    else
        Output.RGBColor = In.Diffuse;

    return Output;
}
```



## <a name="related-topics"></a><span data-ttu-id="6a6e8-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6a6e8-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a6e8-127">Effekt Format</span><span class="sxs-lookup"><span data-stu-id="6a6e8-127">Effect Format</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 