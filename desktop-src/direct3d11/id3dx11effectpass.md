---
title: ID3DX11EffectPass-Schnittstelle (D3dx11effect. h)
description: Eine ID3DX11EffectPass-Schnittstelle kapselt Zustands Zuweisungen innerhalb eines Verfahrens. Die Lebensdauer eines ID3DX11EffectPass-Objekts entspricht der Lebensdauer seines übergeordneten ID3DX11Effect-Objekts.
ms.assetid: 4d86c362-b0f8-4396-86de-c7c89710f46d
keywords:
- ID3DX11EffectPass-Schnittstelle Direct3D 11
- ID3DX11EffectPass Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectPass
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a26732543d1033cfc439755df6ac397d2a28ec1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219648"
---
# <a name="id3dx11effectpass-interface"></a><span data-ttu-id="50baf-105">ID3DX11EffectPass-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="50baf-105">ID3DX11EffectPass interface</span></span>

<span data-ttu-id="50baf-106">Eine **ID3DX11EffectPass** -Schnittstelle kapselt Zustands Zuweisungen innerhalb eines Verfahrens.</span><span class="sxs-lookup"><span data-stu-id="50baf-106">An **ID3DX11EffectPass** interface encapsulates state assignments within a technique.</span></span>

<span data-ttu-id="50baf-107">Die Lebensdauer eines **ID3DX11EffectPass** -Objekts entspricht der Lebensdauer seines übergeordneten [**ID3DX11Effect**](id3dx11effect.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="50baf-107">The lifetime of an **ID3DX11EffectPass** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="50baf-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="50baf-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="50baf-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="50baf-109">Methods</span></span>

<span data-ttu-id="50baf-110">Die **ID3DX11EffectPass** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="50baf-110">The **ID3DX11EffectPass** interface has these methods.</span></span>



| <span data-ttu-id="50baf-111">Methode</span><span class="sxs-lookup"><span data-stu-id="50baf-111">Method</span></span>                                                                   | <span data-ttu-id="50baf-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50baf-112">Description</span></span>                                                       |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="50baf-113">**Anwenden**</span><span class="sxs-lookup"><span data-stu-id="50baf-113">**Apply**</span></span>](id3dx11effectpass-apply.md)                                 | <span data-ttu-id="50baf-114">Legen Sie den in einem Pass enthaltenen Status auf das Gerät fest.</span><span class="sxs-lookup"><span data-stu-id="50baf-114">Set the state contained in a pass to the device.</span></span><br/>       |
| [<span data-ttu-id="50baf-115">**Computestateblockmask**</span><span class="sxs-lookup"><span data-stu-id="50baf-115">**ComputeStateBlockMask**</span></span>](id3dx11effectpass-computestateblockmask.md) | <span data-ttu-id="50baf-116">Generiert eine Maske zum zulassen/verhindern von Zustandsänderungen.</span><span class="sxs-lookup"><span data-stu-id="50baf-116">Generate a mask for allowing/preventing state changes.</span></span><br/> |
| [<span data-ttu-id="50baf-117">**Getannotationbyindex**</span><span class="sxs-lookup"><span data-stu-id="50baf-117">**GetAnnotationByIndex**</span></span>](id3dx11effectpass-getannotationbyindex.md)   | <span data-ttu-id="50baf-118">Eine Anmerkung nach Index erhalten.</span><span class="sxs-lookup"><span data-stu-id="50baf-118">Get an annotation by index.</span></span><br/>                            |
| [<span data-ttu-id="50baf-119">**Getannotationbyname**</span><span class="sxs-lookup"><span data-stu-id="50baf-119">**GetAnnotationByName**</span></span>](id3dx11effectpass-getannotationbyname.md)     | <span data-ttu-id="50baf-120">Eine Anmerkung anhand des Namens erhalten.</span><span class="sxs-lookup"><span data-stu-id="50baf-120">Get an annotation by name.</span></span><br/>                             |
| [<span data-ttu-id="50baf-121">**Getcomputeshaderentsc**</span><span class="sxs-lookup"><span data-stu-id="50baf-121">**GetComputeShaderDesc**</span></span>](id3dx11effectpass-getcomputeshaderdesc.md)   | <span data-ttu-id="50baf-122">Eine COMPUTE-shaderbeschreibung erhalten.</span><span class="sxs-lookup"><span data-stu-id="50baf-122">Get a compute-shader description.</span></span><br/>                      |
| [<span data-ttu-id="50baf-123">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="50baf-123">**GetDesc**</span></span>](id3dx11effectpass-getdesc.md)                             | <span data-ttu-id="50baf-124">Eine Pass Beschreibung erhalten.</span><span class="sxs-lookup"><span data-stu-id="50baf-124">Get a pass description.</span></span><br/>                                |
| [<span data-ttu-id="50baf-125">**Getdomainshaderdebug**</span><span class="sxs-lookup"><span data-stu-id="50baf-125">**GetDomainShaderDesc**</span></span>](id3dx11effectpass-getdomainshaderdesc.md)     | <span data-ttu-id="50baf-126">Eine Domänen-Shader-Beschreibung erhalten.</span><span class="sxs-lookup"><span data-stu-id="50baf-126">Get a domain-shader description.</span></span><br/>                       |
| [<span data-ttu-id="50baf-127">**Getgeometryshaderdebug**</span><span class="sxs-lookup"><span data-stu-id="50baf-127">**GetGeometryShaderDesc**</span></span>](id3dx11effectpass-getgeometryshaderdesc.md) | <span data-ttu-id="50baf-128">Eine Geometry-shaderbeschreibung erhalten.</span><span class="sxs-lookup"><span data-stu-id="50baf-128">Get a geometry-shader description.</span></span><br/>                     |
| [<span data-ttu-id="50baf-129">**Gethullshaderdebug**</span><span class="sxs-lookup"><span data-stu-id="50baf-129">**GetHullShaderDesc**</span></span>](id3dx11effectpass-gethullshaderdesc.md)         | <span data-ttu-id="50baf-130">Die Beschreibung von "Hull-Shader" wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="50baf-130">Get hull-shader description.</span></span><br/>                           |
| [<span data-ttu-id="50baf-131">**Getpixelshaderdebug**</span><span class="sxs-lookup"><span data-stu-id="50baf-131">**GetPixelShaderDesc**</span></span>](id3dx11effectpass-getpixelshaderdesc.md)       | <span data-ttu-id="50baf-132">Eine Pixel-shaderbeschreibung erhalten.</span><span class="sxs-lookup"><span data-stu-id="50baf-132">Get a pixel-shader description.</span></span><br/>                        |
| [<span data-ttu-id="50baf-133">**Getvertexshaderdebug**</span><span class="sxs-lookup"><span data-stu-id="50baf-133">**GetVertexShaderDesc**</span></span>](id3dx11effectpass-getvertexshaderdesc.md)     | <span data-ttu-id="50baf-134">Eine Vertex-shaderbeschreibung erhalten.</span><span class="sxs-lookup"><span data-stu-id="50baf-134">Get a vertex-shader description.</span></span><br/>                       |
| [<span data-ttu-id="50baf-135">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="50baf-135">**IsValid**</span></span>](id3dx11effectpass-isvalid.md)                             | <span data-ttu-id="50baf-136">Testen Sie einen Durchlauf, um festzustellen, ob er eine gültige Syntax enthält.</span><span class="sxs-lookup"><span data-stu-id="50baf-136">Test a pass to see if it contains valid syntax.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="50baf-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50baf-137">Remarks</span></span>

