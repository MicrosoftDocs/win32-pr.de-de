---
description: Ruft den Blend Faktor und den Scheitelpunkt ab, der von einem angegebenen Knochen Einfluss betroffen ist.
ms.assetid: bbed4766-e571-4a9e-b7e3-047052470cbe
title: 'ID3DXSkinInfo:: getbonevertexinfluence-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e3cb7c530ed72a65f9a3e8de6b0735b1a7ae5e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354076"
---
# <a name="id3dxskininfogetbonevertexinfluence-method"></a><span data-ttu-id="33c9b-103">ID3DXSkinInfo:: getbonevertexinfluence-Methode</span><span class="sxs-lookup"><span data-stu-id="33c9b-103">ID3DXSkinInfo::GetBoneVertexInfluence method</span></span>

<span data-ttu-id="33c9b-104">Ruft den Blend Faktor und den Scheitelpunkt ab, der von einem angegebenen Knochen Einfluss betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="33c9b-104">Retrieves the blend factor and vertex affected by a specified bone influence.</span></span>

## <a name="syntax"></a><span data-ttu-id="33c9b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="33c9b-105">Syntax</span></span>


```C++
HRESULT GetBoneVertexInfluence(
  [in]      DWORD boneNum,
  [in]      DWORD influenceNum,
  [in, out] FLOAT *pWeight,
  [in, out] DWORD *pVertexNum
);
```



## <a name="parameters"></a><span data-ttu-id="33c9b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="33c9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33c9b-107">*bonumum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33c9b-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c9b-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33c9b-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33c9b-109">Der Index des-Knochens.</span><span class="sxs-lookup"><span data-stu-id="33c9b-109">Index of the bone.</span></span> <span data-ttu-id="33c9b-110">Muss zwischen 0 und der Anzahl der Knochen liegen.</span><span class="sxs-lookup"><span data-stu-id="33c9b-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="33c9b-111">*Einflussfaktoren* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33c9b-111">*influenceNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c9b-112">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33c9b-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33c9b-113">Index des Einfluss Arrays des angegebenen Knochen.</span><span class="sxs-lookup"><span data-stu-id="33c9b-113">Index of the influence array of the specified bone.</span></span>

</dd> <dt>

<span data-ttu-id="33c9b-114">*pweight* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="33c9b-114">*pWeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="33c9b-115">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="33c9b-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="33c9b-116">Zeiger auf den Blend-Faktor, der durch Einflussfaktoren beeinflusst wird.</span><span class="sxs-lookup"><span data-stu-id="33c9b-116">Pointer to the blend factor influenced by influenceNum.</span></span>

</dd> <dt>

<span data-ttu-id="33c9b-117">*pvertexnum* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="33c9b-117">*pVertexNum* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="33c9b-118">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="33c9b-118">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="33c9b-119">Zeiger auf den Scheitelpunkt, der durch Einflussfaktoren beeinflusst wird.</span><span class="sxs-lookup"><span data-stu-id="33c9b-119">Pointer to the vertex influenced by influenceNum.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33c9b-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33c9b-120">Return value</span></span>

<span data-ttu-id="33c9b-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="33c9b-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="33c9b-122">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="33c9b-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="33c9b-123">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="33c9b-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="33c9b-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33c9b-124">Requirements</span></span>



| <span data-ttu-id="33c9b-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33c9b-125">Requirement</span></span> | <span data-ttu-id="33c9b-126">Wert</span><span class="sxs-lookup"><span data-stu-id="33c9b-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33c9b-127">Header</span><span class="sxs-lookup"><span data-stu-id="33c9b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="33c9b-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="33c9b-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="33c9b-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="33c9b-129">Library</span></span><br/> | <dl> <span data-ttu-id="33c9b-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33c9b-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="33c9b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33c9b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33c9b-132">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="33c9b-132">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="33c9b-133">**ID3DXSkinInfo:: setbonevertexinfluence**</span><span class="sxs-lookup"><span data-stu-id="33c9b-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span></span>](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="33c9b-134">**ID3DXSkinInfo:: findbonevertexinfluendceindex**</span><span class="sxs-lookup"><span data-stu-id="33c9b-134">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span></span>](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[<span data-ttu-id="33c9b-135">**ID3DXSkinInfo:: getboneingefluence**</span><span class="sxs-lookup"><span data-stu-id="33c9b-135">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
