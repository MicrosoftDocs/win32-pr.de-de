---
title: ID3DX11EffectMatrixVariable-Schnittstelle (D3dx11effect. h)
description: Eine Matrix Variable-Schnittstelle greift auf eine Matrix zu.
ms.assetid: 44f30d1a-3ec1-49d7-92c0-475cf2fa4d2a
keywords:
- ID3DX11EffectMatrixVariable-Schnittstelle Direct3D 11
- ID3DX11EffectMatrixVariable Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5c4c89a231d429fc0a1f8fecbcbb4d06db35cb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982366"
---
# <a name="id3dx11effectmatrixvariable-interface"></a><span data-ttu-id="0254f-105">ID3DX11EffectMatrixVariable-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0254f-105">ID3DX11EffectMatrixVariable interface</span></span>

<span data-ttu-id="0254f-106">Eine Matrix Variable-Schnittstelle greift auf eine Matrix zu.</span><span class="sxs-lookup"><span data-stu-id="0254f-106">A matrix-variable interface accesses a matrix.</span></span>

## <a name="members"></a><span data-ttu-id="0254f-107">Member</span><span class="sxs-lookup"><span data-stu-id="0254f-107">Members</span></span>

<span data-ttu-id="0254f-108">Die **ID3DX11EffectMatrixVariable** -Schnittstelle erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="0254f-108">The **ID3DX11EffectMatrixVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="0254f-109">**ID3DX11EffectMatrixVariable** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0254f-109">**ID3DX11EffectMatrixVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="0254f-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="0254f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0254f-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="0254f-111">Methods</span></span>

<span data-ttu-id="0254f-112">Die **ID3DX11EffectMatrixVariable** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0254f-112">The **ID3DX11EffectMatrixVariable** interface has these methods.</span></span>



| <span data-ttu-id="0254f-113">Methode</span><span class="sxs-lookup"><span data-stu-id="0254f-113">Method</span></span>                                                                                 | <span data-ttu-id="0254f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0254f-114">Description</span></span>                                                       |
|:---------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="0254f-115">**GetMatrix**</span><span class="sxs-lookup"><span data-stu-id="0254f-115">**GetMatrix**</span></span>](id3dx11effectmatrixvariable-getmatrix.md)                             | <span data-ttu-id="0254f-116">Eine Matrix erhalten.</span><span class="sxs-lookup"><span data-stu-id="0254f-116">Get a matrix.</span></span><br/>                                          |
| [<span data-ttu-id="0254f-117">**Getmatrixarray**</span><span class="sxs-lookup"><span data-stu-id="0254f-117">**GetMatrixArray**</span></span>](id3dx11effectmatrixvariable-getmatrixarray.md)                   | <span data-ttu-id="0254f-118">Ein Array von Matrizen erhalten.</span><span class="sxs-lookup"><span data-stu-id="0254f-118">Get an array of matrices.</span></span><br/>                              |
| [<span data-ttu-id="0254f-119">**Getmatrixtransform**</span><span class="sxs-lookup"><span data-stu-id="0254f-119">**GetMatrixTranspose**</span></span>](id3dx11effectmatrixvariable-getmatrixtranspose.md)           | <span data-ttu-id="0254f-120">Eine Gleit Komma Matrix austauschen und erhalten.</span><span class="sxs-lookup"><span data-stu-id="0254f-120">Transpose and get a floating-point matrix.</span></span><br/>             |
| [<span data-ttu-id="0254f-121">**Getmatrixtransposearray**</span><span class="sxs-lookup"><span data-stu-id="0254f-121">**GetMatrixTransposeArray**</span></span>](id3dx11effectmatrixvariable-getmatrixtransposearray.md) | <span data-ttu-id="0254f-122">Austauschen und erhalten eines Arrays von Gleit Komma Matrizen.</span><span class="sxs-lookup"><span data-stu-id="0254f-122">Transpose and get an array of floating-point matrices.</span></span><br/> |
| [<span data-ttu-id="0254f-123">**SetMatrix**</span><span class="sxs-lookup"><span data-stu-id="0254f-123">**SetMatrix**</span></span>](id3dx11effectmatrixvariable-setmatrix.md)                             | <span data-ttu-id="0254f-124">Legen Sie eine Gleit Komma Matrix fest.</span><span class="sxs-lookup"><span data-stu-id="0254f-124">Set a floating-point matrix.</span></span><br/>                           |
| [<span data-ttu-id="0254f-125">**Setmatrixarray**</span><span class="sxs-lookup"><span data-stu-id="0254f-125">**SetMatrixArray**</span></span>](id3dx11effectmatrixvariable-setmatrixarray.md)                   | <span data-ttu-id="0254f-126">Legen Sie ein Array von Gleit Komma Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="0254f-126">Set an array of floating-point matrices.</span></span><br/>               |
| [<span data-ttu-id="0254f-127">**Setmatrixtransform**</span><span class="sxs-lookup"><span data-stu-id="0254f-127">**SetMatrixTranspose**</span></span>](id3dx11effectmatrixvariable-setmatrixtranspose.md)           | <span data-ttu-id="0254f-128">Sie sollten eine Gleit Komma Matrix austauschen und festlegen.</span><span class="sxs-lookup"><span data-stu-id="0254f-128">Transpose and set a floating-point matrix.</span></span><br/>             |
| [<span data-ttu-id="0254f-129">**Setmatrixtransposearray**</span><span class="sxs-lookup"><span data-stu-id="0254f-129">**SetMatrixTransposeArray**</span></span>](id3dx11effectmatrixvariable-setmatrixtransposearray.md) | <span data-ttu-id="0254f-130">Ein Array von Gleit Komma Matrizen wird aus-und festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0254f-130">Transpose and set an array of floating-point matrices.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0254f-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0254f-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0254f-132">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="0254f-132">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0254f-133">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0254f-133">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0254f-134">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0254f-134">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0254f-135">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0254f-135">Requirements</span></span>



| <span data-ttu-id="0254f-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0254f-136">Requirement</span></span> | <span data-ttu-id="0254f-137">Wert</span><span class="sxs-lookup"><span data-stu-id="0254f-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0254f-138">Header</span><span class="sxs-lookup"><span data-stu-id="0254f-138">Header</span></span><br/>  | <dl> <span data-ttu-id="0254f-139"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0254f-139"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0254f-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0254f-140">Library</span></span><br/> | <dl> <span data-ttu-id="0254f-141"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="0254f-141"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0254f-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0254f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0254f-143">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="0254f-143">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="0254f-144">Effekte 11-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0254f-144">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="0254f-145">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0254f-145">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





