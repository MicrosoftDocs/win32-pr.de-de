---
title: Effect-System Schnittstellen (Direct3D 11)
description: Das Effect-System definiert mehrere Schnittstellen zur Verwaltung des Wirkungs Zustands.
ms.assetid: 5cba6055-d153-4837-9a08-96efbde5f48f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af76a54be06e52e320743ca945abb31d1d50d213
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708544"
---
# <a name="effect-system-interfaces-direct3d-11"></a><span data-ttu-id="ba89e-103">Effect-System Schnittstellen (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="ba89e-103">Effect System Interfaces (Direct3D 11)</span></span>

<span data-ttu-id="ba89e-104">Das Effect-System definiert mehrere Schnittstellen zur Verwaltung des Wirkungs Zustands.</span><span class="sxs-lookup"><span data-stu-id="ba89e-104">The effect system defines several interfaces for managing effect state.</span></span> <span data-ttu-id="ba89e-105">Es gibt zwei Arten von Schnittstellen: solche, die von der Laufzeit verwendet werden, um einen Effekt und reflektionsschnittstellen zum erhalten und Festlegen von Effekt Variablen zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="ba89e-105">There are two types of interfaces: those used by the runtime to render an effect and reflection interfaces for getting and setting effect variables.</span></span>

-   [<span data-ttu-id="ba89e-106">Lauf Zeit Schnittstellen von Effekten</span><span class="sxs-lookup"><span data-stu-id="ba89e-106">Effect Runtime Interfaces</span></span>](#effect-runtime-interfaces)
-   [<span data-ttu-id="ba89e-107">Effekt reflektionseschnittstellen</span><span class="sxs-lookup"><span data-stu-id="ba89e-107">Effect Reflection Interfaces</span></span>](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a><span data-ttu-id="ba89e-108">Lauf Zeit Schnittstellen von Effekten</span><span class="sxs-lookup"><span data-stu-id="ba89e-108">Effect Runtime Interfaces</span></span>

<span data-ttu-id="ba89e-109">Verwenden Sie Lauf Zeit Schnittstellen zum Rendering eines Effekts.</span><span class="sxs-lookup"><span data-stu-id="ba89e-109">Use runtime interfaces to render an effect.</span></span>



| <span data-ttu-id="ba89e-110">Lauf Zeit Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ba89e-110">Runtime Interfaces</span></span>                                       | <span data-ttu-id="ba89e-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba89e-111">Description</span></span>                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="ba89e-112">**ID3DX11Effect**</span><span class="sxs-lookup"><span data-stu-id="ba89e-112">**ID3DX11Effect**</span></span>](id3dx11effect.md)                   | <span data-ttu-id="ba89e-113">Sammlung von einer oder mehreren Gruppen und Techniken zum Rendern.</span><span class="sxs-lookup"><span data-stu-id="ba89e-113">Collection of one or more groups and techniques for rendering.</span></span> |
| [<span data-ttu-id="ba89e-114">**ID3DX11EffectPass**</span><span class="sxs-lookup"><span data-stu-id="ba89e-114">**ID3DX11EffectPass**</span></span>](id3dx11effectpass.md)           | <span data-ttu-id="ba89e-115">Eine Auflistung von Zustands Zuweisungen.</span><span class="sxs-lookup"><span data-stu-id="ba89e-115">A collection of state assignments.</span></span>                             |
| [<span data-ttu-id="ba89e-116">**ID3DX11EffectTechnique**</span><span class="sxs-lookup"><span data-stu-id="ba89e-116">**ID3DX11EffectTechnique**</span></span>](id3dx11effecttechnique.md) | <span data-ttu-id="ba89e-117">Eine Auflistung von einem oder mehreren Durchläufen.</span><span class="sxs-lookup"><span data-stu-id="ba89e-117">A collection of one or more passes.</span></span>                            |
| [<span data-ttu-id="ba89e-118">**ID3DX11EffectGroup**</span><span class="sxs-lookup"><span data-stu-id="ba89e-118">**ID3DX11EffectGroup**</span></span>](id3dx11effectgroup.md)         | <span data-ttu-id="ba89e-119">Eine Auflistung von einer oder mehreren Techniken.</span><span class="sxs-lookup"><span data-stu-id="ba89e-119">A collection of one or more techniques.</span></span>                        |



 

## <a name="effect-reflection-interfaces"></a><span data-ttu-id="ba89e-120">Effekt reflektionseschnittstellen</span><span class="sxs-lookup"><span data-stu-id="ba89e-120">Effect Reflection Interfaces</span></span>

<span data-ttu-id="ba89e-121">Reflektion wird im Effektsystem implementiert, um das Lesen (und schreiben) des Wirkungs Zustands zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ba89e-121">Reflection is implemented in the effect system to support reading (and writing) effect state.</span></span> <span data-ttu-id="ba89e-122">Es gibt mehrere Möglichkeiten, auf Wirkungs Variablen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ba89e-122">There are multiple ways to access effect variables.</span></span>

### <a name="setting-groups-of-effect-state"></a><span data-ttu-id="ba89e-123">Festlegen von Gruppen von Effekt Zuständen</span><span class="sxs-lookup"><span data-stu-id="ba89e-123">Setting Groups of Effect State</span></span>

<span data-ttu-id="ba89e-124">Verwenden Sie diese Schnittstellen, um eine Gruppe des Zustands zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ba89e-124">Use these interfaces to get and set a group of state.</span></span>



| <span data-ttu-id="ba89e-125">Reflektionseschnittstellen</span><span class="sxs-lookup"><span data-stu-id="ba89e-125">Reflection Interfaces</span></span>                                                          | <span data-ttu-id="ba89e-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba89e-126">Description</span></span>                      |
|--------------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="ba89e-127">**ID3DX11EffectBlendVariable**</span><span class="sxs-lookup"><span data-stu-id="ba89e-127">**ID3DX11EffectBlendVariable**</span></span>](id3dx11effectblendvariable.md)               | <span data-ttu-id="ba89e-128">Get-und Set-Blend-Zustand.</span><span class="sxs-lookup"><span data-stu-id="ba89e-128">Get and set blend state.</span></span>         |
| [<span data-ttu-id="ba89e-129">**ID3DX11EffectDepthStencilVariable**</span><span class="sxs-lookup"><span data-stu-id="ba89e-129">**ID3DX11EffectDepthStencilVariable**</span></span>](id3dx11effectdepthstencilvariable.md) | <span data-ttu-id="ba89e-130">Get und Set tiefen Schablone State.</span><span class="sxs-lookup"><span data-stu-id="ba89e-130">Get and set depth-stencil state.</span></span> |
| [<span data-ttu-id="ba89e-131">**ID3DX11EffectRasterizerVariable**</span><span class="sxs-lookup"><span data-stu-id="ba89e-131">**ID3DX11EffectRasterizerVariable**</span></span>](id3dx11effectrasterizervariable.md)     | <span data-ttu-id="ba89e-132">Get-und Set-Status des Rasterizers.</span><span class="sxs-lookup"><span data-stu-id="ba89e-132">Get and set rasterizer state.</span></span>    |
| [<span data-ttu-id="ba89e-133">**ID3DX11EffectSamplerVariable**</span><span class="sxs-lookup"><span data-stu-id="ba89e-133">**ID3DX11EffectSamplerVariable**</span></span>](id3dx11effectsamplervariable.md)           | <span data-ttu-id="ba89e-134">Holen Sie sich den samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="ba89e-134">Get and set sampler state.</span></span>       |



 

### <a name="setting-effect-resources"></a><span data-ttu-id="ba89e-135">Festlegen von Effekt Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ba89e-135">Setting Effect Resources</span></span>

<span data-ttu-id="ba89e-136">Verwenden Sie diese Schnittstellen, um Ressourcen zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ba89e-136">Use these interfaces to get and set resources.</span></span>



| <span data-ttu-id="ba89e-137">Reflektionseschnittstellen</span><span class="sxs-lookup"><span data-stu-id="ba89e-137">Reflection Interfaces</span></span>                                                                        | <span data-ttu-id="ba89e-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba89e-138">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="ba89e-139">**ID3DX11EffectConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="ba89e-139">**ID3DX11EffectConstantBuffer**</span></span>](id3dx11effectconstantbuffer.md)                           | <span data-ttu-id="ba89e-140">Zugreifen auf Daten in einem Textur Puffer oder Konstantenpuffer.</span><span class="sxs-lookup"><span data-stu-id="ba89e-140">Access data in a texture buffer or constant buffer.</span></span> |
| [<span data-ttu-id="ba89e-141">**ID3DX11EffectDepthStencilViewVariable**</span><span class="sxs-lookup"><span data-stu-id="ba89e-141">**ID3DX11EffectDepthStencilViewVariable**</span></span>](id3dx11effectdepthstencilviewvariable.md)       | <span data-ttu-id="ba89e-142">Zugreifen auf Daten in einer tiefen Schablone-Ressource.</span><span class="sxs-lookup"><span data-stu-id="ba89e-142">Access data in a depth-stencil resource.</span></span>            |
| [<span data-ttu-id="ba89e-143">**ID3DX11EffectRenderTargetViewVariable**</span><span class="sxs-lookup"><span data-stu-id="ba89e-143">**ID3DX11EffectRenderTargetViewVariable**</span></span>](id3dx11effectrendertargetviewvariable.md)       | <span data-ttu-id="ba89e-144">Zugreifen auf Daten in einem Renderziel.</span><span class="sxs-lookup"><span data-stu-id="ba89e-144">Access data in a render target.</span></span>                     |
| [<span data-ttu-id="ba89e-145">**ID3DX11EffectShaderResourceVariable**</span><span class="sxs-lookup"><span data-stu-id="ba89e-145">**ID3DX11EffectShaderResourceVariable**</span></span>](id3dx11effectshaderresourcevariable.md)           | <span data-ttu-id="ba89e-146">Zugreifen auf Daten in einer Shaderressource.</span><span class="sxs-lookup"><span data-stu-id="ba89e-146">Access data in a shader resource.</span></span>                   |
| [<span data-ttu-id="ba89e-147">**ID3DX11EffectUnorderedAccessViewVariable**</span><span class="sxs-lookup"><span data-stu-id="ba89e-147">**ID3DX11EffectUnorderedAccessViewVariable**</span></span>](id3dx11effectunorderedaccessviewvariable.md) | <span data-ttu-id="ba89e-148">Zugreifen auf Daten in einer ungeordneten Zugriffs Ansicht.</span><span class="sxs-lookup"><span data-stu-id="ba89e-148">Access data in an unordered access view.</span></span>            |



 

