---
description: Führt ein einheitliches Mosaik basierend auf der Mosaik Ebene aus.
ms.assetid: 0fc701b4-0636-450e-b8e0-e7a490871316
title: 'ID3DXPatchMesh:: tttellate-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Tessellate
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b94b79a9decd2f44fa1675e257a2401e2ae8f7a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373550"
---
# <a name="id3dxpatchmeshtessellate-method"></a><span data-ttu-id="caf4d-103">ID3DXPatchMesh:: Tess-Methode</span><span class="sxs-lookup"><span data-stu-id="caf4d-103">ID3DXPatchMesh::Tessellate method</span></span>

<span data-ttu-id="caf4d-104">Führt ein einheitliches Mosaik basierend auf der Mosaik Ebene aus.</span><span class="sxs-lookup"><span data-stu-id="caf4d-104">Performs uniform tessellation based on the tessellation level.</span></span>

## <a name="syntax"></a><span data-ttu-id="caf4d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="caf4d-105">Syntax</span></span>


```C++
HRESULT Tessellate(
  [in] FLOAT      fTessLevel,
  [in] LPD3DXMESH pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="caf4d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="caf4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caf4d-107">*ftess Level* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="caf4d-107">*fTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caf4d-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="caf4d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="caf4d-109">Mosaik Ebene.</span><span class="sxs-lookup"><span data-stu-id="caf4d-109">Tessellation level.</span></span> <span data-ttu-id="caf4d-110">Dies ist die Anzahl der Scheitel Punkte, die zwischen vorhandenen Vertices eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="caf4d-110">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="caf4d-111">Der Bereich dieses float-Parameters ist 0 < ftess Level <= 32.</span><span class="sxs-lookup"><span data-stu-id="caf4d-111">The range of this float parameter is 0 < fTessLevel <= 32.</span></span>

</dd> <dt>

<span data-ttu-id="caf4d-112">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="caf4d-112">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caf4d-113">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="caf4d-113">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="caf4d-114">Resultierende Mosaik Gitter.</span><span class="sxs-lookup"><span data-stu-id="caf4d-114">Resulting tessellated mesh.</span></span> <span data-ttu-id="caf4d-115">Siehe [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="caf4d-115">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caf4d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="caf4d-116">Return value</span></span>

<span data-ttu-id="caf4d-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="caf4d-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="caf4d-118">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="caf4d-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="caf4d-119">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="caf4d-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="caf4d-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="caf4d-120">Remarks</span></span>

<span data-ttu-id="caf4d-121">Diese Funktion wird effizienter durchgeführt, wenn das patchmesh mit [**ID3DXPatchMesh:: optimiert**](id3dxpatchmesh--optimize.md)optimiert wurde.</span><span class="sxs-lookup"><span data-stu-id="caf4d-121">This function will perform more efficiently if the patch mesh has been optimized using [**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="caf4d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="caf4d-122">Requirements</span></span>



| <span data-ttu-id="caf4d-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="caf4d-123">Requirement</span></span> | <span data-ttu-id="caf4d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="caf4d-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="caf4d-125">Header</span><span class="sxs-lookup"><span data-stu-id="caf4d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="caf4d-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="caf4d-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="caf4d-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="caf4d-127">Library</span></span><br/> | <dl> <span data-ttu-id="caf4d-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="caf4d-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="caf4d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="caf4d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caf4d-130">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="caf4d-130">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
