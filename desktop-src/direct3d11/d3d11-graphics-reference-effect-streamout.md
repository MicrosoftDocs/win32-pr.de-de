---
title: Stream out-Syntax
description: Ein Geometry-Shader mit Stream out wird mit einer bestimmten Syntax deklariert.
ms.assetid: 58cf6503-0dde-4c88-837d-ae0e0eda17d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ea78d1b2109e343f01800b3a3d5e1bf6efaba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992791"
---
# <a name="stream-out-syntax"></a><span data-ttu-id="6b41d-103">Stream out-Syntax</span><span class="sxs-lookup"><span data-stu-id="6b41d-103">Stream Out Syntax</span></span>

<span data-ttu-id="6b41d-104">Ein Geometry-Shader mit Stream out wird mit einer bestimmten Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="6b41d-104">A geometry shader with stream out is declared with a particular syntax.</span></span> <span data-ttu-id="6b41d-105">In diesem Thema wird die-Syntax beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6b41d-105">This topic describes the syntax.</span></span> <span data-ttu-id="6b41d-106">In der Effect-Laufzeit wird diese Syntax in einen-Befehl von [**ID3D11Device::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)-Alias konvertiert.</span><span class="sxs-lookup"><span data-stu-id="6b41d-106">In the effect runtime, this syntax will be converted to a call to [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput).</span></span>

## <a name="construct-syntax"></a><span data-ttu-id="6b41d-107">Syntax erstellen</span><span class="sxs-lookup"><span data-stu-id="6b41d-107">Construct Syntax</span></span>


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0" )
```





| <span data-ttu-id="6b41d-108">Name</span><span class="sxs-lookup"><span data-stu-id="6b41d-108">Name</span></span>                   | <span data-ttu-id="6b41d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b41d-109">Description</span></span>                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b41d-110">**Streamingshadervar**</span><span class="sxs-lookup"><span data-stu-id="6b41d-110">**StreamingShaderVar**</span></span> | <span data-ttu-id="6b41d-111">Optional.</span><span class="sxs-lookup"><span data-stu-id="6b41d-111">Optional.</span></span> <span data-ttu-id="6b41d-112">Eine ASCI-Zeichenfolge, die den Namen einer Geometry-shadervariablen mit Stream out eindeutig identifiziert. Dies ist optional, da constructgswithso direkt in einem setgeometryshader-oder bindinterfaces-aufrufen platziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6b41d-112">An ASCI string that uniquely identifies the name of a geometry shader variable with stream out. This is optional because ConstructGSWithSO can be placed directly in a SetGeometryShader or BindInterfaces call.</span></span> |
| <span data-ttu-id="6b41d-113">**Shadervar**</span><span class="sxs-lookup"><span data-stu-id="6b41d-113">**ShaderVar**</span></span>          | <span data-ttu-id="6b41d-114">Eine Geometry-Shader-oder Vertex-Shader-Variable.</span><span class="sxs-lookup"><span data-stu-id="6b41d-114">A geometry shader or vertex shader variable.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="6b41d-115">**OutputDecl0**</span><span class="sxs-lookup"><span data-stu-id="6b41d-115">**OutputDecl0**</span></span>        | <span data-ttu-id="6b41d-116">Eine Zeichenfolge, die definiert, welche shaderausgaben in Stream 0 gestreamt werden. Die Syntax finden Sie weiter unten.</span><span class="sxs-lookup"><span data-stu-id="6b41d-116">A string defining which shader outputs in stream 0 are streamed out. See below for syntax.</span></span>                                                                                                                                 |



 

<span data-ttu-id="6b41d-117">Dies ist die Syntax, die in FX \_ 4 \_ 0-Dateien definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6b41d-117">This is the syntax was defined in fx\_4\_0 files.</span></span> <span data-ttu-id="6b41d-118">Beachten Sie, dass in GS \_ 4 \_ 0 und vs \_ x-Shadern nur ein Datenstrom vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6b41d-118">Note that in gs\_4\_0 and vs\_x shaders, there is only one stream of data.</span></span> <span data-ttu-id="6b41d-119">Der resultierende Shader gibt einen Datenstrom sowohl an die Stream-out-Einheit als auch an die Raster-Einheit aus.</span><span class="sxs-lookup"><span data-stu-id="6b41d-119">The resulting shader will output one stream to both the stream out unit and the rasterizer unit.</span></span>


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0", "OutputDecl1", "OutputDecl2", 
"OutputDecl3", RasterizedStream )
```





