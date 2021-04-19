---
description: Ruft die Gitter Optionen ab, die für dieses Mesh zum Zeitpunkt der Erstellung aktiviert sind.
ms.assetid: 4be990d7-77ab-4273-b852-e6283a89ac6c
title: 'ID3DXBaseMesh:: GetOptions-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetOptions
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a751230b4ccfc537f651846ed455b62d7c7f8262
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373535"
---
# <a name="id3dxbasemeshgetoptions-method"></a><span data-ttu-id="715e2-103">ID3DXBaseMesh:: GetOptions-Methode</span><span class="sxs-lookup"><span data-stu-id="715e2-103">ID3DXBaseMesh::GetOptions method</span></span>

<span data-ttu-id="715e2-104">Ruft die Gitter Optionen ab, die für dieses Mesh zum Zeitpunkt der Erstellung aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="715e2-104">Retrieves the mesh options enabled for this mesh at creation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="715e2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="715e2-105">Syntax</span></span>


```C++
DWORD GetOptions();
```



## <a name="parameters"></a><span data-ttu-id="715e2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="715e2-106">Parameters</span></span>

<span data-ttu-id="715e2-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="715e2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="715e2-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="715e2-108">Return value</span></span>

<span data-ttu-id="715e2-109">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="715e2-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="715e2-110">Gibt eine Kombination aus einem oder mehreren der folgenden Flags zurück, die die Optionen angibt, die für dieses Mesh zum Zeitpunkt der Erstellung aktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="715e2-110">Returns a combination of one or more of the following flags, indicating the options enabled for this mesh at creation time.</span></span>



