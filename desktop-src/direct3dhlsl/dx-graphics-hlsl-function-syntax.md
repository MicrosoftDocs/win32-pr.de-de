---
title: Syntax der Funktionsdeklaration
description: HLSL-Funktionen werden mit der folgenden Syntax deklariert.
ms.assetid: f8968de2-7b2d-4a2e-8312-cec5b652f700
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2781d173eb4a1c18a661495d9fb55a0cced81921
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998327"
---
# <a name="function-declaration-syntax"></a><span data-ttu-id="00a1d-103">Syntax der Funktionsdeklaration</span><span class="sxs-lookup"><span data-stu-id="00a1d-103">Function Declaration Syntax</span></span>

<span data-ttu-id="00a1d-104">HLSL-Funktionen werden mit der folgenden Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="00a1d-104">HLSL functions are declared with the following syntax.</span></span>



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00a1d-105">\[*StorageClass* \] \[clipplanes() \] \[ precise \] Return Value \_ *Name* ( \[ *ArgumentList* \] ) : \[ *Semantic* \] { \[ *StatementBlock* \] };</span><span class="sxs-lookup"><span data-stu-id="00a1d-105">\[*StorageClass*\] \[clipplanes()\] \[precise\] Return\_Value *Name* ( \[*ArgumentList*\] ) \[: *Semantic*\] {   \[*StatementBlock*\] };</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="00a1d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="00a1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00a1d-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*</span><span class="sxs-lookup"><span data-stu-id="00a1d-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*</span></span>
</dt> <dd>

<span data-ttu-id="00a1d-108">Modifizierer, der eine Funktionsdeklaration neu definiert.</span><span class="sxs-lookup"><span data-stu-id="00a1d-108">Modifier that redefines a function declaration.</span></span> <span data-ttu-id="00a1d-109">**Inline** ist derzeit der einzige Modifiziererwert.</span><span class="sxs-lookup"><span data-stu-id="00a1d-109">**inline** is currently the only modifier value.</span></span> <span data-ttu-id="00a1d-110">Der Modifiziererwert muss **inline** sein, da er auch der Standardwert ist.</span><span class="sxs-lookup"><span data-stu-id="00a1d-110">The modifier value must be **inline** because it is also the default value.</span></span> <span data-ttu-id="00a1d-111">Daher ist eine Funktion inline, unabhängig davon, ob Sie **inline** angeben, und alle Funktionen in HLSL sind inline.</span><span class="sxs-lookup"><span data-stu-id="00a1d-111">Therefore, a function is inline regardless of whether you specify **inline**, and all functions in HLSL are inline.</span></span> <span data-ttu-id="00a1d-112">Eine Inlinefunktion generiert eine Kopie des Funktionstexts (beim Kompilieren) für jeden Funktionsaufruf.</span><span class="sxs-lookup"><span data-stu-id="00a1d-112">An inline function generates a copy of the function body (when compiling) for each function call.</span></span> <span data-ttu-id="00a1d-113">Dies wird durchgeführt, um den Mehraufwand für den Aufruf der Funktion zu verringern.</span><span class="sxs-lookup"><span data-stu-id="00a1d-113">This is done to decrease the overhead of calling the function.</span></span>

</dd> <dt>

<span data-ttu-id="00a1d-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*</span><span class="sxs-lookup"><span data-stu-id="00a1d-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*</span></span>
</dt> <dd>