### <a name="setting-other-effect-variables"></a><span data-ttu-id="ba89e-149">Festlegen anderer Effekt Variablen</span><span class="sxs-lookup"><span data-stu-id="ba89e-149">Setting Other Effect Variables</span></span>

<span data-ttu-id="ba89e-150">Verwenden Sie diese Schnittstellen, um den Status anhand des Variablen Typs zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ba89e-150">Use these interfaces to get and set state by the variable type.</span></span>



| <span data-ttu-id="ba89e-151">Reflektionseschnittstellen</span><span class="sxs-lookup"><span data-stu-id="ba89e-151">Reflection Interfaces</span></span>                                                            | <span data-ttu-id="ba89e-152">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba89e-152">Description</span></span>               |
|----------------------------------------------------------------------------------|---------------------------|
| [<span data-ttu-id="ba89e-153">**ID3DX11EffectClassInstanceVariable**</span><span class="sxs-lookup"><span data-stu-id="ba89e-153">**ID3DX11EffectClassInstanceVariable**</span></span>](id3dx11effectclassinstancevariable.md) | <span data-ttu-id="ba89e-154">Eine Klasseninstanz erhalten.</span><span class="sxs-lookup"><span data-stu-id="ba89e-154">Get a class instance.</span></span>     |
| [<span data-ttu-id="ba89e-155">**ID3DX11EffectInterfaceVariable**</span><span class="sxs-lookup"><span data-stu-id="ba89e-155">**ID3DX11EffectInterfaceVariable**</span></span>](id3dx11effectinterfacevariable.md)         | <span data-ttu-id="ba89e-156">Sie erhalten eine Schnittstelle und legen Sie fest.</span><span class="sxs-lookup"><span data-stu-id="ba89e-156">Get and set an interface.</span></span> |
| [<span data-ttu-id="ba89e-157">**ID3DX11EffectMatrixVariable**</span><span class="sxs-lookup"><span data-stu-id="ba89e-157">**ID3DX11EffectMatrixVariable**</span></span>](id3dx11effectmatrixvariable.md)               | <span data-ttu-id="ba89e-158">Gibt eine Matrix an und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="ba89e-158">Get and set a matrix.</span></span>     |
| [<span data-ttu-id="ba89e-159">**ID3DX11EffectScalarVariable**</span><span class="sxs-lookup"><span data-stu-id="ba89e-159">**ID3DX11EffectScalarVariable**</span></span>](id3dx11effectscalarvariable.md)               | <span data-ttu-id="ba89e-160">Ein Skalarwert wird abgerufen und festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ba89e-160">Get and set a scalar.</span></span>     |
| [<span data-ttu-id="ba89e-161">**ID3DX11EffectShaderVariable**</span><span class="sxs-lookup"><span data-stu-id="ba89e-161">**ID3DX11EffectShaderVariable**</span></span>](id3dx11effectshadervariable.md)               | <span data-ttu-id="ba89e-162">Eine shadervariable erhalten.</span><span class="sxs-lookup"><span data-stu-id="ba89e-162">Get a shader variable.</span></span>    |
| [<span data-ttu-id="ba89e-163">**ID3DX11EffectStringVariable**</span><span class="sxs-lookup"><span data-stu-id="ba89e-163">**ID3DX11EffectStringVariable**</span></span>](id3dx11effectstringvariable.md)               | <span data-ttu-id="ba89e-164">Gibt eine Zeichenfolge zurück und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="ba89e-164">Get and set a string.</span></span>     |
| [<span data-ttu-id="ba89e-165">**ID3DX11EffectType**</span><span class="sxs-lookup"><span data-stu-id="ba89e-165">**ID3DX11EffectType**</span></span>](id3dx11effecttype.md)                                   | <span data-ttu-id="ba89e-166">Einen Variablentyp erhalten.</span><span class="sxs-lookup"><span data-stu-id="ba89e-166">Get a variable type.</span></span>      |
| [<span data-ttu-id="ba89e-167">**ID3DX11EffectVectorVariable**</span><span class="sxs-lookup"><span data-stu-id="ba89e-167">**ID3DX11EffectVectorVariable**</span></span>](id3dx11effectvectorvariable.md)               | <span data-ttu-id="ba89e-168">Get und Set a Vector.</span><span class="sxs-lookup"><span data-stu-id="ba89e-168">Get and set a vector.</span></span>     |



 

<span data-ttu-id="ba89e-169">Alle Reflektionsobjekte werden von [**ID3DX11EffectVariable**](id3dx11effectvariable.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ba89e-169">All reflection interfaces derive from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba89e-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ba89e-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba89e-171">Effekte (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="ba89e-171">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[<span data-ttu-id="ba89e-172">Programmieranleitung für Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="ba89e-172">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 

 