<span data-ttu-id="50baf-138">Ein Durchlauf ist ein Codeblock, der renderstatusobjekte und Shader festlegt.</span><span class="sxs-lookup"><span data-stu-id="50baf-138">A pass is a block of code that sets render-state objects and shaders.</span></span> <span data-ttu-id="50baf-139">Ein Durchlauf wird innerhalb einer Technik deklariert.</span><span class="sxs-lookup"><span data-stu-id="50baf-139">A pass is declared within a technique.</span></span>

<span data-ttu-id="50baf-140">Um eine Effect-Pass-Schnittstelle zu erhalten, müssen Sie eine Methode wie [**ID3DX11EffectTechnique:: getpassbyname**](id3dx11effecttechnique-getpassbyname.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="50baf-140">To get an effect-pass interface, call a method like [**ID3DX11EffectTechnique::GetPassByName**](id3dx11effecttechnique-getpassbyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="50baf-141">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="50baf-141">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="50baf-142">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="50baf-142">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="50baf-143">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="50baf-143">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="50baf-144">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="50baf-144">Requirements</span></span>



| <span data-ttu-id="50baf-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50baf-145">Requirement</span></span> | <span data-ttu-id="50baf-146">Wert</span><span class="sxs-lookup"><span data-stu-id="50baf-146">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50baf-147">Header</span><span class="sxs-lookup"><span data-stu-id="50baf-147">Header</span></span><br/>  | <dl> <span data-ttu-id="50baf-148"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="50baf-148"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="50baf-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="50baf-149">Library</span></span><br/> | <dl> <span data-ttu-id="50baf-150"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="50baf-150"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50baf-151">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="50baf-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50baf-152">Effekte 11-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="50baf-152">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="50baf-153">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="50baf-153">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





