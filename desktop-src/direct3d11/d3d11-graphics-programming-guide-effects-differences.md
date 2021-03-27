---
title: Unterschiede zwischen den Effekten 10 und Effekte 11
description: In diesem Thema werden die Unterschiede zwischen den Effekten 10 und den Effekten 11 veranschaulicht.
ms.assetid: c3e5e6bc-c544-49ee-b6d9-021ce87f9b12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29af1b9e7aec72f96a62e0f62668b81a6eec8367
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728232"
---
# <a name="differences-between-effects-10-and-effects-11"></a><span data-ttu-id="e25ff-103">Unterschiede zwischen den Effekten 10 und Effekte 11</span><span class="sxs-lookup"><span data-stu-id="e25ff-103">Differences Between Effects 10 and Effects 11</span></span>

<span data-ttu-id="e25ff-104">In diesem Thema werden die Unterschiede zwischen den Effekten 10 und den Effekten 11 veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="e25ff-104">This topic shows the differences between Effects 10 and Effects 11.</span></span>

## <a name="device-contexts-threading-and-cloning"></a><span data-ttu-id="e25ff-105">Geräte Kontexte, Threading und Klonen</span><span class="sxs-lookup"><span data-stu-id="e25ff-105">Device Contexts, Threading, and Cloning</span></span>

<span data-ttu-id="e25ff-106">Die ID3D10Device-Schnittstelle wurde in Direct3D 11 in zwei Schnittstellen aufgeteilt: ID3D11Device und Verknüpfung id3d11devicecontext aus.</span><span class="sxs-lookup"><span data-stu-id="e25ff-106">The ID3D10Device interface has been split into two interfaces in Direct3D 11: ID3D11Device and ID3D11DeviceContext.</span></span> <span data-ttu-id="e25ff-107">Sie können mehrere ID3D11DeviceContexts erstellen, um die gleichzeitige Ausführung für mehrere Threads zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="e25ff-107">You can create multiple ID3D11DeviceContexts to facilitate concurrent execution on multiple threads.</span></span> <span data-ttu-id="e25ff-108">Effekte 11 erweitert dieses Konzept auf das Effects-Framework.</span><span class="sxs-lookup"><span data-stu-id="e25ff-108">Effects 11 extends this concept to the Effects framework.</span></span>

<span data-ttu-id="e25ff-109">Die Auswirkung 11-Laufzeit ist ein Single Thread.</span><span class="sxs-lookup"><span data-stu-id="e25ff-109">The Effects 11 runtime is single-threaded.</span></span> <span data-ttu-id="e25ff-110">Aus diesem Grund sollten Sie keine einzelne ID3DX11Effect-Instanz mit mehreren Threads gleichzeitig verwenden.</span><span class="sxs-lookup"><span data-stu-id="e25ff-110">For this reason, you should not use a single ID3DX11Effect instance with multiple threads concurrently.</span></span>

<span data-ttu-id="e25ff-111">Wenn Sie die Effekte 11-Laufzeit für mehrere Instanzen verwenden möchten, müssen Sie separate ID3DX11Effect-Instanzen erstellen.</span><span class="sxs-lookup"><span data-stu-id="e25ff-111">To use the Effects 11 runtime on multiple instances, you must create separate ID3DX11Effect instances.</span></span> <span data-ttu-id="e25ff-112">Da Verknüpfung id3d11devicecontext aus auch Single Thread ist, sollten Sie bei Apply verschiedene Verknüpfung id3d11devicecontext aus-Instanzen an jede Effekt Instanz übergeben.</span><span class="sxs-lookup"><span data-stu-id="e25ff-112">Because the ID3D11DeviceContext is also single-threaded, you should pass different ID3D11DeviceContext instances to each effect instance on Apply.</span></span> <span data-ttu-id="e25ff-113">Sie können diese separaten Geräte Kontexte verwenden, um Befehlslisten zu erstellen, damit der Renderingthread diese auf den unmittelbaren Gerätekontext anwenden kann.</span><span class="sxs-lookup"><span data-stu-id="e25ff-113">You can use these separate device contexts to create command lists so that the rendering thread can apply them on the immediate device context.</span></span>

