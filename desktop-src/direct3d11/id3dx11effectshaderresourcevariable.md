---
title: ID3DX11EffectShaderResourceVariable-Schnittstelle (D3dx11effect. h)
description: Eine Shader-Resource-Schnittstelle greift auf eine Shaderressource zu.
ms.assetid: 936a3439-1f7d-4fea-b124-1d6ead528250
keywords:
- ID3DX11EffectShaderResourceVariable-Schnittstelle Direct3D 11
- ID3DX11EffectShaderResourceVariable Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7abfc2bf29bf3ea5333bf9e7da6630a62c5747aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996298"
---
# <a name="id3dx11effectshaderresourcevariable-interface"></a><span data-ttu-id="58742-105">ID3DX11EffectShaderResourceVariable-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="58742-105">ID3DX11EffectShaderResourceVariable interface</span></span>

<span data-ttu-id="58742-106">Eine Shader-Resource-Schnittstelle greift auf eine Shaderressource zu.</span><span class="sxs-lookup"><span data-stu-id="58742-106">A shader-resource interface accesses a shader resource.</span></span>

## <a name="members"></a><span data-ttu-id="58742-107">Member</span><span class="sxs-lookup"><span data-stu-id="58742-107">Members</span></span>

<span data-ttu-id="58742-108">Die **ID3DX11EffectShaderResourceVariable** -Schnittstelle erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="58742-108">The **ID3DX11EffectShaderResourceVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="58742-109">**ID3DX11EffectShaderResourceVariable** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="58742-109">**ID3DX11EffectShaderResourceVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="58742-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="58742-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="58742-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="58742-111">Methods</span></span>

<span data-ttu-id="58742-112">Die **ID3DX11EffectShaderResourceVariable** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="58742-112">The **ID3DX11EffectShaderResourceVariable** interface has these methods.</span></span>



| <span data-ttu-id="58742-113">Methode</span><span class="sxs-lookup"><span data-stu-id="58742-113">Method</span></span>                                                                           | <span data-ttu-id="58742-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58742-114">Description</span></span>                                  |
|:---------------------------------------------------------------------------------|:---------------------------------------------|
| [<span data-ttu-id="58742-115">**GetResource**</span><span class="sxs-lookup"><span data-stu-id="58742-115">**GetResource**</span></span>](id3dx11effectshaderresourcevariable-getresource.md)           | <span data-ttu-id="58742-116">Eine Shaderressource erhalten.</span><span class="sxs-lookup"><span data-stu-id="58742-116">Get a shader resource.</span></span><br/>            |
| [<span data-ttu-id="58742-117">**Getresourcearray**</span><span class="sxs-lookup"><span data-stu-id="58742-117">**GetResourceArray**</span></span>](id3dx11effectshaderresourcevariable-getresourcearray.md) | <span data-ttu-id="58742-118">Ein Array von Shaderressourcen erhalten.</span><span class="sxs-lookup"><span data-stu-id="58742-118">Get an array of shader resources.</span></span><br/> |
| [<span data-ttu-id="58742-119">**Ziel Quelle**</span><span class="sxs-lookup"><span data-stu-id="58742-119">**SetResource**</span></span>](id3dx11effectshaderresourcevariable-setresource.md)           | <span data-ttu-id="58742-120">Legen Sie eine Shaderressource fest.</span><span class="sxs-lookup"><span data-stu-id="58742-120">Set a shader resource.</span></span><br/>            |
| [<span data-ttu-id="58742-121">**"Tartresourcearray"**</span><span class="sxs-lookup"><span data-stu-id="58742-121">**SetResourceArray**</span></span>](id3dx11effectshaderresourcevariable-setresourcearray.md) | <span data-ttu-id="58742-122">Legen Sie ein Array von Shaderressourcen fest.</span><span class="sxs-lookup"><span data-stu-id="58742-122">Set an array of shader resources.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="58742-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58742-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="58742-124">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="58742-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="58742-125">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="58742-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="58742-126">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="58742-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="58742-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="58742-127">Requirements</span></span>



| <span data-ttu-id="58742-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58742-128">Requirement</span></span> | <span data-ttu-id="58742-129">Wert</span><span class="sxs-lookup"><span data-stu-id="58742-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58742-130">Header</span><span class="sxs-lookup"><span data-stu-id="58742-130">Header</span></span><br/>  | <dl> <span data-ttu-id="58742-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="58742-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="58742-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="58742-132">Library</span></span><br/> | <dl> <span data-ttu-id="58742-133"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="58742-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58742-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="58742-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58742-135">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="58742-135">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="58742-136">Effekte 11-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="58742-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="58742-137">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="58742-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





