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
ms.openlocfilehash: 847194c08b865542cff1deb20c8518a7e4b62ab9
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119045"
---
# <a name="function-declaration-syntax"></a><span data-ttu-id="b380c-103">Syntax der Funktionsdeklaration</span><span class="sxs-lookup"><span data-stu-id="b380c-103">Function Declaration Syntax</span></span>

<span data-ttu-id="b380c-104">HLSL-Funktionen werden mit der folgenden Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="b380c-104">HLSL functions are declared with the following syntax.</span></span>

<span data-ttu-id="b380c-105">\[*StorageClass* \] \[clipplanes() \] \[ precise \] Return Value \_ *Name* ( \[ *ArgumentList* \] ) : \[ *Semantic* \] { \[ *StatementBlock* \] };</span><span class="sxs-lookup"><span data-stu-id="b380c-105">\[*StorageClass*\] \[clipplanes()\] \[precise\] Return\_Value *Name* ( \[*ArgumentList*\] ) \[: *Semantic*\] {   \[*StatementBlock*\] };</span></span>



 

## <a name="parameters"></a><span data-ttu-id="b380c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b380c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b380c-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*</span><span class="sxs-lookup"><span data-stu-id="b380c-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*</span></span>
</dt> <dd>

<span data-ttu-id="b380c-108">Modifizierer, der eine Funktionsdeklaration neu definiert.</span><span class="sxs-lookup"><span data-stu-id="b380c-108">Modifier that redefines a function declaration.</span></span> <span data-ttu-id="b380c-109">**Inline** ist derzeit der einzige Modifiziererwert.</span><span class="sxs-lookup"><span data-stu-id="b380c-109">**inline** is currently the only modifier value.</span></span> <span data-ttu-id="b380c-110">Der Modifiziererwert muss **inline** sein, da er auch der Standardwert ist.</span><span class="sxs-lookup"><span data-stu-id="b380c-110">The modifier value must be **inline** because it is also the default value.</span></span> <span data-ttu-id="b380c-111">Daher ist eine Funktion inline, unabhängig davon, ob Sie **inline** angeben und alle Funktionen in HLSL inline sind.</span><span class="sxs-lookup"><span data-stu-id="b380c-111">Therefore, a function is inline regardless of whether you specify **inline**, and all functions in HLSL are inline.</span></span> <span data-ttu-id="b380c-112">Eine Inlinefunktion generiert eine Kopie des Funktionstexts (beim Kompilieren) für jeden Funktionsaufruf.</span><span class="sxs-lookup"><span data-stu-id="b380c-112">An inline function generates a copy of the function body (when compiling) for each function call.</span></span> <span data-ttu-id="b380c-113">Dies wird durchgeführt, um den Mehraufwand für den Aufruf der Funktion zu verringern.</span><span class="sxs-lookup"><span data-stu-id="b380c-113">This is done to decrease the overhead of calling the function.</span></span>

</dd> <dt>

<span data-ttu-id="b380c-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*</span><span class="sxs-lookup"><span data-stu-id="b380c-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*</span></span>
</dt> <dd>

