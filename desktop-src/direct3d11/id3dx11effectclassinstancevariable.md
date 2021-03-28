---
title: ID3DX11EffectClassInstanceVariable-Schnittstelle (D3dx11effect. h)
description: Greift auf eine Klasseninstanz zu.
ms.assetid: 64bbae01-1b54-4b3c-9115-80d7b8911ff8
keywords:
- ID3DX11EffectClassInstanceVariable-Schnittstelle Direct3D 11
- ID3DX11EffectClassInstanceVariable Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectClassInstanceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e8b6c7ca76dd595363fa0cd80753fce0b66b2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355986"
---
# <a name="id3dx11effectclassinstancevariable-interface"></a><span data-ttu-id="116e7-105">ID3DX11EffectClassInstanceVariable-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="116e7-105">ID3DX11EffectClassInstanceVariable interface</span></span>

<span data-ttu-id="116e7-106">Greift auf eine Klasseninstanz zu.</span><span class="sxs-lookup"><span data-stu-id="116e7-106">Accesses a class instance.</span></span>

## <a name="members"></a><span data-ttu-id="116e7-107">Member</span><span class="sxs-lookup"><span data-stu-id="116e7-107">Members</span></span>

<span data-ttu-id="116e7-108">Die **ID3DX11EffectClassInstanceVariable** -Schnittstelle erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="116e7-108">The **ID3DX11EffectClassInstanceVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="116e7-109">**ID3DX11EffectClassInstanceVariable** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="116e7-109">**ID3DX11EffectClassInstanceVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="116e7-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="116e7-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="116e7-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="116e7-111">Methods</span></span>

<span data-ttu-id="116e7-112">Die **ID3DX11EffectClassInstanceVariable** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="116e7-112">The **ID3DX11EffectClassInstanceVariable** interface has these methods.</span></span>



| <span data-ttu-id="116e7-113">Methode</span><span class="sxs-lookup"><span data-stu-id="116e7-113">Method</span></span>                                                                          | <span data-ttu-id="116e7-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="116e7-114">Description</span></span>                       |
|:--------------------------------------------------------------------------------|:----------------------------------|
| [<span data-ttu-id="116e7-115">**Getclassinstance**</span><span class="sxs-lookup"><span data-stu-id="116e7-115">**GetClassInstance**</span></span>](id3dx11effectclassinstancevariable-getclassinstance.md) | <span data-ttu-id="116e7-116">Ruft eine-Klasseninstanz ab.</span><span class="sxs-lookup"><span data-stu-id="116e7-116">Gets a class instance.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="116e7-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="116e7-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="116e7-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="116e7-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="116e7-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="116e7-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="116e7-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="116e7-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="116e7-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="116e7-121">Requirements</span></span>



| <span data-ttu-id="116e7-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="116e7-122">Requirement</span></span> | <span data-ttu-id="116e7-123">Wert</span><span class="sxs-lookup"><span data-stu-id="116e7-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="116e7-124">Header</span><span class="sxs-lookup"><span data-stu-id="116e7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="116e7-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="116e7-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="116e7-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="116e7-126">Library</span></span><br/> | <dl> <span data-ttu-id="116e7-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="116e7-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="116e7-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="116e7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="116e7-129">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="116e7-129">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="116e7-130">Effekte 11-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="116e7-130">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="116e7-131">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="116e7-131">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





