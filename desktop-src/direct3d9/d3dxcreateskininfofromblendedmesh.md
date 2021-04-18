---
description: Erstellt ein Skin-Mesh aus einem anderen Mesh.
ms.assetid: 4c69377e-61ef-42b8-8864-c116164d4b22
title: D3DXCreateSkinInfoFromBlendedMesh-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFromBlendedMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d81de43dde2b4f0df5913831ddfcefbab1a41855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530926"
---
# <a name="d3dxcreateskininfofromblendedmesh-function"></a><span data-ttu-id="50e59-103">D3DXCreateSkinInfoFromBlendedMesh-Funktion</span><span class="sxs-lookup"><span data-stu-id="50e59-103">D3DXCreateSkinInfoFromBlendedMesh function</span></span>

<span data-ttu-id="50e59-104">Erstellt ein Skin-Mesh aus einem anderen Mesh.</span><span class="sxs-lookup"><span data-stu-id="50e59-104">Creates a skin mesh from another mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e59-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="50e59-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfoFromBlendedMesh(
  _In_        LPD3DXBASEMESH      pMesh,
  _In_        DWORD               NumBones,
  _In_  const D3DXBONECOMBINATION *pBoneCombinationTable,
  _Out_       LPD3DXSKININFO      *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="50e59-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50e59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50e59-107">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50e59-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50e59-108">Typ: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="50e59-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="50e59-109">Zeiger auf ein [**ID3DXBaseMesh**](id3dxbasemesh.md) -Objekt, das Mesh, aus dem das Skin Mesh erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="50e59-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) object, the mesh from which to create the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="50e59-110">*Numbones* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50e59-110">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50e59-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50e59-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50e59-112">Die Länge des Arrays, das an die boneid angehängt ist.</span><span class="sxs-lookup"><span data-stu-id="50e59-112">The length of the array attached to the BoneId.</span></span> <span data-ttu-id="50e59-113">Siehe [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span><span class="sxs-lookup"><span data-stu-id="50e59-113">See [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span></span>

</dd> <dt>

<span data-ttu-id="50e59-114">*pbonecombinationtable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50e59-114">*pBoneCombinationTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50e59-115">Typ: **Konstanten [**D3DXBONECOMBINATION**](d3dxbonecombination.md) \***</span><span class="sxs-lookup"><span data-stu-id="50e59-115">Type: **const [**D3DXBONECOMBINATION**](d3dxbonecombination.md)\***</span></span>

<span data-ttu-id="50e59-116">Zeiger auf ein Array von Bone-Kombinationen.</span><span class="sxs-lookup"><span data-stu-id="50e59-116">Pointer to an array of bone combinations.</span></span> <span data-ttu-id="50e59-117">Siehe [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span><span class="sxs-lookup"><span data-stu-id="50e59-117">See [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span></span>

</dd> <dt>

<span data-ttu-id="50e59-118">*ppskininfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="50e59-118">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50e59-119">Typ: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="50e59-119">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="50e59-120">Adresse eines Zeigers auf eine [**ID3DXSkinInfo**](id3dxskininfo.md) -Schnittstelle, die das erstellte Skin-Mesh-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="50e59-120">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50e59-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50e59-121">Return value</span></span>

<span data-ttu-id="50e59-122">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="50e59-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="50e59-123">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="50e59-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="50e59-124">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: E \_ outo-Memory.</span><span class="sxs-lookup"><span data-stu-id="50e59-124">If the function fails, the return value can be the following: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="50e59-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50e59-125">Requirements</span></span>



| <span data-ttu-id="50e59-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50e59-126">Requirement</span></span> | <span data-ttu-id="50e59-127">Wert</span><span class="sxs-lookup"><span data-stu-id="50e59-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50e59-128">Header</span><span class="sxs-lookup"><span data-stu-id="50e59-128">Header</span></span><br/>  | <dl> <span data-ttu-id="50e59-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="50e59-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="50e59-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="50e59-130">Library</span></span><br/> | <dl> <span data-ttu-id="50e59-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50e59-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="50e59-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50e59-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50e59-133">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="50e59-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
