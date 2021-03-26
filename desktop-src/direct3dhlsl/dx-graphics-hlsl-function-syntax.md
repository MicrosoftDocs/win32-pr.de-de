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
ms.openlocfilehash: 7358a59dba0096f5c8ffe58072a974ebff9a1050
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390862"
---
# <a name="function-declaration-syntax"></a><span data-ttu-id="6f0f9-103">Syntax der Funktionsdeklaration</span><span class="sxs-lookup"><span data-stu-id="6f0f9-103">Function Declaration Syntax</span></span>

<span data-ttu-id="6f0f9-104">HLSL-Funktionen werden mit der folgenden Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-104">HLSL functions are declared with the following syntax.</span></span>



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f0f9-105">\[*Storageclass* \] \[clipplane () \] \[ präziser \] Rückgabe \_ Wert *Name* (Argument \[ *List* \] ) \[ : *Semantik* \] { \[ *Status Block* \] };</span><span class="sxs-lookup"><span data-stu-id="6f0f9-105">\[*StorageClass*\] \[clipplanes()\] \[precise\] Return\_Value *Name* ( \[*ArgumentList*\] ) \[: *Semantic*\] {   \[*StatementBlock*\] };</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="6f0f9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f0f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f0f9-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*Storageclass*</span><span class="sxs-lookup"><span data-stu-id="6f0f9-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*</span></span>
</dt> <dd>

<span data-ttu-id="6f0f9-108">Ein Modifizierer, der eine Funktionsdeklaration neu definiert.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-108">Modifier that redefines a function declaration.</span></span> <span data-ttu-id="6f0f9-109">**Inline** ist zurzeit der einzige Modifiziererwert.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-109">**inline** is currently the only modifier value.</span></span> <span data-ttu-id="6f0f9-110">Der Modifiziererwert muss **Inline** sein, da er auch der Standardwert ist.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-110">The modifier value must be **inline** because it is also the default value.</span></span> <span data-ttu-id="6f0f9-111">Daher ist eine Funktion Inline, unabhängig davon, ob Sie **Inline** angeben und alle Funktionen in HLSL Inline sind.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-111">Therefore, a function is inline regardless of whether you specify **inline**, and all functions in HLSL are inline.</span></span> <span data-ttu-id="6f0f9-112">Eine Inline Funktion generiert eine Kopie des Funktions Texts (beim Kompilieren) für jeden Funktions Aufruf.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-112">An inline function generates a copy of the function body (when compiling) for each function call.</span></span> <span data-ttu-id="6f0f9-113">Dies geschieht, um den mehr Aufwand für das Aufrufen der-Funktion zu verringern.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-113">This is done to decrease the overhead of calling the function.</span></span>

</dd> <dt>

<span data-ttu-id="6f0f9-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplane*</span><span class="sxs-lookup"><span data-stu-id="6f0f9-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*</span></span>
</dt> <dd>

<span data-ttu-id="6f0f9-115">Optionale Liste von Clip-Ebenen, die bis zu 6 vom Benutzer angegebene Clip Flächen sind.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-115">Optional list of clip planes, which is up to 6 user-specified clip planes.</span></span> <span data-ttu-id="6f0f9-116">Dies ist ein alternativer Mechanismus für [SV \_ clipdistance](dx-graphics-hlsl-semantics.md) , der auf [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x und höher funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-116">This is an alternate mechanism for [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) that works on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span>

</dd> <dt>

<span data-ttu-id="6f0f9-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Benennen*</span><span class="sxs-lookup"><span data-stu-id="6f0f9-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="6f0f9-118">Eine ASCII-Zeichenfolge, die den Namen der Shader-Funktion eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-118">An ASCII string that uniquely identifies the name of the shader function.</span></span>

</dd> <dt>

<span data-ttu-id="6f0f9-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*Argument List*</span><span class="sxs-lookup"><span data-stu-id="6f0f9-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*</span></span>
</dt> <dd>

<span data-ttu-id="6f0f9-120">Optionale Argumentliste, eine durch Trennzeichen getrennte Liste von [Argumenten](dx-graphics-hlsl-function-parameters.md) , die an eine Funktion übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-120">Optional argument list, which is a comma-separated list of [arguments](dx-graphics-hlsl-function-parameters.md) passed into a function.</span></span>

</dd> <dt>