<span data-ttu-id="b380c-115">Optionale Liste der Clipebenen, d. h. bis zu 6 benutzerdefinierte Clipebenen.</span><span class="sxs-lookup"><span data-stu-id="b380c-115">Optional list of clip planes, which is up to 6 user-specified clip planes.</span></span> <span data-ttu-id="b380c-116">Dies ist ein alternativer Mechanismus für [SV \_ ClipDistance,](dx-graphics-hlsl-semantics.md) der auf [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x und höher funktioniert.</span><span class="sxs-lookup"><span data-stu-id="b380c-116">This is an alternate mechanism for [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) that works on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span>

</dd> <dt>

<span data-ttu-id="b380c-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Namen*</span><span class="sxs-lookup"><span data-stu-id="b380c-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="b380c-118">Eine ASCII-Zeichenfolge, die den Namen der Shaderfunktion eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b380c-118">An ASCII string that uniquely identifies the name of the shader function.</span></span>

</dd> <dt>

<span data-ttu-id="b380c-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*Argumentlist*</span><span class="sxs-lookup"><span data-stu-id="b380c-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*</span></span>
</dt> <dd>

<span data-ttu-id="b380c-120">Optionale Argumentliste, bei der es sich um eine durch Kommas getrennte Liste von [Argumenten](dx-graphics-hlsl-function-parameters.md) handelt, die an eine Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="b380c-120">Optional argument list, which is a comma-separated list of [arguments](dx-graphics-hlsl-function-parameters.md) passed into a function.</span></span>

</dd> <dt>

<span data-ttu-id="b380c-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantische*</span><span class="sxs-lookup"><span data-stu-id="b380c-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="b380c-122">Optionale Zeichenfolge, die die beabsichtigte Verwendung der Rückgabedaten angibt (siehe [Semantik (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span><span class="sxs-lookup"><span data-stu-id="b380c-122">Optional string that identifies the intended usage of the return data (see [Semantics (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span></span>

</dd> <dt>

<span data-ttu-id="b380c-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span><span class="sxs-lookup"><span data-stu-id="b380c-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span></span>
</dt> <dd>

<span data-ttu-id="b380c-124">Optionale [Anweisungen,](dx-graphics-hlsl-statement-blocks.md) die den Textkörper der Funktion bilden.</span><span class="sxs-lookup"><span data-stu-id="b380c-124">Optional [statements](dx-graphics-hlsl-statement-blocks.md) that make up the body of the function.</span></span> <span data-ttu-id="b380c-125">Eine Funktion, die ohne Text definiert ist, wird als Funktionsprototyp bezeichnet. Der Text einer Prototypfunktion muss an anderer Stelle definiert werden, bevor die Funktion aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b380c-125">A function defined without a body is called a function prototype; the body of a prototype function must be defined elsewhere before the function can be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b380c-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b380c-126">Return Value</span></span>

<span data-ttu-id="b380c-127">Der Rückgabetyp kann einer dieser [HLSL-Typen](dx-graphics-hlsl-data-types.md)sein.</span><span class="sxs-lookup"><span data-stu-id="b380c-127">The return type can be any one of these [HLSL types](dx-graphics-hlsl-data-types.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b380c-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b380c-128">Remarks</span></span>

<span data-ttu-id="b380c-129">Die Syntax auf dieser Seite beschreibt fast jeden Typ von HLSL-Funktion. Dazu gehören Vertex-Shader, Pixel-Shader und Hilfsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="b380c-129">The syntax on this page describes almost every type of HLSL function, this includes vertex shaders, pixel shaders, and helper functions.</span></span> <span data-ttu-id="b380c-130">Während ein geometriebasierter Shader auch mit einer Funktion implementiert wird, ist seine Syntax etwas komplizierter, sodass es eine separate Seite gibt, die eine Deklaration einer [Geometry-Shader-Funktion definiert (siehe Geometry-Shader-Objekt (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="b380c-130">While a geometry shader is also implemented with a function, its syntax is a little more complicated, so there is a separate page that defines a geometry shader function declaration (see [Geometry-Shader Object (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).</span></span>

<span data-ttu-id="b380c-131">Eine Funktion kann überladen werden, solange sie eine eindeutige Kombination aus Parametertypen und/oder Parameterreihenfolge erhält.</span><span class="sxs-lookup"><span data-stu-id="b380c-131">A function can be overloaded as long as it is given a unique combination of parameter types and/or parameter order.</span></span> <span data-ttu-id="b380c-132">HLSL implementiert auch eine Reihe von integrierten oder [**intrinsischen Funktionen.**](dx-graphics-hlsl-intrinsic-functions.md)</span><span class="sxs-lookup"><span data-stu-id="b380c-132">HLSL also implements a number of built in, or [**intrinsic functions**](dx-graphics-hlsl-intrinsic-functions.md).</span></span>

<span data-ttu-id="b380c-133">Sie können benutzerspezifische Clipebenen mit dem **Clipplanes-Attribut** angeben.</span><span class="sxs-lookup"><span data-stu-id="b380c-133">You can specify user-specific clip planes with the **clipplanes** attribute.</span></span> <span data-ttu-id="b380c-134">Windows wendet diese Clipebenen auf alle gezeichneten Primitive an.</span><span class="sxs-lookup"><span data-stu-id="b380c-134">Windows applies these clip planes to all of the primitives drawn.</span></span> <span data-ttu-id="b380c-135">Das **Clipplanes-Attribut** funktioniert wie [SV \_ ClipDistance,](dx-graphics-hlsl-semantics.md) funktioniert jedoch auf allen [Hardwarefeatureebenen](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x und höher.</span><span class="sxs-lookup"><span data-stu-id="b380c-135">The **clipplanes** attribute works like [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) but works on all hardware [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span> <span data-ttu-id="b380c-136">Weitere Informationen finden Sie unter [User clip planes on feature level 9 hardware (Benutzer clip planes on feature level 9 hardware ( Benutzer clip planes on feature level 9 hardware](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9)).</span><span class="sxs-lookup"><span data-stu-id="b380c-136">For more info, see [User clip planes on feature level 9 hardware](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).</span></span>

## <a name="examples"></a><span data-ttu-id="b380c-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b380c-137">Examples</span></span>

<span data-ttu-id="b380c-138">Dieses Beispiel stammt aus BasicHLSL10.fx aus dem [BasicHLSL10-Beispiel.](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="b380c-138">This example is from BasicHLSL10.fx from the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span></span>


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



<span data-ttu-id="b380c-139">Dieses Beispiel aus AdvancedParticles.fx aus dem [AdvancedParticles-Beispiel](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)veranschaulicht die Verwendung einer Semantik für den Rückgabetyp.</span><span class="sxs-lookup"><span data-stu-id="b380c-139">This example from AdvancedParticles.fx from the [AdvancedParticles Sample](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx), illustrates using a semantic for the return type.</span></span>


```hlsl
//
// PS for particles
//
float4 PSPointSprite(PSSceneIn input) : SV_Target
{   
    return g_txDiffuse.Sample( g_samLinear, input.tex ) * input.color;
}
```



## <a name="related-topics"></a><span data-ttu-id="b380c-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b380c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b380c-141">Funktionen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b380c-141">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 
