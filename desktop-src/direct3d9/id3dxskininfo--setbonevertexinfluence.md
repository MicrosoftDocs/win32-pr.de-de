---
description: Legt einen Einfluss Wert eines Knotens in einem einzelnen Scheitelpunkt fest.
ms.assetid: 9283866f-3dfe-467d-a74f-77e89c2778c4
title: 'ID3DXSkinInfo:: setbonevertexinfluence-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: db84cdf9a1647bc5302c421e52d50f812e74596e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365068"
---
# <a name="id3dxskininfosetbonevertexinfluence-method"></a><span data-ttu-id="21c5a-103">ID3DXSkinInfo:: setbonevertexinfluence-Methode</span><span class="sxs-lookup"><span data-stu-id="21c5a-103">ID3DXSkinInfo::SetBoneVertexInfluence method</span></span>

<span data-ttu-id="21c5a-104">Legt einen Einfluss Wert eines Knotens in einem einzelnen Scheitelpunkt fest.</span><span class="sxs-lookup"><span data-stu-id="21c5a-104">Sets an influence value of a bone on a single vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="21c5a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="21c5a-105">Syntax</span></span>


```C++
HRESULT SetBoneVertexInfluence(
  [in] DWORD boneNum,
  [in] DWORD influenceNum,
  [in] FLOAT weight
);
```



## <a name="parameters"></a><span data-ttu-id="21c5a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="21c5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21c5a-107">*bonumum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21c5a-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21c5a-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21c5a-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21c5a-109">Der Index des-Knochens.</span><span class="sxs-lookup"><span data-stu-id="21c5a-109">Index of the bone.</span></span> <span data-ttu-id="21c5a-110">Muss zwischen 0 und der Anzahl der Knochen liegen.</span><span class="sxs-lookup"><span data-stu-id="21c5a-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="21c5a-111">*Einflussfaktoren* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21c5a-111">*influenceNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21c5a-112">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21c5a-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21c5a-113">Index des Einfluss Arrays des angegebenen Knochen.</span><span class="sxs-lookup"><span data-stu-id="21c5a-113">Index of the influence array of the specified bone.</span></span>

</dd> <dt>

<span data-ttu-id="21c5a-114">*Gewichtung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21c5a-114">*weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21c5a-115">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21c5a-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21c5a-116">Der Blend-Faktor des angegebenen Knochen Einflusses.</span><span class="sxs-lookup"><span data-stu-id="21c5a-116">Blend factor of the specified bone influence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21c5a-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21c5a-117">Return value</span></span>

<span data-ttu-id="21c5a-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="21c5a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="21c5a-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="21c5a-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="21c5a-120">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="21c5a-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="21c5a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21c5a-121">Requirements</span></span>



| <span data-ttu-id="21c5a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21c5a-122">Requirement</span></span> | <span data-ttu-id="21c5a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="21c5a-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21c5a-124">Header</span><span class="sxs-lookup"><span data-stu-id="21c5a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="21c5a-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="21c5a-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="21c5a-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="21c5a-126">Library</span></span><br/> | <dl> <span data-ttu-id="21c5a-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21c5a-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="21c5a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21c5a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21c5a-129">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="21c5a-129">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="21c5a-130">**ID3DXSkinInfo:: getbonevertexinfluence**</span><span class="sxs-lookup"><span data-stu-id="21c5a-130">**ID3DXSkinInfo::GetBoneVertexInfluence**</span></span>](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="21c5a-131">**ID3DXSkinInfo:: findbonevertexinfluendceindex**</span><span class="sxs-lookup"><span data-stu-id="21c5a-131">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span></span>](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[<span data-ttu-id="21c5a-132">**ID3DXSkinInfo:: getboneingefluence**</span><span class="sxs-lookup"><span data-stu-id="21c5a-132">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
