---
description: Optimiert das patchemesh für effizientes Mosaik.
ms.assetid: 0049e649-5fe5-45b4-9b09-14b7f99b4988
title: 'ID3DXPatchMesh:: optimiert-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fa66aadd0ef1f9f9f65747694fc311f80172449
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961766"
---
# <a name="id3dxpatchmeshoptimize-method"></a><span data-ttu-id="ff60a-103">ID3DXPatchMesh:: optimiert-Methode</span><span class="sxs-lookup"><span data-stu-id="ff60a-103">ID3DXPatchMesh::Optimize method</span></span>

<span data-ttu-id="ff60a-104">Optimiert das patchemesh für effizientes Mosaik.</span><span class="sxs-lookup"><span data-stu-id="ff60a-104">Optimizes the patch mesh for efficient tessellation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff60a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff60a-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in] DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="ff60a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff60a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff60a-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="ff60a-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff60a-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff60a-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff60a-109">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff60a-109">Currently unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff60a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff60a-110">Return value</span></span>

<span data-ttu-id="ff60a-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ff60a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ff60a-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ff60a-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ff60a-113">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ cannotattrsort.</span><span class="sxs-lookup"><span data-stu-id="ff60a-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_CANNOTATTRSORT.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff60a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff60a-114">Remarks</span></span>

<span data-ttu-id="ff60a-115">Nachdem eine Anwendung Informationen zu einem Mesh generiert hat, können die Mesh-Daten optimiert (neu angeordnet) werden, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="ff60a-115">After an application generates adjacency information for a mesh, the mesh data can be optimized (reordered) for better drawing performance.</span></span> <span data-ttu-id="ff60a-116">Diese Methode bestimmt, welche Patches nebeneinander liegen (innerhalb der bereitgestellten Toleranz).</span><span class="sxs-lookup"><span data-stu-id="ff60a-116">This method determines which patches are adjacent (within the provided tolerance).</span></span>

<span data-ttu-id="ff60a-117">Informationen zur Informations Optimierung werden auch verwendet, um den Mosaik Prozess zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="ff60a-117">Adjacency information is also used to optimize tessellation.</span></span> <span data-ttu-id="ff60a-118">Generieren Sie Informationen zu den Informationen einmal, und wiederholen Sie den Prozess durch Aufrufen von [**ID3DXPatchMesh::**](id3dxpatchmesh--tessellate.md)Mosaik.</span><span class="sxs-lookup"><span data-stu-id="ff60a-118">Generate adjacency information once and tessellate repeatedly by calling [**ID3DXPatchMesh::Tessellate**](id3dxpatchmesh--tessellate.md).</span></span> <span data-ttu-id="ff60a-119">Die ausgeführte Optimierung ist unabhängig von der tatsächlich verwendeten Mosaik Ebene.</span><span class="sxs-lookup"><span data-stu-id="ff60a-119">The optimization performed is independent of the actual tessellation level used.</span></span> <span data-ttu-id="ff60a-120">Wenn die Gitter Scheitel Punkte geändert werden, müssen Sie jedoch die Informationen zur Informationsquellen Generierung erneut generieren.</span><span class="sxs-lookup"><span data-stu-id="ff60a-120">However, if the mesh vertices are changed, you must regenerate the adjacency information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff60a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff60a-121">Requirements</span></span>



| <span data-ttu-id="ff60a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff60a-122">Requirement</span></span> | <span data-ttu-id="ff60a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="ff60a-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff60a-124">Header</span><span class="sxs-lookup"><span data-stu-id="ff60a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ff60a-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff60a-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ff60a-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ff60a-126">Library</span></span><br/> | <dl> <span data-ttu-id="ff60a-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff60a-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ff60a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff60a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff60a-129">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="ff60a-129">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="ff60a-130">**ID3DXPatchMesh:: generateency**</span><span class="sxs-lookup"><span data-stu-id="ff60a-130">**ID3DXPatchMesh::GenerateAdjacency**</span></span>](id3dxpatchmesh--generateadjacency.md)
</dt> </dl>

 

 
