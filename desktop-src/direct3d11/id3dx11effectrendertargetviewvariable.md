---
title: ID3DX11EffectRenderTargetViewVariable-Schnittstelle (D3dx11effect. h)
description: Eine Renderziel-View-Schnittstelle greift auf ein Renderziel zu.
ms.assetid: 35c4e1da-05a8-4f1c-8730-58e3c90ad213
keywords:
- ID3DX11EffectRenderTargetViewVariable-Schnittstelle Direct3D 11
- ID3DX11EffectRenderTargetViewVariable Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5b20f83639fd973016bbe263d9d21dae7b295c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982203"
---
# <a name="id3dx11effectrendertargetviewvariable-interface"></a><span data-ttu-id="63f6d-105">ID3DX11EffectRenderTargetViewVariable-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="63f6d-105">ID3DX11EffectRenderTargetViewVariable interface</span></span>

<span data-ttu-id="63f6d-106">Eine Renderziel-View-Schnittstelle greift auf ein Renderziel zu.</span><span class="sxs-lookup"><span data-stu-id="63f6d-106">A render-target-view interface accesses a render target.</span></span>

## <a name="members"></a><span data-ttu-id="63f6d-107">Member</span><span class="sxs-lookup"><span data-stu-id="63f6d-107">Members</span></span>

<span data-ttu-id="63f6d-108">Die **ID3DX11EffectRenderTargetViewVariable** -Schnittstelle erbt von [**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="63f6d-108">The **ID3DX11EffectRenderTargetViewVariable** interface inherits from [**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="63f6d-109">**ID3DX11EffectRenderTargetViewVariable** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="63f6d-109">**ID3DX11EffectRenderTargetViewVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="63f6d-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="63f6d-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="63f6d-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="63f6d-111">Methods</span></span>

<span data-ttu-id="63f6d-112">Die **ID3DX11EffectRenderTargetViewVariable** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="63f6d-112">The **ID3DX11EffectRenderTargetViewVariable** interface has these methods.</span></span>



| <span data-ttu-id="63f6d-113">Methode</span><span class="sxs-lookup"><span data-stu-id="63f6d-113">Method</span></span>                                                                                     | <span data-ttu-id="63f6d-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63f6d-114">Description</span></span>                                |
|:-------------------------------------------------------------------------------------------|:-------------------------------------------|
| [<span data-ttu-id="63f6d-115">**GetRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="63f6d-115">**GetRenderTarget**</span></span>](id3dx11effectrendertargetviewvariable-getrendertarget.md)           | <span data-ttu-id="63f6d-116">Renderziel.</span><span class="sxs-lookup"><span data-stu-id="63f6d-116">Get a render-target.</span></span><br/>            |
| [<span data-ttu-id="63f6d-117">**GetRenderTargetArray**</span><span class="sxs-lookup"><span data-stu-id="63f6d-117">**GetRenderTargetArray**</span></span>](id3dx11effectrendertargetviewvariable-getrendertargetarray.md) | <span data-ttu-id="63f6d-118">Ein Array von renderzielen erhalten.</span><span class="sxs-lookup"><span data-stu-id="63f6d-118">Get an array of render-targets.</span></span><br/> |
| [<span data-ttu-id="63f6d-119">**"Zielort"**</span><span class="sxs-lookup"><span data-stu-id="63f6d-119">**SetRenderTarget**</span></span>](id3dx11effectrendertargetviewvariable-setrendertarget.md)           | <span data-ttu-id="63f6d-120">Legen Sie ein Renderziel fest.</span><span class="sxs-lookup"><span data-stu-id="63f6d-120">Set a render-target.</span></span><br/>            |
| [<span data-ttu-id="63f6d-121">**"Tartrendertargetarray"**</span><span class="sxs-lookup"><span data-stu-id="63f6d-121">**SetRenderTargetArray**</span></span>](id3dx11effectrendertargetviewvariable-setrendertargetarray.md) | <span data-ttu-id="63f6d-122">Legen Sie ein Array von Renderingzielen fest.</span><span class="sxs-lookup"><span data-stu-id="63f6d-122">Set an array of render-targets.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="63f6d-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63f6d-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="63f6d-124">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="63f6d-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="63f6d-125">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="63f6d-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="63f6d-126">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="63f6d-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="63f6d-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="63f6d-127">Requirements</span></span>



| <span data-ttu-id="63f6d-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63f6d-128">Requirement</span></span> | <span data-ttu-id="63f6d-129">Wert</span><span class="sxs-lookup"><span data-stu-id="63f6d-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63f6d-130">Header</span><span class="sxs-lookup"><span data-stu-id="63f6d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="63f6d-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="63f6d-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="63f6d-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="63f6d-132">Library</span></span><br/> | <dl> <span data-ttu-id="63f6d-133"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="63f6d-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63f6d-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="63f6d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63f6d-135">**ID3DX11EffectRasterizerVariable**</span><span class="sxs-lookup"><span data-stu-id="63f6d-135">**ID3DX11EffectRasterizerVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="63f6d-136">Effekte 11-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="63f6d-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="63f6d-137">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="63f6d-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





