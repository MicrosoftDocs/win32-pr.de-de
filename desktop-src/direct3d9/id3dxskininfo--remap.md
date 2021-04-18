---
description: Aktualisiert die Informationen zu den Informationen zu den Daten, die nach dem erneuten ordnen der Scheitel Punkte entsprechen Diese Methode sollte aufgerufen werden, wenn der Ziel Vertex-Puffer extern neu angeordnet wurde.
ms.assetid: bff5229f-e547-4ab3-84c6-58b15a7825e9
title: 'ID3DXSkinInfo:: remap-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Remap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 657cf0977592a8e19e68b8aeb950c62d404e7cdb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354974"
---
# <a name="id3dxskininforemap-method"></a><span data-ttu-id="a8d83-104">ID3DXSkinInfo:: remap-Methode</span><span class="sxs-lookup"><span data-stu-id="a8d83-104">ID3DXSkinInfo::Remap method</span></span>

<span data-ttu-id="a8d83-105">Aktualisiert die Informationen zu den Informationen zu den Daten, die nach dem erneuten ordnen der Scheitel Punkte entsprechen</span><span class="sxs-lookup"><span data-stu-id="a8d83-105">Updates bone influence information to match vertices after they are reordered.</span></span> <span data-ttu-id="a8d83-106">Diese Methode sollte aufgerufen werden, wenn der Ziel Vertex-Puffer extern neu angeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="a8d83-106">This method should be called if the target vertex buffer has been reordered externally.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8d83-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8d83-107">Syntax</span></span>


```C++
HRESULT Remap(
  [in] DWORD NumVertices,
  [in] DWORD *pVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="a8d83-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8d83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8d83-109">*Numvertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8d83-109">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d83-110">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8d83-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a8d83-111">Anzahl der zu neuumwandenden Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="a8d83-111">Number of vertices to remap.</span></span>

</dd> <dt>

<span data-ttu-id="a8d83-112">*pvertexremap* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8d83-112">*pVertexRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d83-113">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8d83-113">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a8d83-114">Ein Array von DWords, dessen Länge durch numvertices angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a8d83-114">Array of DWORDS whose length is specified by NumVertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8d83-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8d83-115">Return value</span></span>

<span data-ttu-id="a8d83-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a8d83-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a8d83-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a8d83-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a8d83-118">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="a8d83-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8d83-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8d83-119">Remarks</span></span>

<span data-ttu-id="a8d83-120">Jedes Element in pvertexremap gibt den vorherigen Scheitelpunkt Index für diese Position an.</span><span class="sxs-lookup"><span data-stu-id="a8d83-120">Each element in pVertexRemap specifies the previous vertex index for that position.</span></span> <span data-ttu-id="a8d83-121">Wenn sich z. b. ein Scheitelpunkt an Position 3, aber an Position 5 neu zugeordnet wurde, sollte das fünfte Element von pvertexremap 3 enthalten.</span><span class="sxs-lookup"><span data-stu-id="a8d83-121">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap should contain 3.</span></span> <span data-ttu-id="a8d83-122">Das von [**ID3DXMesh:: optimiert**](id3dxmesh--optimize.md) zurückgegebene Vertex-neuumwandlungs Array kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a8d83-122">The vertex remap array returned by [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) can be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8d83-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8d83-123">Requirements</span></span>



| <span data-ttu-id="a8d83-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8d83-124">Requirement</span></span> | <span data-ttu-id="a8d83-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a8d83-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8d83-126">Header</span><span class="sxs-lookup"><span data-stu-id="a8d83-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a8d83-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8d83-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a8d83-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a8d83-128">Library</span></span><br/> | <dl> <span data-ttu-id="a8d83-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8d83-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a8d83-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8d83-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8d83-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="a8d83-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
