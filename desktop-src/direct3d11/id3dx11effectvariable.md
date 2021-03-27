---
title: ID3DX11EffectVariable-Schnittstelle (D3dx11effect. h)
description: Die ID3DX11EffectVariable-Schnittstelle ist die Basisklasse für alle Effekt Variablen. Die Lebensdauer eines ID3DX11EffectVariable-Objekts entspricht der Lebensdauer seines übergeordneten ID3DX11Effect-Objekts.
ms.assetid: 07f1b7d7-c266-49ae-b79a-7a645521df89
keywords:
- ID3DX11EffectVariable-Schnittstelle Direct3D 11
- ID3DX11EffectVariable Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df38a12c54776072bb922ffc4cd5bcd0d79776
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762198"
---
# <a name="id3dx11effectvariable-interface"></a><span data-ttu-id="28ac0-105">ID3DX11EffectVariable-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="28ac0-105">ID3DX11EffectVariable interface</span></span>

<span data-ttu-id="28ac0-106">Die **ID3DX11EffectVariable** -Schnittstelle ist die Basisklasse für alle Effekt Variablen.</span><span class="sxs-lookup"><span data-stu-id="28ac0-106">The **ID3DX11EffectVariable** interface is the base class for all effect variables.</span></span>

<span data-ttu-id="28ac0-107">Die Lebensdauer eines **ID3DX11EffectVariable** -Objekts entspricht der Lebensdauer seines übergeordneten [**ID3DX11Effect**](id3dx11effect.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="28ac0-107">The lifetime of an **ID3DX11EffectVariable** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="28ac0-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="28ac0-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="28ac0-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="28ac0-109">Methods</span></span>

<span data-ttu-id="28ac0-110">Die **ID3DX11EffectVariable** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="28ac0-110">The **ID3DX11EffectVariable** interface has these methods.</span></span>



| <span data-ttu-id="28ac0-111">Methode</span><span class="sxs-lookup"><span data-stu-id="28ac0-111">Method</span></span>                                                                           | <span data-ttu-id="28ac0-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28ac0-112">Description</span></span>                                            |
|:---------------------------------------------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="28ac0-113">**Asblend**</span><span class="sxs-lookup"><span data-stu-id="28ac0-113">**AsBlend**</span></span>](id3dx11effectvariable-asblend.md)                                 | <span data-ttu-id="28ac0-114">Eine Effect-Blend-Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-114">Get a effect-blend variable.</span></span><br/>                |
| [<span data-ttu-id="28ac0-115">**Asclassinstance**</span><span class="sxs-lookup"><span data-stu-id="28ac0-115">**AsClassInstance**</span></span>](id3dx11effectvariable-asclassinstance.md)                 | <span data-ttu-id="28ac0-116">Eine Klasseninstanz-Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-116">Get a class-instance variable.</span></span><br/>              |
| [<span data-ttu-id="28ac0-117">**Asconstantbuffer**</span><span class="sxs-lookup"><span data-stu-id="28ac0-117">**AsConstantBuffer**</span></span>](id3dx11effectvariable-asconstantbuffer.md)               | <span data-ttu-id="28ac0-118">Einen konstanten Puffer erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-118">Get a constant buffer.</span></span><br/>                      |
| [<span data-ttu-id="28ac0-119">**Asdepthstencil**</span><span class="sxs-lookup"><span data-stu-id="28ac0-119">**AsDepthStencil**</span></span>](id3dx11effectvariable-asdepthstencil.md)                   | <span data-ttu-id="28ac0-120">Eine tiefen Schablone-Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-120">Get a depth-stencil variable.</span></span><br/>               |
| [<span data-ttu-id="28ac0-121">**Asdepthstencilview**</span><span class="sxs-lookup"><span data-stu-id="28ac0-121">**AsDepthStencilView**</span></span>](id3dx11effectvariable-asdepthstencilview.md)           | <span data-ttu-id="28ac0-122">Eine tiefen Schablone-Ansichts Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-122">Get a depth-stencil-view variable.</span></span><br/>          |
| [<span data-ttu-id="28ac0-123">**Asinterface**</span><span class="sxs-lookup"><span data-stu-id="28ac0-123">**AsInterface**</span></span>](id3dx11effectvariable-asinterface.md)                         | <span data-ttu-id="28ac0-124">Eine Schnittstellen Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-124">Get an interface variable.</span></span><br/>                  |
| [<span data-ttu-id="28ac0-125">**Asmatrix**</span><span class="sxs-lookup"><span data-stu-id="28ac0-125">**AsMatrix**</span></span>](id3dx11effectvariable-asmatrix.md)                               | <span data-ttu-id="28ac0-126">Eine Matrix Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-126">Get a matrix variable.</span></span><br/>                      |
| [<span data-ttu-id="28ac0-127">**Asrasterizer**</span><span class="sxs-lookup"><span data-stu-id="28ac0-127">**AsRasterizer**</span></span>](id3dx11effectvariable-asrasterizer.md)                       | <span data-ttu-id="28ac0-128">Eine Raster-Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-128">Get a rasterizer variable.</span></span><br/>                  |
| [<span data-ttu-id="28ac0-129">**Asrendertargetview**</span><span class="sxs-lookup"><span data-stu-id="28ac0-129">**AsRenderTargetView**</span></span>](id3dx11effectvariable-asrendertargetview.md)           | <span data-ttu-id="28ac0-130">Eine "Rendering-Target-View"-Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-130">Get a render-target-view variable.</span></span><br/>          |
| [<span data-ttu-id="28ac0-131">**Assampler**</span><span class="sxs-lookup"><span data-stu-id="28ac0-131">**AsSampler**</span></span>](id3dx11effectvariable-assampler.md)                             | <span data-ttu-id="28ac0-132">Eine samplervariable erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-132">Get a sampler variable.</span></span><br/>                     |
| [<span data-ttu-id="28ac0-133">**Asscalar**</span><span class="sxs-lookup"><span data-stu-id="28ac0-133">**AsScalar**</span></span>](id3dx11effectvariable-asscalar.md)                               | <span data-ttu-id="28ac0-134">Eine skalare Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-134">Get a scalar variable.</span></span><br/>                      |
| [<span data-ttu-id="28ac0-135">**Asshader**</span><span class="sxs-lookup"><span data-stu-id="28ac0-135">**AsShader**</span></span>](id3dx11effectvariable-asshader.md)                               | <span data-ttu-id="28ac0-136">Eine shadervariable erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-136">Get a shader variable.</span></span><br/>                      |
| [<span data-ttu-id="28ac0-137">**Asshaderresource**</span><span class="sxs-lookup"><span data-stu-id="28ac0-137">**AsShaderResource**</span></span>](id3dx11effectvariable-asshaderresource.md)               | <span data-ttu-id="28ac0-138">Eine Shader-Resource-Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-138">Get a shader-resource variable.</span></span><br/>             |
| [<span data-ttu-id="28ac0-139">**AsString**</span><span class="sxs-lookup"><span data-stu-id="28ac0-139">**AsString**</span></span>](id3dx11effectvariable-asstring.md)                               | <span data-ttu-id="28ac0-140">Eine Zeichen folgen Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-140">Get a string variable.</span></span><br/>                      |
| [<span data-ttu-id="28ac0-141">**Asunorderedaccessview**</span><span class="sxs-lookup"><span data-stu-id="28ac0-141">**AsUnorderedAccessView**</span></span>](id3dx11effectvariable-asunorderedaccessview.md)     | <span data-ttu-id="28ac0-142">Abrufen einer Variablen mit ungeordneter Zugriffs Sicht.</span><span class="sxs-lookup"><span data-stu-id="28ac0-142">Get an unordered-access-view variable.</span></span><br/>      |
| [<span data-ttu-id="28ac0-143">**Asvector**</span><span class="sxs-lookup"><span data-stu-id="28ac0-143">**AsVector**</span></span>](id3dx11effectvariable-asvector.md)                               | <span data-ttu-id="28ac0-144">Eine Vektor Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-144">Get a vector variable.</span></span><br/>                      |
| [<span data-ttu-id="28ac0-145">**Getannotationbyindex**</span><span class="sxs-lookup"><span data-stu-id="28ac0-145">**GetAnnotationByIndex**</span></span>](id3dx11effectvariable-getannotationbyindex.md)       | <span data-ttu-id="28ac0-146">Eine Anmerkung nach Index erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-146">Get an annotation by index.</span></span><br/>                 |
| [<span data-ttu-id="28ac0-147">**Getannotationbyname**</span><span class="sxs-lookup"><span data-stu-id="28ac0-147">**GetAnnotationByName**</span></span>](id3dx11effectvariable-getannotationbyname.md)         | <span data-ttu-id="28ac0-148">Eine Anmerkung anhand des Namens erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-148">Get an annotation by name.</span></span><br/>                  |
| [<span data-ttu-id="28ac0-149">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="28ac0-149">**GetDesc**</span></span>](id3dx11effectvariable-getdesc.md)                                 | <span data-ttu-id="28ac0-150">Hier erhalten Sie eine Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="28ac0-150">Get a description.</span></span><br/>                          |
| [<span data-ttu-id="28ac0-151">**GetElement**</span><span class="sxs-lookup"><span data-stu-id="28ac0-151">**GetElement**</span></span>](id3dx11effectvariable-getelement.md)                           | <span data-ttu-id="28ac0-152">Ein Array Element erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-152">Get an array element.</span></span><br/>                       |
| [<span data-ttu-id="28ac0-153">**Getmembership byindex**</span><span class="sxs-lookup"><span data-stu-id="28ac0-153">**GetMemberByIndex**</span></span>](id3dx11effectvariable-getmemberbyindex.md)               | <span data-ttu-id="28ac0-154">Einen Strukturmember nach Index erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-154">Get a structure member by index.</span></span><br/>            |
| [<span data-ttu-id="28ac0-155">**Getmembership byname**</span><span class="sxs-lookup"><span data-stu-id="28ac0-155">**GetMemberByName**</span></span>](id3dx11effectvariable-getmemberbyname.md)                 | <span data-ttu-id="28ac0-156">Einen Strukturmember anhand des Namens erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-156">Get a structure member by name.</span></span><br/>             |
| [<span data-ttu-id="28ac0-157">**Getmembership bysemantic**</span><span class="sxs-lookup"><span data-stu-id="28ac0-157">**GetMemberBySemantic**</span></span>](id3dx11effectvariable-getmemberbysemantic.md)         | <span data-ttu-id="28ac0-158">Einen Strukturmember nach Semantik erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-158">Get a structure member by semantic.</span></span><br/>         |
| [<span data-ttu-id="28ac0-159">**Getparametenconstantbuffer**</span><span class="sxs-lookup"><span data-stu-id="28ac0-159">**GetParentConstantBuffer**</span></span>](id3dx11effectvariable-getparentconstantbuffer.md) | <span data-ttu-id="28ac0-160">Einen konstanten Puffer erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-160">Get a constant buffer.</span></span><br/>                      |
| [<span data-ttu-id="28ac0-161">**Getrawvalue**</span><span class="sxs-lookup"><span data-stu-id="28ac0-161">**GetRawValue**</span></span>](id3dx11effectvariable-getrawvalue.md)                         | <span data-ttu-id="28ac0-162">Abrufen von Daten</span><span class="sxs-lookup"><span data-stu-id="28ac0-162">Get data.</span></span><br/>                                   |
| [<span data-ttu-id="28ac0-163">**GetType**</span><span class="sxs-lookup"><span data-stu-id="28ac0-163">**GetType**</span></span>](id3dx11effectvariable-gettype.md)                                 | <span data-ttu-id="28ac0-164">Typinformationen erhalten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-164">Get type information.</span></span><br/>                       |
| [<span data-ttu-id="28ac0-165">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="28ac0-165">**IsValid**</span></span>](id3dx11effectvariable-isvalid.md)                                 | <span data-ttu-id="28ac0-166">Vergleichen Sie den Datentyp mit den gespeicherten Daten.</span><span class="sxs-lookup"><span data-stu-id="28ac0-166">Compare the data type with the data stored.</span></span><br/> |
| [<span data-ttu-id="28ac0-167">**"Strawvalue"**</span><span class="sxs-lookup"><span data-stu-id="28ac0-167">**SetRawValue**</span></span>](id3dx11effectvariable-setrawvalue.md)                         | <span data-ttu-id="28ac0-168">Legen Sie Daten fest.</span><span class="sxs-lookup"><span data-stu-id="28ac0-168">Set data.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="28ac0-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28ac0-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="28ac0-170">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="28ac0-170">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="28ac0-171">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="28ac0-171">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="28ac0-172">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="28ac0-172">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="28ac0-173">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="28ac0-173">Requirements</span></span>



| <span data-ttu-id="28ac0-174">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28ac0-174">Requirement</span></span> | <span data-ttu-id="28ac0-175">Wert</span><span class="sxs-lookup"><span data-stu-id="28ac0-175">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28ac0-176">Header</span><span class="sxs-lookup"><span data-stu-id="28ac0-176">Header</span></span><br/>  | <dl> <span data-ttu-id="28ac0-177"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="28ac0-177"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="28ac0-178">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="28ac0-178">Library</span></span><br/> | <dl> <span data-ttu-id="28ac0-179"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="28ac0-179"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28ac0-180">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="28ac0-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28ac0-181">Effekte 11-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="28ac0-181">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="28ac0-182">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="28ac0-182">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





