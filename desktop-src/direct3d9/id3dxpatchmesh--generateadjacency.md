---
description: Generiert eine Liste der Gitter Kanten und der Patches, die die einzelnen Kanten gemeinsam verwenden.
ms.assetid: 024528c0-2c0d-4448-9b38-05cf8d6ffc63
title: 'ID3DXPatchMesh:: generateaccessency-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68de2a77b9d27391c57ec299ceb87d29166ee248
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394066"
---
# <a name="id3dxpatchmeshgenerateadjacency-method"></a><span data-ttu-id="f7ade-103">ID3DXPatchMesh:: generateaccessency-Methode</span><span class="sxs-lookup"><span data-stu-id="f7ade-103">ID3DXPatchMesh::GenerateAdjacency method</span></span>

<span data-ttu-id="f7ade-104">Generiert eine Liste der Gitter Kanten und der Patches, die die einzelnen Kanten gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7ade-104">Generate a list of mesh edges and the patches that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7ade-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7ade-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT fTolerance
);
```



## <a name="parameters"></a><span data-ttu-id="f7ade-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7ade-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7ade-107">*ftolerance* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7ade-107">*fTolerance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7ade-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7ade-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f7ade-109">Gibt an, dass Scheitel Punkte, die sich an der Position um weniger als die Toleranz unterscheiden, als Coincident behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f7ade-109">Specifies that vertices that differ in position by less than the tolerance should be treated as coincident.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7ade-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f7ade-110">Return value</span></span>

<span data-ttu-id="f7ade-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f7ade-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f7ade-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f7ade-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f7ade-113">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="f7ade-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7ade-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7ade-114">Remarks</span></span>

<span data-ttu-id="f7ade-115">Nachdem eine Anwendung Informationen zu einem Mesh generiert hat, können die Mesh-Daten optimiert werden, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="f7ade-115">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span> <span data-ttu-id="f7ade-116">Diese Methode bestimmt, welche Patches nebeneinander liegen (innerhalb der bereitgestellten Toleranz).</span><span class="sxs-lookup"><span data-stu-id="f7ade-116">This method determines which patches are adjacent (within the provided tolerance).</span></span> <span data-ttu-id="f7ade-117">Diese Informationen werden intern verwendet, um den Mosaik Prozess zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="f7ade-117">This information is used internally to optimize tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7ade-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f7ade-118">Requirements</span></span>



| <span data-ttu-id="f7ade-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7ade-119">Requirement</span></span> | <span data-ttu-id="f7ade-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f7ade-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7ade-121">Header</span><span class="sxs-lookup"><span data-stu-id="f7ade-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f7ade-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7ade-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f7ade-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f7ade-123">Library</span></span><br/> | <dl> <span data-ttu-id="f7ade-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7ade-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f7ade-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7ade-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7ade-126">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="f7ade-126">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="f7ade-127">**ID3DXPatchMesh:: optimieren**</span><span class="sxs-lookup"><span data-stu-id="f7ade-127">**ID3DXPatchMesh::Optimize**</span></span>](id3dxpatchmesh--optimize.md)
</dt> </dl>

 

 
