---
title: ID3DX11EffectGroup-Schnittstelle (D3dx11effect. h)
description: Die ID3DX11EffectGroup-Schnittstelle greift auf eine Effekt Gruppe zu. Die Lebensdauer eines ID3DX11EffectGroup-Objekts entspricht der Lebensdauer seines übergeordneten ID3DX11Effect-Objekts.
ms.assetid: f5a35c47-0bac-4559-bd6c-5e8bc7699e10
keywords:
- ID3DX11EffectGroup-Schnittstelle Direct3D 11
- ID3DX11EffectGroup Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5970506b850d164a4018cd371e19bfab6cd3624
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982281"
---
# <a name="id3dx11effectgroup-interface"></a><span data-ttu-id="a0473-105">ID3DX11EffectGroup-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a0473-105">ID3DX11EffectGroup interface</span></span>

<span data-ttu-id="a0473-106">Die **ID3DX11EffectGroup** -Schnittstelle greift auf eine Effekt Gruppe zu.</span><span class="sxs-lookup"><span data-stu-id="a0473-106">The **ID3DX11EffectGroup** interface accesses an Effect group.</span></span>

<span data-ttu-id="a0473-107">Die Lebensdauer eines **ID3DX11EffectGroup** -Objekts entspricht der Lebensdauer seines übergeordneten [**ID3DX11Effect**](id3dx11effect.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="a0473-107">The lifetime of an **ID3DX11EffectGroup** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="a0473-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="a0473-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a0473-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="a0473-109">Methods</span></span>

<span data-ttu-id="a0473-110">Die **ID3DX11EffectGroup** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a0473-110">The **ID3DX11EffectGroup** interface has these methods.</span></span>



| <span data-ttu-id="a0473-111">Methode</span><span class="sxs-lookup"><span data-stu-id="a0473-111">Method</span></span>                                                                  | <span data-ttu-id="a0473-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0473-112">Description</span></span>                                                   |
|:------------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="a0473-113">**Getannotationbyindex**</span><span class="sxs-lookup"><span data-stu-id="a0473-113">**GetAnnotationByIndex**</span></span>](id3dx11effectgroup-getannotationbyindex.md) | <span data-ttu-id="a0473-114">Eine Anmerkung nach Index erhalten.</span><span class="sxs-lookup"><span data-stu-id="a0473-114">Get an annotation by index.</span></span><br/>                        |
| [<span data-ttu-id="a0473-115">**Getannotationbyname**</span><span class="sxs-lookup"><span data-stu-id="a0473-115">**GetAnnotationByName**</span></span>](id3dx11effectgroup-getannotationbyname.md)   | <span data-ttu-id="a0473-116">Eine Anmerkung anhand des Namens erhalten.</span><span class="sxs-lookup"><span data-stu-id="a0473-116">Get an annotation by name.</span></span><br/>                         |
| [<span data-ttu-id="a0473-117">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="a0473-117">**GetDesc**</span></span>](id3dx11effectgroup-getdesc.md)                           | <span data-ttu-id="a0473-118">Ruft eine Gruppenbeschreibung ab.</span><span class="sxs-lookup"><span data-stu-id="a0473-118">Gets a group description.</span></span><br/>                          |
| [<span data-ttu-id="a0473-119">**Gettechniquebyindex**</span><span class="sxs-lookup"><span data-stu-id="a0473-119">**GetTechniqueByIndex**</span></span>](id3dx11effectgroup-gettechniquebyindex.md)   | <span data-ttu-id="a0473-120">Holen Sie sich eine Technik nach Index.</span><span class="sxs-lookup"><span data-stu-id="a0473-120">Get a technique by index.</span></span><br/>                          |
| [<span data-ttu-id="a0473-121">**Gettechniquebyname**</span><span class="sxs-lookup"><span data-stu-id="a0473-121">**GetTechniqueByName**</span></span>](id3dx11effectgroup-gettechniquebyname.md)     | <span data-ttu-id="a0473-122">Holen Sie sich eine Technik anhand des Namens.</span><span class="sxs-lookup"><span data-stu-id="a0473-122">Get a technique by name.</span></span><br/>                           |
| [<span data-ttu-id="a0473-123">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="a0473-123">**IsValid**</span></span>](id3dx11effectgroup-isvalid.md)                           | <span data-ttu-id="a0473-124">Testen Sie einen Effekt, um festzustellen, ob er eine gültige Syntax enthält.</span><span class="sxs-lookup"><span data-stu-id="a0473-124">Test an effect to see if it contains valid syntax.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a0473-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0473-125">Remarks</span></span>

<span data-ttu-id="a0473-126">Um eine **ID3DX11EffectGroup** -Schnittstelle zu erhalten, müssen Sie eine Methode wie [**ID3DX11Effect:: getgroupbyname**](id3dx11effect-getgroupbyname.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a0473-126">To get an **ID3DX11EffectGroup** interface, call a method like [**ID3DX11Effect::GetGroupByName**](id3dx11effect-getgroupbyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="a0473-127">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="a0473-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a0473-128">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a0473-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a0473-129">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a0473-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a0473-130">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a0473-130">Requirements</span></span>



| <span data-ttu-id="a0473-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0473-131">Requirement</span></span> | <span data-ttu-id="a0473-132">Wert</span><span class="sxs-lookup"><span data-stu-id="a0473-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0473-133">Header</span><span class="sxs-lookup"><span data-stu-id="a0473-133">Header</span></span><br/>  | <dl> <span data-ttu-id="a0473-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0473-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a0473-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a0473-135">Library</span></span><br/> | <dl> <span data-ttu-id="a0473-136"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="a0473-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0473-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a0473-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0473-138">Effekte 11-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a0473-138">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a0473-139">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a0473-139">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