| <span data-ttu-id="6b41d-120">Name</span><span class="sxs-lookup"><span data-stu-id="6b41d-120">Name</span></span>                   | <span data-ttu-id="6b41d-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b41d-121">Description</span></span>                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b41d-122">**Streamingshadervar**</span><span class="sxs-lookup"><span data-stu-id="6b41d-122">**StreamingShaderVar**</span></span> | <span data-ttu-id="6b41d-123">Optional.</span><span class="sxs-lookup"><span data-stu-id="6b41d-123">Optional.</span></span> <span data-ttu-id="6b41d-124">Eine ASCI-Zeichenfolge, die den Namen einer Geometry-shadervariablen mit Stream out eindeutig identifiziert. Dies ist optional, da constructgswithso direkt in einem setgeometryshader-oder bindinterfaces-aufrufen platziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6b41d-124">An ASCI string that uniquely identifies the name of a geometry shader variable with stream out. This is optional because ConstructGSWithSO can be placed directly in a SetGeometryShader or BindInterfaces call.</span></span> |
| <span data-ttu-id="6b41d-125">**Shadervar**</span><span class="sxs-lookup"><span data-stu-id="6b41d-125">**ShaderVar**</span></span>          | <span data-ttu-id="6b41d-126">Eine Geometry-Shader-oder Vertex-Shader-Variable.</span><span class="sxs-lookup"><span data-stu-id="6b41d-126">A geometry shader or vertex shader variable.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="6b41d-127">**OutputDecl0**</span><span class="sxs-lookup"><span data-stu-id="6b41d-127">**OutputDecl0**</span></span>        | <span data-ttu-id="6b41d-128">Eine Zeichenfolge, die definiert, welche shaderausgaben in Stream 0 gestreamt werden. Die Syntax finden Sie weiter unten.</span><span class="sxs-lookup"><span data-stu-id="6b41d-128">A string defining which shader outputs in stream 0 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="6b41d-129">**OutputDecl1**</span><span class="sxs-lookup"><span data-stu-id="6b41d-129">**OutputDecl1**</span></span>        | <span data-ttu-id="6b41d-130">Eine Zeichenfolge, die definiert, welche shaderausgaben in Stream 1 gestreamt werden. Die Syntax finden Sie weiter unten.</span><span class="sxs-lookup"><span data-stu-id="6b41d-130">A string defining which shader outputs in stream 1 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="6b41d-131">**OutputDecl2**</span><span class="sxs-lookup"><span data-stu-id="6b41d-131">**OutputDecl2**</span></span>        | <span data-ttu-id="6b41d-132">Eine Zeichenfolge, die definiert, welche shaderausgaben in Stream 2 gestreamt werden. Die Syntax finden Sie weiter unten.</span><span class="sxs-lookup"><span data-stu-id="6b41d-132">A string defining which shader outputs in stream 2 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="6b41d-133">**OutputDecl3**</span><span class="sxs-lookup"><span data-stu-id="6b41d-133">**OutputDecl3**</span></span>        | <span data-ttu-id="6b41d-134">Eine Zeichenfolge, die definiert, welche shaderausgaben in Stream 3 gestreamt werden. Die Syntax finden Sie weiter unten.</span><span class="sxs-lookup"><span data-stu-id="6b41d-134">A string defining which shader outputs in stream 3 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="6b41d-135">**Rasterizedstream**</span><span class="sxs-lookup"><span data-stu-id="6b41d-135">**RasterizedStream**</span></span>   | <span data-ttu-id="6b41d-136">Eine ganze Zahl, die angibt, welcher Stream an den Rasterizer gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b41d-136">An integer specifying which stream will be sent to the rasterizer.</span></span>                                                                                                                                                         |



 

<span data-ttu-id="6b41d-137">Beachten Sie, dass GS \_ 5 \_ 0-Shader bis zu vier Datenströme definieren können.</span><span class="sxs-lookup"><span data-stu-id="6b41d-137">Note that gs\_5\_0 shaders can define up to four streams of data.</span></span> <span data-ttu-id="6b41d-138">Der resultierende Shader gibt einen Datenstrom für jede Ausgabe Deklaration ungleich **null** und einen Stream der Raster-Einheit an die Datenstrom Ausgabe aus.</span><span class="sxs-lookup"><span data-stu-id="6b41d-138">The resulting shader will output one stream to the stream out unit for each non-**NULL** output declaration and one stream the rasterizer unit.</span></span>

