---
description: 'Das Effect-System definiert mehrere Schnittstellen zur Verwaltung des Wirkungs Zustands. Es gibt zwei Arten von Schnittstellen: solche, die von der Laufzeit verwendet werden, um einen Effekt und reflektionsschnittstellen zum erhalten und Festlegen von Effekt Variablen zu erzeugen.'
ms.assetid: 068d49d2-0e14-4080-9fee-20d984f22545
title: Effect-System Schnittstellen (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40b21d98bedaec65550343260e7c52e2df1c302
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126325"
---
# <a name="effect-system-interfaces-direct3d-10"></a><span data-ttu-id="b5b71-104">Effect-System Schnittstellen (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="b5b71-104">Effect System Interfaces (Direct3D 10)</span></span>

<span data-ttu-id="b5b71-105">Das Effect-System definiert mehrere Schnittstellen zur Verwaltung des Wirkungs Zustands.</span><span class="sxs-lookup"><span data-stu-id="b5b71-105">The effect system defines several interfaces for managing effect state.</span></span> <span data-ttu-id="b5b71-106">Es gibt zwei Arten von Schnittstellen: solche, die von der Laufzeit verwendet werden, um einen Effekt und reflektionsschnittstellen zum erhalten und Festlegen von Effekt Variablen zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="b5b71-106">There are two types of interfaces: those used by the runtime to render an effect and reflection interfaces for getting and setting effect variables.</span></span>

-   [<span data-ttu-id="b5b71-107">Lauf Zeit Schnittstellen von Effekten</span><span class="sxs-lookup"><span data-stu-id="b5b71-107">Effect Runtime Interfaces</span></span>](#effect-runtime-interfaces)
-   [<span data-ttu-id="b5b71-108">Effekt reflektionseschnittstellen</span><span class="sxs-lookup"><span data-stu-id="b5b71-108">Effect Reflection Interfaces</span></span>](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a><span data-ttu-id="b5b71-109">Lauf Zeit Schnittstellen von Effekten</span><span class="sxs-lookup"><span data-stu-id="b5b71-109">Effect Runtime Interfaces</span></span>

<span data-ttu-id="b5b71-110">Verwenden Sie Lauf Zeit Schnittstellen zum Rendering eines Effekts.</span><span class="sxs-lookup"><span data-stu-id="b5b71-110">Use runtime interfaces to render an effect.</span></span>



| <span data-ttu-id="b5b71-111">Lauf Zeit Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b5b71-111">Runtime Interfaces</span></span>                                               | <span data-ttu-id="b5b71-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5b71-112">Description</span></span>                                                          |
|------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="b5b71-113">**ID3D10Effect-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b5b71-113">**ID3D10Effect Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                   | <span data-ttu-id="b5b71-114">Sammlung von einer oder mehreren Techniken zum Rendern.</span><span class="sxs-lookup"><span data-stu-id="b5b71-114">Collection of one or more techniques for rendering.</span></span>                  |
| <span data-ttu-id="b5b71-115">[**ID3D10Include-Schnittstelle**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b5b71-115">[**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span></span>                 | <span data-ttu-id="b5b71-116">Eine Schnittstelle zum Hinzufügen benutzerdefinierter Verhalten beim Lesen von Includedateien.</span><span class="sxs-lookup"><span data-stu-id="b5b71-116">An interface for adding custom behaviors when reading include files.</span></span> |
| [<span data-ttu-id="b5b71-117">**ID3D10EffectPass-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b5b71-117">**ID3D10EffectPass Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)           | <span data-ttu-id="b5b71-118">Eine Auflistung von Zustands Zuweisungen.</span><span class="sxs-lookup"><span data-stu-id="b5b71-118">A collection of state assignments.</span></span>                                   |
| [<span data-ttu-id="b5b71-119">**ID3D10EffectPool-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b5b71-119">**ID3D10EffectPool Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)           | <span data-ttu-id="b5b71-120">Erstellen Sie einen Speicherort für Variablen, die zwischen Effekten gemeinsam verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b5b71-120">Create a memory location for variables to be shared between effects.</span></span> |
| [<span data-ttu-id="b5b71-121">**ID3D10EffectTechnique-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b5b71-121">**ID3D10EffectTechnique Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique) | <span data-ttu-id="b5b71-122">Eine Auflistung von einem oder mehreren Durchläufen.</span><span class="sxs-lookup"><span data-stu-id="b5b71-122">A collection of one or more passes.</span></span>                                  |



 

## <a name="effect-reflection-interfaces"></a><span data-ttu-id="b5b71-123">Effekt reflektionseschnittstellen</span><span class="sxs-lookup"><span data-stu-id="b5b71-123">Effect Reflection Interfaces</span></span>

<span data-ttu-id="b5b71-124">Reflektion wird im Effektsystem implementiert, um das Lesen (und schreiben) des Wirkungs Zustands zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b5b71-124">Reflection is implemented in the effect system to support reading (and writing) effect state.</span></span> <span data-ttu-id="b5b71-125">Es gibt mehrere Möglichkeiten, auf Wirkungs Variablen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="b5b71-125">There are multiple ways to access effect variables.</span></span>

### <a name="setting-groups-of-effect-state"></a><span data-ttu-id="b5b71-126">Festlegen von Gruppen von Effekt Zuständen</span><span class="sxs-lookup"><span data-stu-id="b5b71-126">Setting Groups of Effect State</span></span>

<span data-ttu-id="b5b71-127">Verwenden Sie diese Schnittstellen, um eine Gruppe des Zustands zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b5b71-127">Use these interfaces to get and set a group of state.</span></span>



| <span data-ttu-id="b5b71-128">Reflektionseschnittstellen</span><span class="sxs-lookup"><span data-stu-id="b5b71-128">Reflection Interfaces</span></span>                                                                  | <span data-ttu-id="b5b71-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5b71-129">Description</span></span>                      |
|----------------------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="b5b71-130">**ID3D10EffectBlendVariable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b5b71-130">**ID3D10EffectBlendVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)               | <span data-ttu-id="b5b71-131">Get-und Set-Blend-Zustand.</span><span class="sxs-lookup"><span data-stu-id="b5b71-131">Get and set blend state.</span></span>         |
| [<span data-ttu-id="b5b71-132">**ID3D10EffectDepthStencilVariable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b5b71-132">**ID3D10EffectDepthStencilVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable) | <span data-ttu-id="b5b71-133">Get und Set tiefen Schablone State.</span><span class="sxs-lookup"><span data-stu-id="b5b71-133">Get and set depth-stencil state.</span></span> |
| [<span data-ttu-id="b5b71-134">**ID3D10EffectRasterizerVariable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b5b71-134">**ID3D10EffectRasterizerVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)     | <span data-ttu-id="b5b71-135">Get-und Set-Status des Rasterizers.</span><span class="sxs-lookup"><span data-stu-id="b5b71-135">Get and set rasterizer state.</span></span>    |
| [<span data-ttu-id="b5b71-136">**ID3D10EffectSamplerVariable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b5b71-136">**ID3D10EffectSamplerVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)           | <span data-ttu-id="b5b71-137">Holen Sie sich den samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="b5b71-137">Get and set sampler state.</span></span>       |



 

### <a name="setting-effect-resources"></a><span data-ttu-id="b5b71-138">Festlegen von Effekt Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b5b71-138">Setting Effect Resources</span></span>

<span data-ttu-id="b5b71-139">Verwenden Sie diese Schnittstellen, um Ressourcen zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b5b71-139">Use these interfaces to get and set resources.</span></span>



| <span data-ttu-id="b5b71-140">Reflektionseschnittstellen</span><span class="sxs-lookup"><span data-stu-id="b5b71-140">Reflection Interfaces</span></span>                                                                          | <span data-ttu-id="b5b71-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5b71-141">Description</span></span>                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="b5b71-142">**ID3D10EffectConstantBuffer-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b5b71-142">**ID3D10EffectConstantBuffer Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | <span data-ttu-id="b5b71-143">Zugreifen auf Daten in einem Textur Puffer oder Konstantenpuffer.</span><span class="sxs-lookup"><span data-stu-id="b5b71-143">Access data in a texture buffer or constant buffer.</span></span> |
| [<span data-ttu-id="b5b71-144">**ID3D10EffectDepthStencilViewVariable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b5b71-144">**ID3D10EffectDepthStencilViewVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | <span data-ttu-id="b5b71-145">Zugreifen auf Daten in einer tiefen Schablone-Ressource.</span><span class="sxs-lookup"><span data-stu-id="b5b71-145">Access data in a depth-stencil resource.</span></span>            |
| [<span data-ttu-id="b5b71-146">**ID3D10EffectRenderTargetViewVariable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b5b71-146">**ID3D10EffectRenderTargetViewVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | <span data-ttu-id="b5b71-147">Zugreifen auf Daten in einem Renderziel.</span><span class="sxs-lookup"><span data-stu-id="b5b71-147">Access data in a render target.</span></span>                     |
| [<span data-ttu-id="b5b71-148">**ID3D10EffectShaderResourceVariable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b5b71-148">**ID3D10EffectShaderResourceVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | <span data-ttu-id="b5b71-149">Zugreifen auf Daten in einer Shaderressource.</span><span class="sxs-lookup"><span data-stu-id="b5b71-149">Access data in a shader resource.</span></span>                   |



 

### <a name="setting-other-effect-variables"></a><span data-ttu-id="b5b71-150">Festlegen anderer Effekt Variablen</span><span class="sxs-lookup"><span data-stu-id="b5b71-150">Setting Other Effect Variables</span></span>

<span data-ttu-id="b5b71-151">Verwenden Sie diese Schnittstellen, um den Status anhand des Variablen Typs zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b5b71-151">Use these interfaces to get and set state by the variable type.</span></span>



| <span data-ttu-id="b5b71-152">Reflektionseschnittstellen</span><span class="sxs-lookup"><span data-stu-id="b5b71-152">Reflection Interfaces</span></span>                                                      | <span data-ttu-id="b5b71-153">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5b71-153">Description</span></span>                    |
|----------------------------------------------------------------------------|--------------------------------|
| [<span data-ttu-id="b5b71-154">**ID3D10EffectMatrixVariable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b5b71-154">**ID3D10EffectMatrixVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable) | <span data-ttu-id="b5b71-155">Gibt eine Matrix an und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="b5b71-155">Get and set a matrix.</span></span>          |
| [<span data-ttu-id="b5b71-156">**ID3D10EffectScalarVariable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b5b71-156">**ID3D10EffectScalarVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable) | <span data-ttu-id="b5b71-157">Ein Skalarwert wird abgerufen und festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b5b71-157">Get and set a scalar.</span></span>          |
| [<span data-ttu-id="b5b71-158">**ID3D10EffectShaderVariable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b5b71-158">**ID3D10EffectShaderVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable) | <span data-ttu-id="b5b71-159">Get und Set a Shader Variable.</span><span class="sxs-lookup"><span data-stu-id="b5b71-159">Get and set a shader variable.</span></span> |
| [<span data-ttu-id="b5b71-160">**ID3D10EffectStringVariable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b5b71-160">**ID3D10EffectStringVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable) | <span data-ttu-id="b5b71-161">Gibt eine Zeichenfolge zurück und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="b5b71-161">Get and set a string.</span></span>          |
| [<span data-ttu-id="b5b71-162">**ID3D10EffectType-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b5b71-162">**ID3D10EffectType Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                     | <span data-ttu-id="b5b71-163">Einen Variablentyp erhalten.</span><span class="sxs-lookup"><span data-stu-id="b5b71-163">Get a variable type.</span></span>           |
| [<span data-ttu-id="b5b71-164">**ID3D10EffectVectorVariable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b5b71-164">**ID3D10EffectVectorVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable) | <span data-ttu-id="b5b71-165">Get und Set a Vector.</span><span class="sxs-lookup"><span data-stu-id="b5b71-165">Get and set a vector.</span></span>          |



 

<span data-ttu-id="b5b71-166">Alle Reflexions Schnittstellen werden von der [**ID3D10EffectVariable-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b5b71-166">All reflection interfaces derive from [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5b71-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b5b71-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5b71-168">Effekte</span><span class="sxs-lookup"><span data-stu-id="b5b71-168">Effects</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> <dt>

[<span data-ttu-id="b5b71-169">Programmier Handbuch für Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="b5b71-169">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
