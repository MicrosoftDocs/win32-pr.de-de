---
description: Erstellt ein leeres Skin-Mesh-Objekt mit einem flexiblen Scheitelpunkt Formatierungs Code (FVF).
ms.assetid: 72e27850-0102-4121-a397-16f2e0220b93
title: D3DXCreateSkinInfoFVF-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 907ab874b8cd8b766e6f9413212ba8771df9b25c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354372"
---
# <a name="d3dxcreateskininfofvf-function"></a><span data-ttu-id="e9f23-103">D3DXCreateSkinInfoFVF-Funktion</span><span class="sxs-lookup"><span data-stu-id="e9f23-103">D3DXCreateSkinInfoFVF function</span></span>

<span data-ttu-id="e9f23-104">Erstellt ein leeres Skin-Mesh-Objekt mit einem flexiblen Scheitelpunkt Formatierungs Code (FVF).</span><span class="sxs-lookup"><span data-stu-id="e9f23-104">Creates an empty skin mesh object using a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f23-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9f23-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfoFVF(
  _In_  DWORD          NumVertices,
  _In_  DWORD          FVF,
  _In_  DWORD          NumBones,
  _Out_ LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e9f23-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9f23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9f23-107">*Numvertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9f23-107">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f23-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e9f23-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e9f23-109">Anzahl der Scheitel Punkte für das Skin-Mesh.</span><span class="sxs-lookup"><span data-stu-id="e9f23-109">Number of vertices for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="e9f23-110">*F-VF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9f23-110">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f23-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e9f23-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e9f23-112">Eine Kombination aus [D3DFVF](d3dfvf.md) , die das Vertex-Format für das zurückgegebene Skin-Mesh beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e9f23-112">Combination of [D3DFVF](d3dfvf.md) that describes the vertex format for the returned skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="e9f23-113">*Numbones* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9f23-113">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f23-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e9f23-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e9f23-115">Anzahl der Knochen für das Skin-Mesh.</span><span class="sxs-lookup"><span data-stu-id="e9f23-115">Number of bones for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="e9f23-116">*ppskininfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e9f23-116">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f23-117">Typ: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="e9f23-117">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="e9f23-118">Adresse eines Zeigers auf eine [**ID3DXSkinInfo**](id3dxskininfo.md) -Schnittstelle, die das erstellte Skin Information-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="e9f23-118">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, representing the created skin information object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9f23-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9f23-119">Return value</span></span>

<span data-ttu-id="e9f23-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e9f23-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e9f23-121">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e9f23-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e9f23-122">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="e9f23-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9f23-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9f23-123">Remarks</span></span>

<span data-ttu-id="e9f23-124">Verwenden Sie [**setboneinfluence**](id3dxskininfo--setboneinfluence.md) , um das leere Skin-Mesh-Objekt aufzufüllen, das von dieser Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e9f23-124">Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9f23-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9f23-125">Requirements</span></span>



| <span data-ttu-id="e9f23-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9f23-126">Requirement</span></span> | <span data-ttu-id="e9f23-127">Wert</span><span class="sxs-lookup"><span data-stu-id="e9f23-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f23-128">Header</span><span class="sxs-lookup"><span data-stu-id="e9f23-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e9f23-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9f23-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e9f23-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e9f23-130">Library</span></span><br/> | <dl> <span data-ttu-id="e9f23-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9f23-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e9f23-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9f23-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f23-133">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e9f23-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="e9f23-134">**Setboneingefluence**</span><span class="sxs-lookup"><span data-stu-id="e9f23-134">**SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
