---
title: ID3DX11EffectType-Schnittstelle (D3dx11effect. h)
description: Die ID3DX11EffectType-Schnittstelle greift auf die Effekt Variablen nach Typ zu. Die Lebensdauer eines ID3DX11EffectType-Objekts entspricht der Lebensdauer seines übergeordneten ID3DX11Effect-Objekts.
ms.assetid: 700076ee-a5fe-4af2-a5f4-053c05d8ddf0
keywords:
- ID3DX11EffectType-Schnittstelle Direct3D 11
- ID3DX11EffectType Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectType
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e3c210ca60abc9e55b8864a2b121cf92be369a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761982"
---
# <a name="id3dx11effecttype-interface"></a><span data-ttu-id="56230-105">ID3DX11EffectType-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="56230-105">ID3DX11EffectType interface</span></span>

<span data-ttu-id="56230-106">Die **ID3DX11EffectType** -Schnittstelle greift auf die Effekt Variablen nach Typ zu.</span><span class="sxs-lookup"><span data-stu-id="56230-106">The **ID3DX11EffectType** interface accesses effect variables by type.</span></span>

<span data-ttu-id="56230-107">Die Lebensdauer eines **ID3DX11EffectType** -Objekts entspricht der Lebensdauer seines übergeordneten [**ID3DX11Effect**](id3dx11effect.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="56230-107">The lifetime of an **ID3DX11EffectType** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="56230-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="56230-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="56230-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="56230-109">Methods</span></span>

<span data-ttu-id="56230-110">Die **ID3DX11EffectType** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="56230-110">The **ID3DX11EffectType** interface has these methods.</span></span>



| <span data-ttu-id="56230-111">Methode</span><span class="sxs-lookup"><span data-stu-id="56230-111">Method</span></span>                                                                       | <span data-ttu-id="56230-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56230-112">Description</span></span>                                       |
|:-----------------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="56230-113">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="56230-113">**GetDesc**</span></span>](id3dx11effecttype-getdesc.md)                                 | <span data-ttu-id="56230-114">Geben Sie eine Beschreibung des Effekt Typs an.</span><span class="sxs-lookup"><span data-stu-id="56230-114">Get an effect-type description.</span></span><br/>        |
| [<span data-ttu-id="56230-115">**Getmembership Name**</span><span class="sxs-lookup"><span data-stu-id="56230-115">**GetMemberName**</span></span>](id3dx11effecttype-getmembername.md)                     | <span data-ttu-id="56230-116">Den Namen eines Members zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="56230-116">Get the name of a member.</span></span><br/>              |
| [<span data-ttu-id="56230-117">**Getmembership Semantic**</span><span class="sxs-lookup"><span data-stu-id="56230-117">**GetMemberSemantic**</span></span>](id3dx11effecttype-getmembersemantic.md)             | <span data-ttu-id="56230-118">Die an einen Member angefügte Semantik wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="56230-118">Get the semantic attached to a member.</span></span><br/> |
| [<span data-ttu-id="56230-119">**GetMemberTypeByIndex**</span><span class="sxs-lookup"><span data-stu-id="56230-119">**GetMemberTypeByIndex**</span></span>](id3dx11effecttype-getmembertypebyindex.md)       | <span data-ttu-id="56230-120">Einen Elementtyp nach Index erhalten.</span><span class="sxs-lookup"><span data-stu-id="56230-120">Get a member type by index.</span></span><br/>            |
| [<span data-ttu-id="56230-121">**GetMemberTypeByName**</span><span class="sxs-lookup"><span data-stu-id="56230-121">**GetMemberTypeByName**</span></span>](id3dx11effecttype-getmembertypebyname.md)         | <span data-ttu-id="56230-122">Einen Elementtyp nach Name erhalten.</span><span class="sxs-lookup"><span data-stu-id="56230-122">Get an member type by name.</span></span><br/>            |
| [<span data-ttu-id="56230-123">**Getmembership typebysemantic**</span><span class="sxs-lookup"><span data-stu-id="56230-123">**GetMemberTypeBySemantic**</span></span>](id3dx11effecttype-getmembertypebysemantic.md) | <span data-ttu-id="56230-124">Einen Elementtyp nach Semantik erhalten.</span><span class="sxs-lookup"><span data-stu-id="56230-124">Get a member type by semantic.</span></span><br/>         |
| [<span data-ttu-id="56230-125">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="56230-125">**IsValid**</span></span>](id3dx11effecttype-isvalid.md)                                 | <span data-ttu-id="56230-126">Testet, ob der Effekts-Typ gültig ist.</span><span class="sxs-lookup"><span data-stu-id="56230-126">Tests that the effect type is valid.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="56230-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56230-127">Remarks</span></span>

<span data-ttu-id="56230-128">Zum Abrufen von Informationen zu einem Effekts-Typ aus einer Effekt Variablen, aufrufen Sie [**ID3DX11EffectVariable:: GetType**](id3dx11effectvariable-gettype.md).</span><span class="sxs-lookup"><span data-stu-id="56230-128">To get information about an effect type from an effect variable, call [**ID3DX11EffectVariable::GetType**](id3dx11effectvariable-gettype.md).</span></span>

> [!Note]  
> <span data-ttu-id="56230-129">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="56230-129">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="56230-130">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="56230-130">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="56230-131">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="56230-131">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="56230-132">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="56230-132">Requirements</span></span>



| <span data-ttu-id="56230-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56230-133">Requirement</span></span> | <span data-ttu-id="56230-134">Wert</span><span class="sxs-lookup"><span data-stu-id="56230-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56230-135">Header</span><span class="sxs-lookup"><span data-stu-id="56230-135">Header</span></span><br/>  | <dl> <span data-ttu-id="56230-136"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="56230-136"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="56230-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="56230-137">Library</span></span><br/> | <dl> <span data-ttu-id="56230-138"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="56230-138"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56230-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="56230-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56230-140">Effekte 11-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="56230-140">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="56230-141">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="56230-141">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