## <a name="stream-out-declaration-syntax"></a><span data-ttu-id="6b41d-139">Syntax der Stream out-Deklaration</span><span class="sxs-lookup"><span data-stu-id="6b41d-139">Stream Out Declaration Syntax</span></span>


```
" [ Buffer: ] Semantic[ SemanticIndex ] [ .Mask ]; [ ... ; ] ... [ ... ;]"
```





| <span data-ttu-id="6b41d-140">Name</span><span class="sxs-lookup"><span data-stu-id="6b41d-140">Name</span></span>              | <span data-ttu-id="6b41d-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b41d-141">Description</span></span>                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b41d-142">**Buffer**</span><span class="sxs-lookup"><span data-stu-id="6b41d-142">**Buffer**</span></span>        | <span data-ttu-id="6b41d-143">Optional.</span><span class="sxs-lookup"><span data-stu-id="6b41d-143">Optional.</span></span> <span data-ttu-id="6b41d-144">Eine ganze Zahl, 0 <= Puffer < 4, die angibt, an welchen Stream-out-Puffer der Wert gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b41d-144">An integer, 0 <= Buffer < 4, specifying which stream out buffer the value will go to.</span></span> |
| <span data-ttu-id="6b41d-145">**Tischer**</span><span class="sxs-lookup"><span data-stu-id="6b41d-145">**Semantic**</span></span>      | <span data-ttu-id="6b41d-146">Eine Zeichenfolge zusammen mit semanticindex, die angibt, welcher Wert ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b41d-146">A string, along with SemanticIndex, specifying which value to output.</span></span>                                 |
| <span data-ttu-id="6b41d-147">**Semanticindex**</span><span class="sxs-lookup"><span data-stu-id="6b41d-147">**SemanticIndex**</span></span> | <span data-ttu-id="6b41d-148">Optional.</span><span class="sxs-lookup"><span data-stu-id="6b41d-148">Optional.</span></span> <span data-ttu-id="6b41d-149">Der der Semantik zugeordnete Index.</span><span class="sxs-lookup"><span data-stu-id="6b41d-149">The index associated with Semantic.</span></span>                                                         |
| <span data-ttu-id="6b41d-150">**Mask**</span><span class="sxs-lookup"><span data-stu-id="6b41d-150">**Mask**</span></span>          | <span data-ttu-id="6b41d-151">Optional.</span><span class="sxs-lookup"><span data-stu-id="6b41d-151">Optional.</span></span> <span data-ttu-id="6b41d-152">Eine Komponenten Maske, die angibt, welche Komponenten des Werts ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6b41d-152">A component mask, indicating which components of the value to output.</span></span>                       |



 

<span data-ttu-id="6b41d-153">Es gibt eine besondere Semantik mit der Bezeichnung "$Skip", die eine leere Semantik angibt, sodass der entsprechende Arbeitsspeicher im Stream-out-Puffer unverändert bleibt.</span><span class="sxs-lookup"><span data-stu-id="6b41d-153">There is one special Semantic, labeled "$SKIP" which indicates an empty semantic, leaving the corresponding memory in the stream out buffer untouched.</span></span> <span data-ttu-id="6b41d-154">Die $Skip Semantik darf keinen semanticindex aufweisen, kann jedoch eine Maske aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6b41d-154">The $SKIP semantic cannot have a SemanticIndex, but can have a Mask.</span></span>

<span data-ttu-id="6b41d-155">Die gesamte Stream out-Deklaration kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="6b41d-155">The entire stream out declaration can be **NULL**.</span></span>

## <a name="example"></a><span data-ttu-id="6b41d-156">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6b41d-156">Example</span></span>


```
struct GSOutput
{
int4 Pos : Position;
int4 Color : Color;
int4 Texcoord : Texcoord;
};

[maxvertexcount(1)]
void gsBase (inout PointStream<GSOutput> OutputStream, inout PointStream<GSOutput> OutputStream1)
{
GSOutput output;
output.Pos = int4(1,2,3,4);
output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream.Append(output);

output.Pos = int4(1,2,3,4);
    output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream1.Append(output);
};


GeometryShader pGSComp = CompileShader(gs_5_0, gsBase());
GeometryShader pGSwSO = ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                   "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1);

// The following two passes perform the same operation
technique11 SOPoints
{
    pass 
    {
        SetGeometryShader(ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                     "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1));
    }
    pass 
    {
        SetGeometryShader(pGSwSO);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="6b41d-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6b41d-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b41d-158">Effekte (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="6b41d-158">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




