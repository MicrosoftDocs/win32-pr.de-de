---
title: ID3DX11EffectShaderVariable-Schnittstelle (D3dx11effect. h)
description: Eine Shader-Variable-Schnittstelle greift auf eine Shader-Variable zu.
ms.assetid: e547a5e9-7b60-4a85-806d-272be55d12e7
keywords:
- ID3DX11EffectShaderVariable-Schnittstelle Direct3D 11
- ID3DX11EffectShaderVariable Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcbb011591f715b4bac57dfa34f640ea90278f6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995925"
---
# <a name="id3dx11effectshadervariable-interface"></a><span data-ttu-id="d30fe-105">ID3DX11EffectShaderVariable-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d30fe-105">ID3DX11EffectShaderVariable interface</span></span>

<span data-ttu-id="d30fe-106">Eine Shader-Variable-Schnittstelle greift auf eine Shader-Variable zu.</span><span class="sxs-lookup"><span data-stu-id="d30fe-106">A shader-variable interface accesses a shader variable.</span></span>

## <a name="members"></a><span data-ttu-id="d30fe-107">Member</span><span class="sxs-lookup"><span data-stu-id="d30fe-107">Members</span></span>

<span data-ttu-id="d30fe-108">Die **ID3DX11EffectShaderVariable** -Schnittstelle erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="d30fe-108">The **ID3DX11EffectShaderVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="d30fe-109">**ID3DX11EffectShaderVariable** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d30fe-109">**ID3DX11EffectShaderVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="d30fe-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="d30fe-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d30fe-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="d30fe-111">Methods</span></span>

<span data-ttu-id="d30fe-112">Die **ID3DX11EffectShaderVariable** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d30fe-112">The **ID3DX11EffectShaderVariable** interface has these methods.</span></span>



| <span data-ttu-id="d30fe-113">Methode</span><span class="sxs-lookup"><span data-stu-id="d30fe-113">Method</span></span>                                                                                                           | <span data-ttu-id="d30fe-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d30fe-114">Description</span></span>                                            |
|:-----------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="d30fe-115">**Getcomputeshader**</span><span class="sxs-lookup"><span data-stu-id="d30fe-115">**GetComputeShader**</span></span>](id3dx11effectshadervariable-getcomputeshader.md)                                         | <span data-ttu-id="d30fe-116">Einen Compute-Shader erhalten.</span><span class="sxs-lookup"><span data-stu-id="d30fe-116">Get a compute shader.</span></span><br/>                       |
| [<span data-ttu-id="d30fe-117">**Getdomainshader**</span><span class="sxs-lookup"><span data-stu-id="d30fe-117">**GetDomainShader**</span></span>](id3dx11effectshadervariable-getdomainshader.md)                                           | <span data-ttu-id="d30fe-118">Einen Domänen-Shader erhalten.</span><span class="sxs-lookup"><span data-stu-id="d30fe-118">Get a domain shader.</span></span><br/>                        |
| [<span data-ttu-id="d30fe-119">**Getgeometryshader**</span><span class="sxs-lookup"><span data-stu-id="d30fe-119">**GetGeometryShader**</span></span>](id3dx11effectshadervariable-getgeometryshader.md)                                       | <span data-ttu-id="d30fe-120">Einen Geometry-Shader erhalten.</span><span class="sxs-lookup"><span data-stu-id="d30fe-120">Get a geometry shader.</span></span><br/>                      |
| [<span data-ttu-id="d30fe-121">**Gethullshader**</span><span class="sxs-lookup"><span data-stu-id="d30fe-121">**GetHullShader**</span></span>](id3dx11effectshadervariable-gethullshader.md)                                               | <span data-ttu-id="d30fe-122">Einen Hull-Shader erhalten.</span><span class="sxs-lookup"><span data-stu-id="d30fe-122">Get a hull shader.</span></span><br/>                          |
| [<span data-ttu-id="d30fe-123">**GetInputSignatureElementDesc**</span><span class="sxs-lookup"><span data-stu-id="d30fe-123">**GetInputSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getinputsignatureelementdesc.md)                 | <span data-ttu-id="d30fe-124">Erhalten Sie eine Beschreibung der Eingabe Signatur.</span><span class="sxs-lookup"><span data-stu-id="d30fe-124">Get an input-signature description.</span></span><br/>         |
| [<span data-ttu-id="d30fe-125">**GetOutputSignatureElementDesc**</span><span class="sxs-lookup"><span data-stu-id="d30fe-125">**GetOutputSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getoutputsignatureelementdesc.md)               | <span data-ttu-id="d30fe-126">Hier erhalten Sie eine Beschreibung der Ausgabe Signatur.</span><span class="sxs-lookup"><span data-stu-id="d30fe-126">Get an output-signature description.</span></span><br/>        |
| [<span data-ttu-id="d30fe-127">**GetPatchConstantSignatureElementDesc**</span><span class="sxs-lookup"><span data-stu-id="d30fe-127">**GetPatchConstantSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getpatchconstantsignatureelementdesc.md) | <span data-ttu-id="d30fe-128">Hier erhalten Sie eine Beschreibung für eine patchkonstante Signatur.</span><span class="sxs-lookup"><span data-stu-id="d30fe-128">Get a patch constant signature description.</span></span><br/> |
| [<span data-ttu-id="d30fe-129">**Getpixelshader**</span><span class="sxs-lookup"><span data-stu-id="d30fe-129">**GetPixelShader**</span></span>](id3dx11effectshadervariable-getpixelshader.md)                                             | <span data-ttu-id="d30fe-130">Einen PixelShader erhalten.</span><span class="sxs-lookup"><span data-stu-id="d30fe-130">Get a pixel shader.</span></span><br/>                         |
| [<span data-ttu-id="d30fe-131">**Getshaderdebug**</span><span class="sxs-lookup"><span data-stu-id="d30fe-131">**GetShaderDesc**</span></span>](id3dx11effectshadervariable-getshaderdesc.md)                                               | <span data-ttu-id="d30fe-132">Eine shaderbeschreibung erhalten.</span><span class="sxs-lookup"><span data-stu-id="d30fe-132">Get a shader description.</span></span><br/>                   |
| [<span data-ttu-id="d30fe-133">**Getvertexshader**</span><span class="sxs-lookup"><span data-stu-id="d30fe-133">**GetVertexShader**</span></span>](id3dx11effectshadervariable-getvertexshader.md)                                           | <span data-ttu-id="d30fe-134">Einen Vertex-Shader erhalten.</span><span class="sxs-lookup"><span data-stu-id="d30fe-134">Get a vertex shader.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="d30fe-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d30fe-135">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d30fe-136">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="d30fe-136">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d30fe-137">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d30fe-137">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d30fe-138">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d30fe-138">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d30fe-139">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d30fe-139">Requirements</span></span>



| <span data-ttu-id="d30fe-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d30fe-140">Requirement</span></span> | <span data-ttu-id="d30fe-141">Wert</span><span class="sxs-lookup"><span data-stu-id="d30fe-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d30fe-142">Header</span><span class="sxs-lookup"><span data-stu-id="d30fe-142">Header</span></span><br/>  | <dl> <span data-ttu-id="d30fe-143"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d30fe-143"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d30fe-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d30fe-144">Library</span></span><br/> | <dl> <span data-ttu-id="d30fe-145"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="d30fe-145"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d30fe-146">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d30fe-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d30fe-147">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="d30fe-147">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="d30fe-148">Effekte 11-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d30fe-148">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="d30fe-149">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d30fe-149">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





