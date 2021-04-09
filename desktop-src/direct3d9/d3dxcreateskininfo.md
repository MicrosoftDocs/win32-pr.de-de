---
description: Erstellt ein leeres Skin-Mesh-Objekt mit einem Deklarator.
ms.assetid: c98da2e5-a9eb-4070-8846-b346b5c57fb3
title: D3DXCreateSkinInfo-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfo
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 83ee214eb997414e113256060dbe59d3cd47d1a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870111"
---
# <a name="d3dxcreateskininfo-function"></a><span data-ttu-id="f4628-103">D3DXCreateSkinInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="f4628-103">D3DXCreateSkinInfo function</span></span>

<span data-ttu-id="f4628-104">Erstellt ein leeres Skin-Mesh-Objekt mit einem Deklarator.</span><span class="sxs-lookup"><span data-stu-id="f4628-104">Creates an empty skin mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4628-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4628-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfo(
  _In_        DWORD             NumVertices,
  _In_  const D3DVERTEXELEMENT9 *pDeclaration,
  _In_        DWORD             NumBones,
  _Out_       LPD3DXSKININFO    *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="f4628-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4628-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4628-107">*Numvertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4628-107">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4628-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4628-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f4628-109">Anzahl der Scheitel Punkte für das Skin-Mesh.</span><span class="sxs-lookup"><span data-stu-id="f4628-109">Number of vertices for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="f4628-110">*pdeclaration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4628-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4628-111">Typ: **Konstanten [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="f4628-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="f4628-112">Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen, das das Scheitelpunkt Format für das zurückgegebene Mesh beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f4628-112">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="f4628-113">*Numbones* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4628-113">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4628-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4628-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f4628-115">Anzahl der Knochen für das Skin-Mesh.</span><span class="sxs-lookup"><span data-stu-id="f4628-115">Number of bones for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="f4628-116">*ppskininfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f4628-116">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4628-117">Typ: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="f4628-117">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="f4628-118">Adresse eines Zeigers auf eine [**ID3DXSkinInfo**](id3dxskininfo.md) -Schnittstelle, die das erstellte Skin-Mesh-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="f4628-118">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4628-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4628-119">Return value</span></span>

<span data-ttu-id="f4628-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f4628-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f4628-121">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f4628-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f4628-122">Wenn die Funktion fehlschlägt, kann der Rückgabewert lauten: E \_ outo-Memory.</span><span class="sxs-lookup"><span data-stu-id="f4628-122">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4628-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4628-123">Remarks</span></span>

<span data-ttu-id="f4628-124">Verwenden Sie [**setboneinfluence**](id3dxskininfo--setboneinfluence.md) , um das leere Skin-Mesh-Objekt aufzufüllen, das von dieser Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f4628-124">Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4628-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4628-125">Requirements</span></span>



| <span data-ttu-id="f4628-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4628-126">Requirement</span></span> | <span data-ttu-id="f4628-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f4628-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4628-128">Header</span><span class="sxs-lookup"><span data-stu-id="f4628-128">Header</span></span><br/>  | <dl> <span data-ttu-id="f4628-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4628-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f4628-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f4628-130">Library</span></span><br/> | <dl> <span data-ttu-id="f4628-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4628-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f4628-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4628-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4628-133">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="f4628-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="f4628-134">**Setboneingefluence**</span><span class="sxs-lookup"><span data-stu-id="f4628-134">**SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
