---
title: ID3DX11EffectTechnique-Schnittstelle (D3dx11effect. h)
description: Eine ID3DX11EffectTechnique-Schnittstelle ist eine Auflistung von Durchläufen. Die Lebensdauer eines ID3DX11EffectTechnique-Objekts entspricht der Lebensdauer seines übergeordneten ID3DX11Effect-Objekts.
ms.assetid: 63d52cac-287d-4432-bf2b-7b4e67e525e6
keywords:
- ID3DX11EffectTechnique-Schnittstelle Direct3D 11
- ID3DX11EffectTechnique Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e582d8f94b2dbcbb2052a8cf3a59d8ba514367cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982540"
---
# <a name="id3dx11effecttechnique-interface"></a><span data-ttu-id="ba338-105">ID3DX11EffectTechnique-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ba338-105">ID3DX11EffectTechnique interface</span></span>

<span data-ttu-id="ba338-106">Eine **ID3DX11EffectTechnique** -Schnittstelle ist eine Auflistung von Durchläufen.</span><span class="sxs-lookup"><span data-stu-id="ba338-106">An **ID3DX11EffectTechnique** interface is a collection of passes.</span></span>

<span data-ttu-id="ba338-107">Die Lebensdauer eines **ID3DX11EffectTechnique** -Objekts entspricht der Lebensdauer seines übergeordneten [**ID3DX11Effect**](id3dx11effect.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="ba338-107">The lifetime of an **ID3DX11EffectTechnique** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="ba338-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="ba338-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ba338-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="ba338-109">Methods</span></span>

<span data-ttu-id="ba338-110">Die **ID3DX11EffectTechnique** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ba338-110">The **ID3DX11EffectTechnique** interface has these methods.</span></span>



| <span data-ttu-id="ba338-111">Methode</span><span class="sxs-lookup"><span data-stu-id="ba338-111">Method</span></span>                                                                        | <span data-ttu-id="ba338-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba338-112">Description</span></span>                                                           |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="ba338-113">**Computestateblockmask**</span><span class="sxs-lookup"><span data-stu-id="ba338-113">**ComputeStateBlockMask**</span></span>](id3dx11effecttechnique-computestateblockmask.md) | <span data-ttu-id="ba338-114">Berechnen Sie eine Zustands Block Maske, um Zustandsänderungen zuzulassen/zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="ba338-114">Compute a state-block mask to allow/prevent state changes.</span></span><br/> |
| [<span data-ttu-id="ba338-115">**Getannotationbyindex**</span><span class="sxs-lookup"><span data-stu-id="ba338-115">**GetAnnotationByIndex**</span></span>](id3dx11effecttechnique-getannotationbyindex.md)   | <span data-ttu-id="ba338-116">Eine Anmerkung nach Index erhalten.</span><span class="sxs-lookup"><span data-stu-id="ba338-116">Get an annotation by index.</span></span><br/>                                |
| [<span data-ttu-id="ba338-117">**Getannotationbyname**</span><span class="sxs-lookup"><span data-stu-id="ba338-117">**GetAnnotationByName**</span></span>](id3dx11effecttechnique-getannotationbyname.md)     | <span data-ttu-id="ba338-118">Eine Anmerkung anhand des Namens erhalten.</span><span class="sxs-lookup"><span data-stu-id="ba338-118">Get an annotation by name.</span></span><br/>                                 |
| [<span data-ttu-id="ba338-119">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="ba338-119">**GetDesc**</span></span>](id3dx11effecttechnique-getdesc.md)                             | <span data-ttu-id="ba338-120">Hier finden Sie eine Technik Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="ba338-120">Get a technique description.</span></span><br/>                               |
| [<span data-ttu-id="ba338-121">**Getpassbyindex**</span><span class="sxs-lookup"><span data-stu-id="ba338-121">**GetPassByIndex**</span></span>](id3dx11effecttechnique-getpassbyindex.md)               | <span data-ttu-id="ba338-122">Einen Pass-by-Index erhalten.</span><span class="sxs-lookup"><span data-stu-id="ba338-122">Get a pass by index.</span></span><br/>                                       |
| [<span data-ttu-id="ba338-123">**Getpassbyname**</span><span class="sxs-lookup"><span data-stu-id="ba338-123">**GetPassByName**</span></span>](id3dx11effecttechnique-getpassbyname.md)                 | <span data-ttu-id="ba338-124">Einen Pass-Through-Namen erhalten.</span><span class="sxs-lookup"><span data-stu-id="ba338-124">Get a pass by name.</span></span><br/>                                        |
| [<span data-ttu-id="ba338-125">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="ba338-125">**IsValid**</span></span>](id3dx11effecttechnique-isvalid.md)                             | <span data-ttu-id="ba338-126">Testen Sie eine Technik, um festzustellen, ob Sie eine gültige Syntax enthält.</span><span class="sxs-lookup"><span data-stu-id="ba338-126">Test a technique to see if it contains valid syntax.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="ba338-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba338-127">Remarks</span></span>

<span data-ttu-id="ba338-128">Ein Effekt enthält mindestens eine Technik. jede Technik enthält einen oder mehrere Durchgänge. Jeder Durchlauf enthält Zustands Zuweisungen.</span><span class="sxs-lookup"><span data-stu-id="ba338-128">An effect contains one or more techniques; each technique contains one or more passes; each pass contains state assignments.</span></span>

<span data-ttu-id="ba338-129">Um eine Wirkungs Technik-Schnittstelle zu erhalten, müssen Sie eine Methode wie [**ID3DX11Effect:: gettechniquebyname**](id3dx11effect-gettechniquebyname.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ba338-129">To get an effect-technique interface, call a method such as [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="ba338-130">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="ba338-130">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ba338-131">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ba338-131">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ba338-132">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ba338-132">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ba338-133">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ba338-133">Requirements</span></span>



| <span data-ttu-id="ba338-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba338-134">Requirement</span></span> | <span data-ttu-id="ba338-135">Wert</span><span class="sxs-lookup"><span data-stu-id="ba338-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba338-136">Header</span><span class="sxs-lookup"><span data-stu-id="ba338-136">Header</span></span><br/>  | <dl> <span data-ttu-id="ba338-137"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba338-137"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ba338-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ba338-138">Library</span></span><br/> | <dl> <span data-ttu-id="ba338-139"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="ba338-139"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba338-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ba338-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba338-141">Effekte 11-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ba338-141">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="ba338-142">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ba338-142">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