| <span data-ttu-id="715e2-111">Wert</span><span class="sxs-lookup"><span data-stu-id="715e2-111">Value</span></span>                   | <span data-ttu-id="715e2-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="715e2-112">Description</span></span>                                                                                                                                                                                      |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="715e2-113">D3DXMESH \_ 32-Bit</span><span class="sxs-lookup"><span data-stu-id="715e2-113">D3DXMESH\_32BIT</span></span>         | <span data-ttu-id="715e2-114">Verwenden Sie 32-Bit-Indizes.</span><span class="sxs-lookup"><span data-stu-id="715e2-114">Use 32-bit indices.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="715e2-115">D3DXMESH \_ DoNotClip</span><span class="sxs-lookup"><span data-stu-id="715e2-115">D3DXMESH\_DONOTCLIP</span></span>     | <span data-ttu-id="715e2-116">Verwenden Sie das D3DUSAGE \_ DoNotClip-nutzungsflag für Scheitelpunkt-und Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="715e2-116">Use the D3DUSAGE\_DONOTCLIP usage flag for vertex and index buffers.</span></span>                                                                                                                             |
| <span data-ttu-id="715e2-117">D3DXMESH \_ dynamisch</span><span class="sxs-lookup"><span data-stu-id="715e2-117">D3DXMESH\_DYNAMIC</span></span>       | <span data-ttu-id="715e2-118">Äquivalent zum Angeben von D3DXMESH \_ vb \_ Dynamic und D3DXMESH \_ IB \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="715e2-118">Equivalent to specifying both D3DXMESH\_VB\_DYNAMIC and D3DXMESH\_IB\_DYNAMIC.</span></span>                                                                                                                   |
| <span data-ttu-id="715e2-119">D3DXMESH \_ rtpatches</span><span class="sxs-lookup"><span data-stu-id="715e2-119">D3DXMESH\_RTPATCHES</span></span>     | <span data-ttu-id="715e2-120">Verwenden Sie das D3DUSAGE \_ rtpatches Usage-Flag für Scheitelpunkt-und Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="715e2-120">Use the D3DUSAGE\_RTPATCHES usage flag for vertex and index buffers.</span></span>                                                                                                                             |
| <span data-ttu-id="715e2-121">D3DXMESH \_ npatches</span><span class="sxs-lookup"><span data-stu-id="715e2-121">D3DXMESH\_NPATCHES</span></span>      | <span data-ttu-id="715e2-122">Die Angabe dieses Flags bewirkt, dass der Scheitelpunkt und der Index Puffer des Mesh mit dem D3DUSAGE \_ npatches-Flag erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="715e2-122">Specifying this flag causes the vertex and index buffer of the mesh to be created with D3DUSAGE\_NPATCHES flag.</span></span> <span data-ttu-id="715e2-123">Dies ist erforderlich, wenn das Mesh-Objekt mit der N-Patch-Erweiterung gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="715e2-123">This is required if the mesh object is to be rendered using N-Patch enhancement.</span></span> |
| <span data-ttu-id="715e2-124">D3DXMESH \_ verwaltet</span><span class="sxs-lookup"><span data-stu-id="715e2-124">D3DXMESH\_MANAGED</span></span>       | <span data-ttu-id="715e2-125">Entspricht der Angabe von D3DXMESH \_ vb \_ Managed und D3DXMESH \_ IB \_ Managed.</span><span class="sxs-lookup"><span data-stu-id="715e2-125">Equivalent to specifying both D3DXMESH\_VB\_MANAGED and D3DXMESH\_IB\_MANAGED.</span></span>                                                                                                                   |
| <span data-ttu-id="715e2-126">D3DXMESH \_ Punkte</span><span class="sxs-lookup"><span data-stu-id="715e2-126">D3DXMESH\_POINTS</span></span>        | <span data-ttu-id="715e2-127">Verwenden Sie das \_ Usage-Flag D3DUSAGE Points für Scheitelpunkt-und Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="715e2-127">Use the D3DUSAGE\_POINTS usage flag for vertex and index buffers.</span></span>                                                                                                                                |
| <span data-ttu-id="715e2-128">D3DXMESH \_ IB \_ dynamisch</span><span class="sxs-lookup"><span data-stu-id="715e2-128">D3DXMESH\_IB\_DYNAMIC</span></span>   | <span data-ttu-id="715e2-129">Verwenden Sie das D3DUSAGE \_ Dynamic Usage-Flag für Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="715e2-129">Use the D3DUSAGE\_DYNAMIC usage flag for index buffers.</span></span>                                                                                                                                          |
| <span data-ttu-id="715e2-130">D3DXMESH \_ IB \_ verwaltet</span><span class="sxs-lookup"><span data-stu-id="715e2-130">D3DXMESH\_IB\_MANAGED</span></span>   | <span data-ttu-id="715e2-131">Verwenden Sie die \_ verwaltete D3DPOOL-Speicher Klasse für Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="715e2-131">Use the D3DPOOL\_MANAGED memory class for index buffers.</span></span>                                                                                                                                         |
| <span data-ttu-id="715e2-132">D3DXMESH \_ IB-System Arbeitsspeicher \_</span><span class="sxs-lookup"><span data-stu-id="715e2-132">D3DXMESH\_IB\_SYSTEMMEM</span></span> | <span data-ttu-id="715e2-133">Verwenden Sie die D3DPOOL \_ SystemMem-Speicher Klasse für Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="715e2-133">Use the D3DPOOL\_SYSTEMMEM memory class for index buffers.</span></span>                                                                                                                                       |
| <span data-ttu-id="715e2-134">D3DXMESH \_ IB \_ schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="715e2-134">D3DXMESH\_IB\_WRITEONLY</span></span> | <span data-ttu-id="715e2-135">Verwenden Sie das D3DUSAGE \_ Write-use-Flag für Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="715e2-135">Use the D3DUSAGE\_WRITEONLY usage flag for index buffers.</span></span>                                                                                                                                        |
| <span data-ttu-id="715e2-136">D3DXMESH \_ SystemMem</span><span class="sxs-lookup"><span data-stu-id="715e2-136">D3DXMESH\_SYSTEMMEM</span></span>     | <span data-ttu-id="715e2-137">Entspricht der Angabe von D3DXMESH \_ vb \_ SystemMem und D3DXMESH \_ IB \_ SystemMem.</span><span class="sxs-lookup"><span data-stu-id="715e2-137">Equivalent to specifying both D3DXMESH\_VB\_SYSTEMMEM and D3DXMESH\_IB\_SYSTEMMEM.</span></span>                                                                                                               |
| <span data-ttu-id="715e2-138">D3DXMESH \_ vb \_ dynamisch</span><span class="sxs-lookup"><span data-stu-id="715e2-138">D3DXMESH\_VB\_DYNAMIC</span></span>   | <span data-ttu-id="715e2-139">Verwenden Sie das D3DUSAGE \_ Dynamic Usage-Flag für Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="715e2-139">Use the D3DUSAGE\_DYNAMIC usage flag for vertex buffers.</span></span>                                                                                                                                         |
| <span data-ttu-id="715e2-140">D3DXMESH \_ vb \_ verwaltet</span><span class="sxs-lookup"><span data-stu-id="715e2-140">D3DXMESH\_VB\_MANAGED</span></span>   | <span data-ttu-id="715e2-141">Verwenden Sie die \_ verwaltete D3DPOOL-Speicher Klasse für Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="715e2-141">Use the D3DPOOL\_MANAGED memory class for vertex buffers.</span></span>                                                                                                                                        |
| <span data-ttu-id="715e2-142">D3DXMESH \_ vb \_ SystemMem</span><span class="sxs-lookup"><span data-stu-id="715e2-142">D3DXMESH\_VB\_SYSTEMMEM</span></span> | <span data-ttu-id="715e2-143">Verwenden Sie die D3DPOOL \_ SystemMem-Speicher Klasse für Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="715e2-143">Use the D3DPOOL\_SYSTEMMEM memory class for vertex buffers.</span></span>                                                                                                                                      |
| <span data-ttu-id="715e2-144">D3DXMESH \_ vb \_ schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="715e2-144">D3DXMESH\_VB\_WRITEONLY</span></span> | <span data-ttu-id="715e2-145">Verwenden Sie das D3DUSAGE \_ Write-use-Flag für Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="715e2-145">Use the D3DUSAGE\_WRITEONLY usage flag for vertex buffers.</span></span>                                                                                                                                       |
| <span data-ttu-id="715e2-146">D3DXMESH \_ schreiben</span><span class="sxs-lookup"><span data-stu-id="715e2-146">D3DXMESH\_WRITEONLY</span></span>     | <span data-ttu-id="715e2-147">Entspricht der Angabe von D3DXMESH \_ vb \_ Write-only und D3DXMESH \_ IB \_ Write.</span><span class="sxs-lookup"><span data-stu-id="715e2-147">Equivalent to specifying both D3DXMESH\_VB\_WRITEONLY and D3DXMESH\_IB\_WRITEONLY.</span></span>                                                                                                               |



 

## <a name="requirements"></a><span data-ttu-id="715e2-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="715e2-148">Requirements</span></span>



| <span data-ttu-id="715e2-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="715e2-149">Requirement</span></span> | <span data-ttu-id="715e2-150">Wert</span><span class="sxs-lookup"><span data-stu-id="715e2-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="715e2-151">Header</span><span class="sxs-lookup"><span data-stu-id="715e2-151">Header</span></span><br/>  | <dl> <span data-ttu-id="715e2-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="715e2-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="715e2-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="715e2-153">Library</span></span><br/> | <dl> <span data-ttu-id="715e2-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="715e2-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="715e2-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="715e2-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="715e2-156">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="715e2-156">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
