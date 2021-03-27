---
title: ID3DX11EffectUnorderedAccessViewVariable-Schnittstelle (D3dx11effect. h)
description: Greift auf eine ungeordnete Zugriffs Ansicht zu.
ms.assetid: f78dc8c5-c85a-48cf-b579-f2937aa5ce2a
keywords:
- ID3DX11EffectUnorderedAccessViewVariable-Schnittstelle Direct3D 11
- ID3DX11EffectUnorderedAccessViewVariable Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d48161ad4d9fc1773889fab0e8a0fd9a21ec793e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995805"
---
# <a name="id3dx11effectunorderedaccessviewvariable-interface"></a><span data-ttu-id="6a367-105">ID3DX11EffectUnorderedAccessViewVariable-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6a367-105">ID3DX11EffectUnorderedAccessViewVariable interface</span></span>

<span data-ttu-id="6a367-106">Greift auf eine ungeordnete Zugriffs Ansicht zu.</span><span class="sxs-lookup"><span data-stu-id="6a367-106">Accesses an unordered access view.</span></span>

## <a name="members"></a><span data-ttu-id="6a367-107">Member</span><span class="sxs-lookup"><span data-stu-id="6a367-107">Members</span></span>

<span data-ttu-id="6a367-108">Die **ID3DX11EffectUnorderedAccessViewVariable** -Schnittstelle erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="6a367-108">The **ID3DX11EffectUnorderedAccessViewVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="6a367-109">**ID3DX11EffectUnorderedAccessViewVariable** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6a367-109">**ID3DX11EffectUnorderedAccessViewVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="6a367-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="6a367-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6a367-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="6a367-111">Methods</span></span>

<span data-ttu-id="6a367-112">Die **ID3DX11EffectUnorderedAccessViewVariable** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6a367-112">The **ID3DX11EffectUnorderedAccessViewVariable** interface has these methods.</span></span>



| <span data-ttu-id="6a367-113">Methode</span><span class="sxs-lookup"><span data-stu-id="6a367-113">Method</span></span>                                                                                                      | <span data-ttu-id="6a367-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a367-114">Description</span></span>                                        |
|:------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="6a367-115">**Getunorderedaccessview**</span><span class="sxs-lookup"><span data-stu-id="6a367-115">**GetUnorderedAccessView**</span></span>](id3dx11effectunorderedaccessviewvariable-getunorderedaccessview.md)           | <span data-ttu-id="6a367-116">Erhalten Sie eine ungeordnete Zugriffs Ansicht.</span><span class="sxs-lookup"><span data-stu-id="6a367-116">Get an unordered-access-view.</span></span><br/>           |
| [<span data-ttu-id="6a367-117">**Getunorderedaccessviewarray**</span><span class="sxs-lookup"><span data-stu-id="6a367-117">**GetUnorderedAccessViewArray**</span></span>](id3dx11effectunorderedaccessviewvariable-getunorderedaccessviewarray.md) | <span data-ttu-id="6a367-118">Abrufen eines Arrays von ungeordneten Access-Ansichten.</span><span class="sxs-lookup"><span data-stu-id="6a367-118">Get an array of unordered-access-views.</span></span><br/> |
| [<span data-ttu-id="6a367-119">**"\*"**</span><span class="sxs-lookup"><span data-stu-id="6a367-119">**SetUnorderedAccessView**</span></span>](id3dx11effectunorderedaccessviewvariable-setunorderedaccessview.md)           | <span data-ttu-id="6a367-120">Legen Sie eine ungeordnete Zugriffs Ansicht fest.</span><span class="sxs-lookup"><span data-stu-id="6a367-120">Set an unordered-access-view.</span></span><br/>           |
| [<span data-ttu-id="6a367-121">**"\*"**</span><span class="sxs-lookup"><span data-stu-id="6a367-121">**SetUnorderedAccessViewArray**</span></span>](id3dx11effectunorderedaccessviewvariable-setunorderedaccessviewarray.md) | <span data-ttu-id="6a367-122">Legen Sie ein Array von ungeordneten Zugriffs Ansichten fest.</span><span class="sxs-lookup"><span data-stu-id="6a367-122">Set an array of unordered-access-views.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6a367-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a367-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6a367-124">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="6a367-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6a367-125">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6a367-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6a367-126">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6a367-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6a367-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6a367-127">Requirements</span></span>



| <span data-ttu-id="6a367-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a367-128">Requirement</span></span> | <span data-ttu-id="6a367-129">Wert</span><span class="sxs-lookup"><span data-stu-id="6a367-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a367-130">Header</span><span class="sxs-lookup"><span data-stu-id="6a367-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6a367-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a367-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6a367-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6a367-132">Library</span></span><br/> | <dl> <span data-ttu-id="6a367-133"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="6a367-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a367-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6a367-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a367-135">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="6a367-135">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="6a367-136">Effekte 11-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6a367-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="6a367-137">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6a367-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