<span data-ttu-id="e25ff-114">Die einfachste Möglichkeit, mehrere Effekte zu erstellen, die dieselbe Funktionalität Kapseln, um Sie für mehrere Threads zu verwenden, besteht darin, einen Effekt zu erstellen und dann geklonte Kopien zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e25ff-114">The easiest way to create multiple effects that encapsulate the same functionality, for use on multiple threads, is to create one effect and then make cloned copies.</span></span> <span data-ttu-id="e25ff-115">Das Klonen bietet die folgenden Vorteile gegenüber der Erstellung mehrerer Kopien von Grund auf:</span><span class="sxs-lookup"><span data-stu-id="e25ff-115">Cloning has the following advantages over creating multiple copies from scratch:</span></span>

1.  <span data-ttu-id="e25ff-116">Die Klon Routine ist schneller als die Erstellungs Routine.</span><span class="sxs-lookup"><span data-stu-id="e25ff-116">The cloning routine is faster than the creation routine.</span></span>
2.  <span data-ttu-id="e25ff-117">Die geklonten Effekte teilen sich die erstellten Shader, Zustands Blöcke und Klassen Instanzen (sodass Sie nicht neu erstellt werden müssen).</span><span class="sxs-lookup"><span data-stu-id="e25ff-117">Cloned effects share created shaders, state blocks, and class instances (so they don't have to be recreated).</span></span>
3.  <span data-ttu-id="e25ff-118">Geklonte Effekte können Konstante Puffer gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="e25ff-118">Cloned effects can share constant buffers.</span></span>
4.  <span data-ttu-id="e25ff-119">Geklonte Effekte beginnen mit dem Zustand, der mit dem aktuellen Effekt übereinstimmt (Variablen Werte, unabhängig davon, ob Sie optimiert wurden).</span><span class="sxs-lookup"><span data-stu-id="e25ff-119">Cloned effects begin with state that matches the current effect (variable values, whether or not it has been optimized).</span></span>

<span data-ttu-id="e25ff-120">Weitere Informationen finden Sie unter [Klonen eines Effekts](d3d11-graphics-programming-guide-effects-cloning.md) .</span><span class="sxs-lookup"><span data-stu-id="e25ff-120">See [Cloning an Effect](d3d11-graphics-programming-guide-effects-cloning.md) for more information.</span></span>

## <a name="effect-pools-and-groups"></a><span data-ttu-id="e25ff-121">Effekt Pools und-Gruppen</span><span class="sxs-lookup"><span data-stu-id="e25ff-121">Effect Pools and Groups</span></span>

<span data-ttu-id="e25ff-122">Der weit verbreitete Gebrauch von Effekt Pools in Direct3D 10 war das Gruppieren von Material.</span><span class="sxs-lookup"><span data-stu-id="e25ff-122">By far the most prevalent use of effect pools in Direct3D 10 was for grouping materials.</span></span> <span data-ttu-id="e25ff-123">Die Effekt Pools wurden aus den Effekten 11 entfernt, und Gruppen wurden hinzugefügt. Dies ist eine effizientere Methode zum Gruppieren von Material.</span><span class="sxs-lookup"><span data-stu-id="e25ff-123">Effect Pools have been removed from Effects 11 and groups have been added, which is a more efficient method of grouping materials.</span></span>

<span data-ttu-id="e25ff-124">Eine Effekt Gruppe ist einfach eine Reihe von Techniken.</span><span class="sxs-lookup"><span data-stu-id="e25ff-124">An effect group is simply a set of techniques.</span></span> <span data-ttu-id="e25ff-125">Weitere Informationen finden Sie unter [Wirkungs Gruppen Syntax (Direct3D 11)](d3d11-effect-group-syntax.md) .</span><span class="sxs-lookup"><span data-stu-id="e25ff-125">See [Effect Group Syntax (Direct3D 11)](d3d11-effect-group-syntax.md) for more information.</span></span>

<span data-ttu-id="e25ff-126">Sehen Sie sich die folgende Effekt Hierarchie mit vier untergeordneten Effekten und einem Effekt Pool an:</span><span class="sxs-lookup"><span data-stu-id="e25ff-126">Consider the following effect hierarchy with four child effects and one effect pool:</span></span>


```
// Effect Pool
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

// Effect Child 1
#include "EffectPool.fx"
technique10 GrassMaterialLowSpec { ... }

// Effect Child 2
#include "EffectPool.fx"
technique10 GrassMaterialHighSpec { ... }

// Effect Child 3
#include "EffectPool.fx"
technique10 WaterMaterialLowSpec { ... }

// Effect Child 4
#include "EffectPool.fx"
technique10 WaterMaterialHighSpec { ... }
```



<span data-ttu-id="e25ff-127">Sie können die gleichen Funktionen in den Effekten 11 durch die Verwendung von Gruppen erreichen:</span><span class="sxs-lookup"><span data-stu-id="e25ff-127">You can achieve the same functionality in Effects 11 by using groups:</span></span>


```
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

fxgroup GrassMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}

fxgroup WaterMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}
```



## <a name="new-shader-stages"></a><span data-ttu-id="e25ff-128">Neue Shader-Stufen</span><span class="sxs-lookup"><span data-stu-id="e25ff-128">New Shader Stages</span></span>

<span data-ttu-id="e25ff-129">Es gibt drei neue Shader-Stufen in Direct3D 11: den Hull-Shader, den Domänen-Shader und den Compute-Shader.</span><span class="sxs-lookup"><span data-stu-id="e25ff-129">There are three new shader stages in Direct3D 11: the hull shader, domain shader, and compute shader.</span></span> <span data-ttu-id="e25ff-130">Effekte 11 behandelt diese auf ähnliche Weise wie Vertex-Shader, Geometry-Shader und Pixel-Shader.</span><span class="sxs-lookup"><span data-stu-id="e25ff-130">Effects 11 handles these in a similar manner to vertex shaders, geometry shaders, and pixel shaders.</span></span>

<span data-ttu-id="e25ff-131">Der Auswirkung 11 wurden drei neue Variablen Typen hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="e25ff-131">Three new variable types have been added to Effects 11:</span></span>

-   <span data-ttu-id="e25ff-132">Hullshader</span><span class="sxs-lookup"><span data-stu-id="e25ff-132">HullShader</span></span>
-   <span data-ttu-id="e25ff-133">Domainshader</span><span class="sxs-lookup"><span data-stu-id="e25ff-133">DomainShader</span></span>
-   <span data-ttu-id="e25ff-134">Computeshader</span><span class="sxs-lookup"><span data-stu-id="e25ff-134">ComputeShader</span></span>

<span data-ttu-id="e25ff-135">Wenn Sie diese Shader in einem Verfahren verwenden, müssen Sie die Technik "technique11" und nicht "technique10" bezeichnen.</span><span class="sxs-lookup"><span data-stu-id="e25ff-135">If you use these shaders in a technique, you must label that technique "technique11", and not "technique10".</span></span> <span data-ttu-id="e25ff-136">Der COMPUTE-Shader kann nicht im gleichen Durchlauf wie jeder andere Grafik Zustand (andere Shader, Zustands Blöcke oder Renderziele) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e25ff-136">The compute shader cannot be set in the same pass as any other graphics state (other shaders, state blocks, or render targets).</span></span>

## <a name="new-texture-types"></a><span data-ttu-id="e25ff-137">Neue Textur Typen</span><span class="sxs-lookup"><span data-stu-id="e25ff-137">New Texture Types</span></span>

<span data-ttu-id="e25ff-138">Direct3D 11 unterstützt die folgenden Textur Typen:</span><span class="sxs-lookup"><span data-stu-id="e25ff-138">Direct3D 11 supports the following texture types:</span></span>

-   [<span data-ttu-id="e25ff-139">Appendstructuredbuffer</span><span class="sxs-lookup"><span data-stu-id="e25ff-139">AppendStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [<span data-ttu-id="e25ff-140">Byteaddressbuffer</span><span class="sxs-lookup"><span data-stu-id="e25ff-140">ByteAddressBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer)
-   [<span data-ttu-id="e25ff-141">Consumestructuredbuffer</span><span class="sxs-lookup"><span data-stu-id="e25ff-141">ConsumeStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)
-   [<span data-ttu-id="e25ff-142">Structuredbuffer</span><span class="sxs-lookup"><span data-stu-id="e25ff-142">StructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer)

## <a name="unordered-access-views"></a><span data-ttu-id="e25ff-143">Ungeordnete Zugriffs Sichten</span><span class="sxs-lookup"><span data-stu-id="e25ff-143">Unordered Access Views</span></span>

<span data-ttu-id="e25ff-144">Effekte 11 unterstützt das Abrufen und Festlegen der neuen ungeordneten Zugriffs Ansichts Typen.</span><span class="sxs-lookup"><span data-stu-id="e25ff-144">Effects 11 supports getting and setting the new unordered access view types.</span></span> <span data-ttu-id="e25ff-145">Dies funktioniert auf ähnliche Weise wie Texturen.</span><span class="sxs-lookup"><span data-stu-id="e25ff-145">This works in a similar manner as textures.</span></span>

<span data-ttu-id="e25ff-146">Sehen Sie sich das HLSL-Beispiel an:</span><span class="sxs-lookup"><span data-stu-id="e25ff-146">Consider this Effects HLSL example:</span></span>


```
  
RWTexture1D<float> myUAV;
```



<span data-ttu-id="e25ff-147">Sie können diese Variable in C++ wie folgt festlegen:</span><span class="sxs-lookup"><span data-stu-id="e25ff-147">You can set this variable in C++ as follows:</span></span>


```
  
ID3D11UnorderedAccessView* pUAVTexture1D = NULL;
ID3DX11EffectUnorderedAccessViewVariable* pUAVVar;
pUAVVar = pEffect->GetVariableByName("myUAV")->AsUnorderedAccessView();
pUAVVar->SetUnorderedAccessView( pUAVTexture1D );
```



<span data-ttu-id="e25ff-148">Direct3D 11 unterstützt die folgenden ungeordneten Zugriffs Ansichts Typen:</span><span class="sxs-lookup"><span data-stu-id="e25ff-148">Direct3D 11 supports the following unordered access view types:</span></span>

-   <span data-ttu-id="e25ff-149">Rwbuffer</span><span class="sxs-lookup"><span data-stu-id="e25ff-149">RWBuffer</span></span>
-   <span data-ttu-id="e25ff-150">Rwbyteaddressbuffer</span><span class="sxs-lookup"><span data-stu-id="e25ff-150">RWByteAddressBuffer</span></span>
-   <span data-ttu-id="e25ff-151">Rwstructuredbuffer</span><span class="sxs-lookup"><span data-stu-id="e25ff-151">RWStructuredBuffer</span></span>
-   <span data-ttu-id="e25ff-152">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="e25ff-152">RWTexture1D</span></span>
-   <span data-ttu-id="e25ff-153">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="e25ff-153">RWTexture1DArray</span></span>
-   <span data-ttu-id="e25ff-154">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="e25ff-154">RWTexture2D</span></span>
-   <span data-ttu-id="e25ff-155">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="e25ff-155">RWTexture2DArray</span></span>
-   <span data-ttu-id="e25ff-156">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="e25ff-156">RWTexture3D</span></span>

## <a name="interfaces-and-class-instances"></a><span data-ttu-id="e25ff-157">Schnittstellen und Klassen Instanzen</span><span class="sxs-lookup"><span data-stu-id="e25ff-157">Interfaces and Class Instances</span></span>

<span data-ttu-id="e25ff-158">Informationen zur Schnittstelle und Klassen Syntax finden Sie unter [Schnittstellen und Klassen](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span><span class="sxs-lookup"><span data-stu-id="e25ff-158">For interface and class syntax, see [Interfaces and Classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span></span>

<span data-ttu-id="e25ff-159">Informationen zum Verwenden von Schnittstellen und Klassen in Effekten finden Sie unter [Schnittstellen und Klassen in Effekten](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).</span><span class="sxs-lookup"><span data-stu-id="e25ff-159">For using interfaces and classes in effects, see [Interfaces and Classes in Effects](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).</span></span>

## <a name="addressable-stream-out"></a><span data-ttu-id="e25ff-160">Adressier barer Datenstrom ausgehend</span><span class="sxs-lookup"><span data-stu-id="e25ff-160">Addressable Stream Out</span></span>

<span data-ttu-id="e25ff-161">In Direct3D 10 konnten Geometry-Shader einen Datenstrom an die Stream-Ausgabe Einheit und die Raster-Einheit ausgeben.</span><span class="sxs-lookup"><span data-stu-id="e25ff-161">In Direct3D 10, geometry shaders could output one stream of data to the stream output unit and the rasterizer unit.</span></span> <span data-ttu-id="e25ff-162">In Direct3D11 können Geometry-Shader bis zu vier Datenströme in die Datenstrom Ausgabe Einheit ausgeben, und höchstens einer dieser Datenströme an die Raster-Einheit.</span><span class="sxs-lookup"><span data-stu-id="e25ff-162">In Direct3D11, geometry shaders can output up to four streams of data to the stream output unit, and at most one of those streams to the rasterizer unit.</span></span> <span data-ttu-id="e25ff-163">Die systeminterne **konstruktgswithso** -Funktion wurde aktualisiert, um diese neue Funktion widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="e25ff-163">The **ConstructGSWithSO** intrinsic has been updated to reflect this new functionality.</span></span>

<span data-ttu-id="e25ff-164">Weitere Informationen finden [Sie unter Stream out-Syntax](d3d11-graphics-reference-effect-streamout.md) .</span><span class="sxs-lookup"><span data-stu-id="e25ff-164">See [Stream Out Syntax](d3d11-graphics-reference-effect-streamout.md) for more information.</span></span>

## <a name="setting-and-unsetting-device-state"></a><span data-ttu-id="e25ff-165">Festlegen und Zurücksetzen des Gerätestatus</span><span class="sxs-lookup"><span data-stu-id="e25ff-165">Setting and Unsetting Device State</span></span>

<span data-ttu-id="e25ff-166">In den Effekten 10 könnten Sie Konstante Puffer und Textur Puffer mithilfe der [**ID3D10EffectConstantBuffer:: setconstantbuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) -und [**settexturebuffer**](id3dx11effectconstantbuffer-settexturebuffer.md) -Funktionen vom Benutzer verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="e25ff-166">In Effects 10, you could make constant buffers and texture buffers user-managed by using the [**ID3D10EffectConstantBuffer::SetConstantBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) and [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md) functions.</span></span> <span data-ttu-id="e25ff-167">Nachdem Sie diese Funktionen aufgerufen haben, verwaltet die Runtime 10 Runtime nicht mehr den konstanten Puffer oder Textur Puffer, und der Benutzer muss die Daten mithilfe der ID3D10Device-Schnittstelle ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="e25ff-167">After you call these functions, the Effects 10 runtime no longer manages the constant buffer or texture buffer and the user must fill the data by using the ID3D10Device interface.</span></span>

<span data-ttu-id="e25ff-168">In Auswirkung 11 können Sie auch die Zustands Blöcke (Blend-Status, Status des Rasterizers, tiefen Schablone und samplerstatus) mithilfe der folgenden Aufrufe erstellen:</span><span class="sxs-lookup"><span data-stu-id="e25ff-168">In Effects 11, you can also make the state blocks (blend state, rasterizer state, depth-stencil state, and sampler state) user-managed by using the following calls:</span></span>

-   [<span data-ttu-id="e25ff-169">**ID3DX11EffectBlendVariable:: setblendstate**</span><span class="sxs-lookup"><span data-stu-id="e25ff-169">**ID3DX11EffectBlendVariable::SetBlendState**</span></span>](id3dx11effectblendvariable-setblendstate.md)
-   [<span data-ttu-id="e25ff-170">**ID3DX11EffectRasterizerVariable:: tartrasterizerstate**</span><span class="sxs-lookup"><span data-stu-id="e25ff-170">**ID3DX11EffectRasterizerVariable::SetRasterizerState**</span></span>](id3dx11effectrasterizervariable-setrasterizerstate.md)
-   [<span data-ttu-id="e25ff-171">**ID3DX11EffectDepthStencilVariable:: setdepthstencilstate**</span><span class="sxs-lookup"><span data-stu-id="e25ff-171">**ID3DX11EffectDepthStencilVariable::SetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)
-   [<span data-ttu-id="e25ff-172">**ID3DX11EffectSamplerVariable:: setsampler**</span><span class="sxs-lookup"><span data-stu-id="e25ff-172">**ID3DX11EffectSamplerVariable::SetSampler**</span></span>](id3dx11effectsamplervariable-setsampler.md)

<span data-ttu-id="e25ff-173">Nachdem Sie diese Funktionen aufgerufen haben, werden die Block Variablen in der Auswirkung 11 nicht mehr verwaltet, und die Werte bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="e25ff-173">After you call these functions, the Effects 11 runtime no longer manages the state block variables, and there values will remain unchanged.</span></span> <span data-ttu-id="e25ff-174">Beachten Sie, dass der Benutzer einen neuen Zustands Block festlegen muss, um die Werte zu ändern, da Zustands Blöcke unveränderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e25ff-174">Note that because state blocks are immutable, the user must set a new state block to change the values.</span></span>

<span data-ttu-id="e25ff-175">Sie können auch Konstante Puffer, Textur Puffer und Zustands Blöcke auf den Nichtbenutzer verwalteten Zustand zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="e25ff-175">You can also revert constant buffers, texture buffers, and state blocks to the non-user managed state.</span></span> <span data-ttu-id="e25ff-176">Wenn Sie diese Variablen nicht mehr festlegen, werden Sie von der Common Language Runtime bei Bedarf weiterhin aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e25ff-176">If you unset these variables, the Effects 11 runtime will continue to update them when necessary.</span></span> <span data-ttu-id="e25ff-177">Mit den folgenden aufrufen können Sie vom Benutzer verwaltete Variablen nicht festlegen:</span><span class="sxs-lookup"><span data-stu-id="e25ff-177">You can use the following calls to unset user managed variables:</span></span>

-   [<span data-ttu-id="e25ff-178">**ID3DX11EffectConstantBuffer:: undosetconstantbuffer**</span><span class="sxs-lookup"><span data-stu-id="e25ff-178">**ID3DX11EffectConstantBuffer::UndoSetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-undosetconstantbuffer.md)
-   [<span data-ttu-id="e25ff-179">**ID3DX11EffectConstantBuffer:: undosettexturebuffer**</span><span class="sxs-lookup"><span data-stu-id="e25ff-179">**ID3DX11EffectConstantBuffer::UndoSetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-undosettexturebuffer.md)
-   [<span data-ttu-id="e25ff-180">**ID3DX11EffectBlendVariable:: undosetblendstate**</span><span class="sxs-lookup"><span data-stu-id="e25ff-180">**ID3DX11EffectBlendVariable::UndoSetBlendState**</span></span>](id3dx11effectblendvariable-undosetblendstate.md)
-   [<span data-ttu-id="e25ff-181">**ID3DX11EffectRasterizerVariable:: undotartrasterizerstate**</span><span class="sxs-lookup"><span data-stu-id="e25ff-181">**ID3DX11EffectRasterizerVariable::UndoSetRasterizerState**</span></span>](id3dx11effectrasterizervariable-undosetrasterizerstate.md)
-   [<span data-ttu-id="e25ff-182">**ID3DX11EffectDepthStencilVariable:: undosetdepthstencilstate**</span><span class="sxs-lookup"><span data-stu-id="e25ff-182">**ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md)
-   [<span data-ttu-id="e25ff-183">**ID3DX11EffectSamplerVariable:: undosetsampler**</span><span class="sxs-lookup"><span data-stu-id="e25ff-183">**ID3DX11EffectSamplerVariable::UndoSetSampler**</span></span>](id3dx11effectsamplervariable-undosetsampler.md)

## <a name="effects-virtual-machine"></a><span data-ttu-id="e25ff-184">Auswirkungen virtueller Computer</span><span class="sxs-lookup"><span data-stu-id="e25ff-184">Effects Virtual Machine</span></span>

<span data-ttu-id="e25ff-185">Die Auswirkungen der virtuellen Maschine, die komplexe Ausdrücke außerhalb der Funktionen ausgewertet hat, wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="e25ff-185">The effects virtual machine, which evaluated complex expressions outside of functions, has been removed.</span></span>

<span data-ttu-id="e25ff-186">Die folgenden Beispiele für komplexe Ausdrücke werden nicht unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e25ff-186">The following examples of complex expressions are not supported:</span></span>

1.  <span data-ttu-id="e25ff-187">Setpixelshader (mypsarray (i \* 3 + j));</span><span class="sxs-lookup"><span data-stu-id="e25ff-187">SetPixelShader( myPSArray( i \* 3 + j ) );</span></span>
2.  <span data-ttu-id="e25ff-188">Setpixelshader (mypsarray ((float) i);</span><span class="sxs-lookup"><span data-stu-id="e25ff-188">SetPixelShader( myPSArray( (float)i );</span></span>
3.  <span data-ttu-id="e25ff-189">Filter = i + 2;</span><span class="sxs-lookup"><span data-stu-id="e25ff-189">FILTER = i + 2;</span></span>

<span data-ttu-id="e25ff-190">Die folgenden Beispiele für nicht komplexe Ausdrücke werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e25ff-190">The following examples of non-complex expressions are supported:</span></span>

1.  <span data-ttu-id="e25ff-191">Setpixelshader (myps);</span><span class="sxs-lookup"><span data-stu-id="e25ff-191">SetPixelShader( myPS );</span></span>
2.  <span data-ttu-id="e25ff-192">Setpixelshader (myps \[ i \] );</span><span class="sxs-lookup"><span data-stu-id="e25ff-192">SetPixelShader( myPS\[i\] );</span></span>
3.  <span data-ttu-id="e25ff-193">Setpixelshader (myps \[ uindex \] );//uindex ist eine uint-Variable.</span><span class="sxs-lookup"><span data-stu-id="e25ff-193">SetPixelShader( myPS\[ uIndex \] ); // uIndex is a uint variable</span></span>
4.  <span data-ttu-id="e25ff-194">Filter = i;</span><span class="sxs-lookup"><span data-stu-id="e25ff-194">FILTER = i;</span></span>
5.  <span data-ttu-id="e25ff-195">Filter = anisotrope;</span><span class="sxs-lookup"><span data-stu-id="e25ff-195">FILTER = ANISOTROPIC;</span></span>

<span data-ttu-id="e25ff-196">Diese Ausdrücke können in Zustands Block Ausdrücken (z. b. Filter) und Pass Ausdrücken (z. b. setpixelshader) vorkommen.</span><span class="sxs-lookup"><span data-stu-id="e25ff-196">These expressions could appear in state block expressions (such as FILTER) and pass expressions (such as SetPixelShader).</span></span>

## <a name="source-availability-and-location"></a><span data-ttu-id="e25ff-197">Quell Verfügbarkeit und-Speicherort</span><span class="sxs-lookup"><span data-stu-id="e25ff-197">Source Availability and Location</span></span>

<span data-ttu-id="e25ff-198">Die Auswirkungen 10 wurden in D3D10.dll verteilt.</span><span class="sxs-lookup"><span data-stu-id="e25ff-198">Effects 10 was distributed in D3D10.dll.</span></span> <span data-ttu-id="e25ff-199">Die Effekte 11 werden als Quelle und mit entsprechenden Visual Studio-Projektmappen verteilt, um Sie zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="e25ff-199">Effects 11 is distributed as source, with corresponding Visual Studio solutions to compile it.</span></span> <span data-ttu-id="e25ff-200">Wenn Sie Effekte vom Typ Anwendungen erstellen, empfiehlt es sich, die Effekte 11-Quelle direkt in diese Anwendungen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="e25ff-200">When you create effects-type applications, we recommend that you include the Effects 11 source directly in those applications.</span></span>

<span data-ttu-id="e25ff-201">Sie können die Effekte 11 von den [Effekten für das Update von Direct3D 11](https://github.com/Microsoft/FX11)erhalten.</span><span class="sxs-lookup"><span data-stu-id="e25ff-201">You can get Effects 11 from [Effects for Direct3D 11 Update](https://github.com/Microsoft/FX11).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e25ff-202">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e25ff-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e25ff-203">Effekte (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="e25ff-203">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 