<span data-ttu-id="00a1d-115">Optionale Liste der Clipebenen, d. h. bis zu sechs benutzerdefinierte Clipebenen.</span><span class="sxs-lookup"><span data-stu-id="00a1d-115">Optional list of clip planes, which is up to 6 user-specified clip planes.</span></span> <span data-ttu-id="00a1d-116">Dies ist ein alternativer Mechanismus für [SV \_ ClipDistance,](dx-graphics-hlsl-semantics.md) der auf [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x und höher funktioniert.</span><span class="sxs-lookup"><span data-stu-id="00a1d-116">This is an alternate mechanism for [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) that works on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span>

</dd> <dt>

<span data-ttu-id="00a1d-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Namen*</span><span class="sxs-lookup"><span data-stu-id="00a1d-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="00a1d-118">Eine ASCII-Zeichenfolge, die den Namen der Shaderfunktion eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="00a1d-118">An ASCII string that uniquely identifies the name of the shader function.</span></span>

</dd> <dt>

<span data-ttu-id="00a1d-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*Argumentlist*</span><span class="sxs-lookup"><span data-stu-id="00a1d-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*</span></span>
</dt> <dd>

<span data-ttu-id="00a1d-120">Optionale Argumentliste, bei der es sich um eine durch Kommas getrennte Liste von [Argumenten](dx-graphics-hlsl-function-parameters.md) handelt, die an eine Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="00a1d-120">Optional argument list, which is a comma-separated list of [arguments](dx-graphics-hlsl-function-parameters.md) passed into a function.</span></span>

</dd> <dt>

<span data-ttu-id="00a1d-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantische*</span><span class="sxs-lookup"><span data-stu-id="00a1d-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="00a1d-122">Optionale Zeichenfolge, die die beabsichtigte Verwendung der Rückgabedaten angibt (siehe [Semantik (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span><span class="sxs-lookup"><span data-stu-id="00a1d-122">Optional string that identifies the intended usage of the return data (see [Semantics (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span></span>

</dd> <dt>

<span data-ttu-id="00a1d-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span><span class="sxs-lookup"><span data-stu-id="00a1d-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span></span>
</dt> <dd>

<span data-ttu-id="00a1d-124">Optionale [Anweisungen,](dx-graphics-hlsl-statement-blocks.md) die den Text der Funktion enthalten.</span><span class="sxs-lookup"><span data-stu-id="00a1d-124">Optional [statements](dx-graphics-hlsl-statement-blocks.md) that make up the body of the function.</span></span> <span data-ttu-id="00a1d-125">Eine Funktion, die ohne Text definiert ist, wird als Funktionsprototyp bezeichnet. Der Text einer Prototypfunktion muss an anderer Stelle definiert werden, bevor die Funktion aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="00a1d-125">A function defined without a body is called a function prototype; the body of a prototype function must be defined elsewhere before the function can be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00a1d-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00a1d-126">Return Value</span></span>

<span data-ttu-id="00a1d-127">Der Rückgabetyp kann einer dieser [HLSL-Typen sein.](dx-graphics-hlsl-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="00a1d-127">The return type can be any one of these [HLSL types](dx-graphics-hlsl-data-types.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="00a1d-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="00a1d-128">Remarks</span></span>

<span data-ttu-id="00a1d-129">Die Syntax auf dieser Seite beschreibt fast jeden Typ von HLSL-Funktion, einschließlich Vertex-Shadern, Pixel-Shadern und Hilfsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="00a1d-129">The syntax on this page describes almost every type of HLSL function, this includes vertex shaders, pixel shaders, and helper functions.</span></span> <span data-ttu-id="00a1d-130">Während ein Geometrie-Shader auch mit einer Funktion implementiert wird, ist seine Syntax etwas komplizierter, sodass es eine separate Seite gibt, die eine Deklaration einer Geometrie-Shaderfunktion definiert (siehe [Geometry-Shader Object (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="00a1d-130">While a geometry shader is also implemented with a function, its syntax is a little more complicated, so there is a separate page that defines a geometry shader function declaration (see [Geometry-Shader Object (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).</span></span>

<span data-ttu-id="00a1d-131">Eine Funktion kann überladen werden, solange sie eine eindeutige Kombination aus Parametertypen und/oder Parameter reihenfolge erhält.</span><span class="sxs-lookup"><span data-stu-id="00a1d-131">A function can be overloaded as long as it is given a unique combination of parameter types and/or parameter order.</span></span> <span data-ttu-id="00a1d-132">HLSL implementiert auch eine Reihe von integrierten oder [**systeminternen Funktionen.**](dx-graphics-hlsl-intrinsic-functions.md)</span><span class="sxs-lookup"><span data-stu-id="00a1d-132">HLSL also implements a number of built in, or [**intrinsic functions**](dx-graphics-hlsl-intrinsic-functions.md).</span></span>

<span data-ttu-id="00a1d-133">Sie können benutzerspezifische Clipebenen mit dem **Clipplanes-Attribut** angeben.</span><span class="sxs-lookup"><span data-stu-id="00a1d-133">You can specify user-specific clip planes with the **clipplanes** attribute.</span></span> <span data-ttu-id="00a1d-134">Windows wendet diese Clipebenen auf alle gezeichneten Primitive an.</span><span class="sxs-lookup"><span data-stu-id="00a1d-134">Windows applies these clip planes to all of the primitives drawn.</span></span> <span data-ttu-id="00a1d-135">Das **Clipplanes-Attribut** funktioniert wie [SV \_ ClipDistance,](dx-graphics-hlsl-semantics.md) funktioniert jedoch auf allen Hardwarefeatures [der](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Ebene 9 x \_ und höher.</span><span class="sxs-lookup"><span data-stu-id="00a1d-135">The **clipplanes** attribute works like [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) but works on all hardware [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span> <span data-ttu-id="00a1d-136">Weitere Informationen finden Sie unter User clip planes on feature level 9 hardware (Benutzeroberflächenebenen auf Hardware [auf Featureebene 9).](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9)</span><span class="sxs-lookup"><span data-stu-id="00a1d-136">For more info, see [User clip planes on feature level 9 hardware](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).</span></span>

## <a name="examples"></a><span data-ttu-id="00a1d-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00a1d-137">Examples</span></span>

<span data-ttu-id="00a1d-138">Dieses Beispiel ist von BasicHLSL10.fx aus dem [BasicHLSL10-Beispiel .](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="00a1d-138">This example is from BasicHLSL10.fx from the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span></span>


```hlsl
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; 
    float4 Diffuse    : COLOR0;
    float2 TextureUV  : TEXCOORD0;
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    ...
    return Output;    
}
```



<span data-ttu-id="00a1d-139">Dieses Beispiel aus AdvancedParticles.fx aus [dem AdvancedParticles-Beispiel](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)veranschaulicht die Verwendung einer Semantik für den Rückgabetyp.</span><span class="sxs-lookup"><span data-stu-id="00a1d-139">This example from AdvancedParticles.fx from the [AdvancedParticles Sample](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx), illustrates using a semantic for the return type.</span></span>


```hlsl
//
// PS for particles
//
float4 PSPointSprite(PSSceneIn input) : SV_Target
{   
    return g_txDiffuse.Sample( g_samLinear, input.tex ) * input.color;
}
```



## <a name="related-topics"></a><span data-ttu-id="00a1d-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="00a1d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00a1d-141">Funktionen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="00a1d-141">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 
