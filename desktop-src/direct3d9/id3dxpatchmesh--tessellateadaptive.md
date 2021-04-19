---
description: Führt ein adaptives Mosaik basierend auf dem z-basierten adaptiven Mosaik Kriterium aus.
ms.assetid: 9f8f5c18-e866-4893-ba07-2a3c0d26c028
title: 'ID3DXPatchMesh:: tttellateadaptive-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.TessellateAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4cc6c6b7ff7b0cdb99e56386df49529f26c9166
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353377"
---
# <a name="id3dxpatchmeshtessellateadaptive-method"></a><span data-ttu-id="bb227-103">ID3DXPatchMesh:: Tess. Adaptive-Methode</span><span class="sxs-lookup"><span data-stu-id="bb227-103">ID3DXPatchMesh::TessellateAdaptive method</span></span>

<span data-ttu-id="bb227-104">Führt ein adaptives Mosaik basierend auf dem z-basierten adaptiven Mosaik Kriterium aus.</span><span class="sxs-lookup"><span data-stu-id="bb227-104">Performs adaptive tessellation based on the z-based adaptive tessellation criterion.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb227-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb227-105">Syntax</span></span>


```C++
HRESULT TessellateAdaptive(
  [in] const D3DXVECTOR4 *pTrans,
  [in]       DWORD       dwMaxTessLevel,
  [in]       DWORD       dwMinTessLevel,
  [in]       LPD3DXMESH  pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="bb227-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb227-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb227-107">*ptrans* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb227-107">*pTrans* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb227-108">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="bb227-108">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="bb227-109">Gibt einen 4D-Vektor an, der mit den Scheitel Punkten dargestellt wird, um die pro-vertexadaptive Mosaik Menge zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bb227-109">Specifies a 4D vector that is dotted with the vertices to get the per-vertex adaptive tessellation amount.</span></span> <span data-ttu-id="bb227-110">Jeder Rand wird auf den Durchschnittswert der Mosaik Ebenen für die beiden Scheitel Punkte, die er verbindet, festgesetzt.</span><span class="sxs-lookup"><span data-stu-id="bb227-110">Each edge is tessellated to the average value of the tessellation levels for the two vertices it connects.</span></span>

</dd> <dt>

<span data-ttu-id="bb227-111">*dwmaxtess Level* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb227-111">*dwMaxTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb227-112">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb227-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb227-113">Maximale Beschränkung für das adaptive Mosaik.</span><span class="sxs-lookup"><span data-stu-id="bb227-113">Maximum limit for adaptive tessellation.</span></span> <span data-ttu-id="bb227-114">Dies ist die Anzahl der Scheitel Punkte, die zwischen vorhandenen Vertices eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="bb227-114">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="bb227-115">Dieser ganzzahlige Wert kann zwischen 1 und 32 (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="bb227-115">This integer value can range from 1 to 32, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="bb227-116">*dwmintess Level* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb227-116">*dwMinTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb227-117">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb227-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb227-118">Mindestgrenzwert für das adaptive Mosaik.</span><span class="sxs-lookup"><span data-stu-id="bb227-118">Minimum limit for adaptive tessellation.</span></span> <span data-ttu-id="bb227-119">Dies ist die Anzahl der Scheitel Punkte, die zwischen vorhandenen Vertices eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="bb227-119">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="bb227-120">Dieser ganzzahlige Wert kann zwischen 1 und 32 (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="bb227-120">This integer value can range from 1 to 32, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="bb227-121">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb227-121">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb227-122">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="bb227-122">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="bb227-123">Resultierende Mosaik Gitter.</span><span class="sxs-lookup"><span data-stu-id="bb227-123">Resulting tessellated mesh.</span></span> <span data-ttu-id="bb227-124">Siehe [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="bb227-124">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb227-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb227-125">Return value</span></span>

<span data-ttu-id="bb227-126">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bb227-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bb227-127">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bb227-127">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bb227-128">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="bb227-128">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb227-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb227-129">Remarks</span></span>

<span data-ttu-id="bb227-130">Diese Funktion wird effizienter durchgeführt, wenn das patchmesh mit [**ID3DXPatchMesh:: optimiert**](id3dxpatchmesh--optimize.md)optimiert wurde.</span><span class="sxs-lookup"><span data-stu-id="bb227-130">This function will perform more efficiently if the patch mesh has been optimized using [**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb227-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb227-131">Requirements</span></span>



| <span data-ttu-id="bb227-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb227-132">Requirement</span></span> | <span data-ttu-id="bb227-133">Wert</span><span class="sxs-lookup"><span data-stu-id="bb227-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb227-134">Header</span><span class="sxs-lookup"><span data-stu-id="bb227-134">Header</span></span><br/>  | <dl> <span data-ttu-id="bb227-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb227-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bb227-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bb227-136">Library</span></span><br/> | <dl> <span data-ttu-id="bb227-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb227-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bb227-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb227-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb227-139">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="bb227-139">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
