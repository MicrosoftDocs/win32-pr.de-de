---
description: Eine Effekt Funktion wird in HLSL geschrieben und mit der folgenden Syntax deklariert.
ms.assetid: 5ac85f09-50ac-4e8f-b4d2-ae8306b59348
title: Effekt Funktions Syntax (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88521eeb85d1e5f54500a045fe5dcfd81d6be2cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483198"
---
# <a name="effect-function-syntax-direct3d-10"></a><span data-ttu-id="95f17-103">Effekt Funktions Syntax (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="95f17-103">Effect Function Syntax (Direct3D 10)</span></span>

<span data-ttu-id="95f17-104">Eine Effekt Funktion wird in HLSL geschrieben und mit der folgenden Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="95f17-104">An effect function is written in HLSL and is declared with the following syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="95f17-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="95f17-105">Syntax</span></span>

<span data-ttu-id="95f17-106">*ReturnType* *FunctionName* (Argument \[ *List* \] )</span><span class="sxs-lookup"><span data-stu-id="95f17-106">*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )</span></span>

<span data-ttu-id="95f17-107">{</span><span class="sxs-lookup"><span data-stu-id="95f17-107">{</span></span>

<dl> <span data-ttu-id="95f17-108">\[ *Anweisungen* \]</span><span class="sxs-lookup"><span data-stu-id="95f17-108">\[ *Statements* \]</span></span>
</dl>

<span data-ttu-id="95f17-109">};</span><span class="sxs-lookup"><span data-stu-id="95f17-109">};</span></span>



| <span data-ttu-id="95f17-110">Name</span><span class="sxs-lookup"><span data-stu-id="95f17-110">Name</span></span>         | <span data-ttu-id="95f17-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95f17-111">Description</span></span>                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95f17-112">ReturnType</span><span class="sxs-lookup"><span data-stu-id="95f17-112">ReturnType</span></span>   | <span data-ttu-id="95f17-113">Beliebiger [HLSL-Typ](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)</span><span class="sxs-lookup"><span data-stu-id="95f17-113">Any [HLSL type](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="95f17-114">FunctionName</span><span class="sxs-lookup"><span data-stu-id="95f17-114">FunctionName</span></span> | <span data-ttu-id="95f17-115">Eine ASCII-Zeichenfolge, die den Namen der Shader-Funktion eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="95f17-115">An ASCII string that uniquely identifies the name of the shader function.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="95f17-116">Argument List</span><span class="sxs-lookup"><span data-stu-id="95f17-116">ArgumentList</span></span> | <span data-ttu-id="95f17-117">Mindestens ein durch Kommas getrenntes Argument (siehe [Funktionsargumente (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="95f17-117">One or more arguments, separated by commas (see [Function Arguments (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)).</span></span>                                                                                                                             |
| <span data-ttu-id="95f17-118">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="95f17-118">Statements</span></span>   | <span data-ttu-id="95f17-119">Mindestens eine-Anweisung (siehe [Anweisungen (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-statements.md)), die den Hauptteil der Funktion bilden.</span><span class="sxs-lookup"><span data-stu-id="95f17-119">One or more statements (see [Statements (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-statements.md)) that make up the body of the function.</span></span> <span data-ttu-id="95f17-120">Wenn eine Funktion ohne Text definiert ist, wird Sie als Prototyp betrachtet. und müssen vor der Verwendung mit einem Text neu definiert werden.</span><span class="sxs-lookup"><span data-stu-id="95f17-120">If a function is defined without a body, it is considered to be a prototype; and must be redefined with a body before use.</span></span> |



 

<span data-ttu-id="95f17-121">Eine Effekt Funktion kann ein Shader sein, oder es kann sich einfach um eine Funktion handeln, die von einem Shader aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="95f17-121">An effect function may be a shader or it may simply be a function called by a shader.</span></span> <span data-ttu-id="95f17-122">Eine Funktion wird durch ihren Namen, die Typen ihrer Parameter und die Zielplattform eindeutig identifiziert. Daher können Funktionen überladen werden.</span><span class="sxs-lookup"><span data-stu-id="95f17-122">A function is uniquely identified by its name, the types of its parameters, and the target platform; therefore, functions can be overloaded.</span></span> <span data-ttu-id="95f17-123">Jede gültige HLSL-Funktion sollte diesem Format entsprechen. eine ausführlichere Liste der Syntax für HLSL-Funktionen finden Sie unter [Functions (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-functions.md).</span><span class="sxs-lookup"><span data-stu-id="95f17-123">Any valid HLSL function should fit this format; for a more detailed list of syntax for HLSL functions, see [Functions (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-functions.md).</span></span>

## <a name="example"></a><span data-ttu-id="95f17-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="95f17-124">Example</span></span>

<span data-ttu-id="95f17-125">Das [BasicHLSL10-Beispiel](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) verwendet einen Pixel-Shader und einen Vertex-Shader.</span><span class="sxs-lookup"><span data-stu-id="95f17-125">The [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) uses both a pixel shader and a vertex shader.</span></span> <span data-ttu-id="95f17-126">Die Pixel-Shader-Funktion heißt rendersceneps und ist unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="95f17-126">The pixel shader function is called RenderScenePS and is shown below.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="95f17-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="95f17-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95f17-128">Effekt Format</span><span class="sxs-lookup"><span data-stu-id="95f17-128">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 
