---
description: Erstellt ein neues patchmesh mit der angegebenen Scheitelpunkt Deklaration.
ms.assetid: cc488cd3-fb38-468f-8aec-17c6ed842582
title: 'ID3DXPatchMesh:: clonemesh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 249b4282aa84e3f7c5ba619a0b42e8c0b1fdf846
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354326"
---
# <a name="id3dxpatchmeshclonemesh-method"></a><span data-ttu-id="06a09-103">ID3DXPatchMesh:: clonemesh-Methode</span><span class="sxs-lookup"><span data-stu-id="06a09-103">ID3DXPatchMesh::CloneMesh method</span></span>

<span data-ttu-id="06a09-104">Erstellt ein neues patchmesh mit der angegebenen Scheitelpunkt Deklaration.</span><span class="sxs-lookup"><span data-stu-id="06a09-104">Creates a new patch mesh with the specified vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="06a09-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="06a09-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDecl,
  [out, retval]       LPD3DXPATCHMESH   *pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="06a09-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="06a09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06a09-107">*Optionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06a09-107">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06a09-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06a09-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06a09-109">Kombination aus einem oder mehreren [**D3DXMESH**](./d3dxmesh.md) -Flags, die Erstellungs Optionen für das Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="06a09-109">Combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="06a09-110">*pdecl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06a09-110">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06a09-111">Typ: **Konstanten [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="06a09-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="06a09-112">Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen, die das Scheitelpunkt Format für die Scheitel Punkte im Ausgabe Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="06a09-112">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements that specify the vertex format for the vertices in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="06a09-113">*pmesh* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="06a09-113">*pMesh* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="06a09-114">Typ: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="06a09-114">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="06a09-115">Adresse eines Zeigers auf eine [**ID3DXPatchMesh**](id3dxpatchmesh.md) -Schnittstelle, die das geklonte Mesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="06a09-115">Address of a pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface that represents the cloned mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06a09-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06a09-116">Return value</span></span>

<span data-ttu-id="06a09-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="06a09-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="06a09-118">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="06a09-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="06a09-119">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="06a09-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="06a09-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06a09-120">Remarks</span></span>

<span data-ttu-id="06a09-121">**Clonemesh** konvertiert den Scheitelpunkt Puffer in die neue Scheitelpunkt Deklaration.</span><span class="sxs-lookup"><span data-stu-id="06a09-121">**CloneMesh** converts the vertex buffer to the new vertex declaration.</span></span> <span data-ttu-id="06a09-122">Einträge in der Vertex-Deklaration, die neu im ursprünglichen Mesh sind, werden auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="06a09-122">Entries in the vertex declaration that are new to the original mesh are set to 0.</span></span> <span data-ttu-id="06a09-123">Wenn das aktuelle Mesh über eine beliebige Konsistenz verfügt, ist das neue Mesh ebenfalls mit der Sicherheit vertraut.</span><span class="sxs-lookup"><span data-stu-id="06a09-123">If the current mesh has adjacency, the new mesh will also have adjacency.</span></span>

## <a name="requirements"></a><span data-ttu-id="06a09-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06a09-124">Requirements</span></span>



| <span data-ttu-id="06a09-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06a09-125">Requirement</span></span> | <span data-ttu-id="06a09-126">Wert</span><span class="sxs-lookup"><span data-stu-id="06a09-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06a09-127">Header</span><span class="sxs-lookup"><span data-stu-id="06a09-127">Header</span></span><br/>  | <dl> <span data-ttu-id="06a09-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="06a09-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="06a09-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="06a09-129">Library</span></span><br/> | <dl> <span data-ttu-id="06a09-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06a09-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="06a09-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06a09-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06a09-132">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="06a09-132">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