<span data-ttu-id="6f0f9-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Tischer*</span><span class="sxs-lookup"><span data-stu-id="6f0f9-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="6f0f9-122">Optionale Zeichenfolge, die die beabsichtigte Verwendung der Rückgabe Daten identifiziert (siehe [Semantik (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span><span class="sxs-lookup"><span data-stu-id="6f0f9-122">Optional string that identifies the intended usage of the return data (see [Semantics (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span></span>

</dd> <dt>

<span data-ttu-id="6f0f9-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*Status Block*</span><span class="sxs-lookup"><span data-stu-id="6f0f9-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span></span>
</dt> <dd>

<span data-ttu-id="6f0f9-124">Optionale [Anweisungen](dx-graphics-hlsl-statement-blocks.md) , die den Hauptteil der Funktion bilden.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-124">Optional [statements](dx-graphics-hlsl-statement-blocks.md) that make up the body of the function.</span></span> <span data-ttu-id="6f0f9-125">Eine Funktion, die ohne Text definiert ist, wird als Funktionsprototyp bezeichnet. der Text einer prototypfunktion muss an anderer Stelle definiert werden, bevor die Funktion aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-125">A function defined without a body is called a function prototype; the body of a prototype function must be defined elsewhere before the function can be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f0f9-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f0f9-126">Return Value</span></span>

<span data-ttu-id="6f0f9-127">Der Rückgabetyp kann einer dieser [HLSL-Typen](dx-graphics-hlsl-data-types.md)sein.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-127">The return type can be any one of these [HLSL types](dx-graphics-hlsl-data-types.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6f0f9-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f0f9-128">Remarks</span></span>

<span data-ttu-id="6f0f9-129">Die Syntax auf dieser Seite beschreibt fast alle Arten von HLSL-Funktionen, darunter Vertex-Shader, Pixel-Shader und Hilfsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-129">The syntax on this page describes almost every type of HLSL function, this includes vertex shaders, pixel shaders, and helper functions.</span></span> <span data-ttu-id="6f0f9-130">Obwohl ein Geometry-Shader auch mit einer Funktion implementiert wird, ist die Syntax etwas komplizierter, sodass eine separate Seite vorhanden ist, die eine Geometry-shaderfunktionsdeklaration definiert (siehe [Geometry-Shader-Objekt (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="6f0f9-130">While a geometry shader is also implemented with a function, its syntax is a little more complicated, so there is a separate page that defines a geometry shader function declaration (see [Geometry-Shader Object (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).</span></span>

<span data-ttu-id="6f0f9-131">Eine Funktion kann überladen werden, solange Sie eine eindeutige Kombination aus Parametertypen und/oder Parameterreihenfolge erhält.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-131">A function can be overloaded as long as it is given a unique combination of parameter types and/or parameter order.</span></span> <span data-ttu-id="6f0f9-132">HLSL implementiert auch eine Reihe integrierter oder [**intrinsischer Funktionen**](dx-graphics-hlsl-intrinsic-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6f0f9-132">HLSL also implements a number of built in, or [**intrinsic functions**](dx-graphics-hlsl-intrinsic-functions.md).</span></span>

<span data-ttu-id="6f0f9-133">Sie können benutzerspezifische Clip-Ebenen mit dem **clipplane** -Attribut angeben.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-133">You can specify user-specific clip planes with the **clipplanes** attribute.</span></span> <span data-ttu-id="6f0f9-134">Diese Clip Flächen werden von Windows auf alle gezeichneten primitiven angewendet.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-134">Windows applies these clip planes to all of the primitives drawn.</span></span> <span data-ttu-id="6f0f9-135">Das **clipplane** -Attribut funktioniert wie [SV \_ clipdistance](dx-graphics-hlsl-semantics.md) , funktioniert jedoch auf allen Hardware [Funktionsebenen](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x und höher.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-135">The **clipplanes** attribute works like [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) but works on all hardware [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span> <span data-ttu-id="6f0f9-136">Weitere Informationen finden Sie unter [User Clip Plane on Feature Level 9 Hardware](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).</span><span class="sxs-lookup"><span data-stu-id="6f0f9-136">For more info, see [User clip planes on feature level 9 hardware](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).</span></span>

## <a name="examples"></a><span data-ttu-id="6f0f9-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f0f9-137">Examples</span></span>

<span data-ttu-id="6f0f9-138">Dieses Beispiel ist aus BasicHLSL10. FX aus dem [BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)-Beispiel.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-138">This example is from BasicHLSL10.fx from the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span></span>


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



<span data-ttu-id="6f0f9-139">Dieses Beispiel aus advancedpartikel. FX aus dem [advancedpartikel](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)-Beispiel veranschaulicht die Verwendung einer Semantik für den Rückgabetyp.</span><span class="sxs-lookup"><span data-stu-id="6f0f9-139">This example from AdvancedParticles.fx from the [AdvancedParticles Sample](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx), illustrates using a semantic for the return type.</span></span>


```hlsl
//
// PS for particles
//
float4 PSPointSprite(PSSceneIn input) : SV_Target
{   
    return g_txDiffuse.Sample( g_samLinear, input.tex ) * input.color;
}
```



## <a name="related-topics"></a><span data-ttu-id="6f0f9-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6f0f9-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f0f9-141">Funktionen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f0f9-141">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 