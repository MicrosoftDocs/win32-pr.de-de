---
description: Ruft den Index des Knochen Einflusses ab, der sich auf einen einzelnen Scheitelpunkt auswirkt.
ms.assetid: vs|directx_sdk|~\id3dxskininfo__findbonevertexinfluenceindex.htm
title: 'ID3DXSkinInfo:: findbonevertexinfluendceindex-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.FindBoneVertexInfluenceIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05a86e98e5001092700fdec12f2a7afc33ddf082
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366433"
---
# <a name="id3dxskininfofindbonevertexinfluenceindex-method"></a><span data-ttu-id="dc2a1-103">ID3DXSkinInfo:: findbonevertexinfluendceindex-Methode</span><span class="sxs-lookup"><span data-stu-id="dc2a1-103">ID3DXSkinInfo::FindBoneVertexInfluenceIndex method</span></span>

<span data-ttu-id="dc2a1-104">Ruft den Index des Knochen Einflusses ab, der sich auf einen einzelnen Scheitelpunkt auswirkt.</span><span class="sxs-lookup"><span data-stu-id="dc2a1-104">Retrieves the index of the bone influence affecting a single vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc2a1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc2a1-105">Syntax</span></span>


```C++
HRESULT FindBoneVertexInfluenceIndex(
  [in]      DWORD boneNum,
  [in]      DWORD vertexNum,
  [in, out] DWORD *pInfluenceIndex
);
```



## <a name="parameters"></a><span data-ttu-id="dc2a1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc2a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc2a1-107">*bonumum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc2a1-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc2a1-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc2a1-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc2a1-109">Der Index des-Knochens.</span><span class="sxs-lookup"><span data-stu-id="dc2a1-109">Index of the bone.</span></span> <span data-ttu-id="dc2a1-110">Muss zwischen 0 und der Anzahl der Knochen liegen.</span><span class="sxs-lookup"><span data-stu-id="dc2a1-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="dc2a1-111">*vertexnum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc2a1-111">*vertexNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc2a1-112">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc2a1-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc2a1-113">Der Index des Scheitel Punkts, für den der Knochen Einfluss gefunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc2a1-113">Index of the vertex for which the bone influence is to be found.</span></span> <span data-ttu-id="dc2a1-114">Muss zwischen 0 und der Anzahl der Scheitel Punkte im Mesh liegen.</span><span class="sxs-lookup"><span data-stu-id="dc2a1-114">Must be between 0 and the number of vertices in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="dc2a1-115">*pinfluendceindex* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="dc2a1-115">*pInfluenceIndex* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc2a1-116">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="dc2a1-116">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dc2a1-117">Zeiger auf den Index des Knochen Einflusses, der vertexnum beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="dc2a1-117">Pointer to the index of the bone influence that affects vertexNum.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc2a1-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc2a1-118">Return value</span></span>

<span data-ttu-id="dc2a1-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dc2a1-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dc2a1-120">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dc2a1-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="dc2a1-121">Wenn der angegebene Knochen den angegebenen Scheitelpunkt nicht beeinflusst, \_ wird "false" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dc2a1-121">If the specified bone does not influence the given vertex, S\_FALSE is returned.</span></span> <span data-ttu-id="dc2a1-122">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="dc2a1-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc2a1-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc2a1-123">Requirements</span></span>



| <span data-ttu-id="dc2a1-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc2a1-124">Requirement</span></span> | <span data-ttu-id="dc2a1-125">Wert</span><span class="sxs-lookup"><span data-stu-id="dc2a1-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc2a1-126">Header</span><span class="sxs-lookup"><span data-stu-id="dc2a1-126">Header</span></span><br/>  | <dl> <span data-ttu-id="dc2a1-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc2a1-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dc2a1-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dc2a1-128">Library</span></span><br/> | <dl> <span data-ttu-id="dc2a1-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc2a1-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dc2a1-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc2a1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc2a1-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="dc2a1-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="dc2a1-132">**ID3DXSkinInfo:: getbonevertexinfluence**</span><span class="sxs-lookup"><span data-stu-id="dc2a1-132">**ID3DXSkinInfo::GetBoneVertexInfluence**</span></span>](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="dc2a1-133">**ID3DXSkinInfo:: setbonevertexinfluence**</span><span class="sxs-lookup"><span data-stu-id="dc2a1-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span></span>](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="dc2a1-134">**ID3DXSkinInfo:: getboneingefluence**</span><span class="sxs-lookup"><span data-stu-id="dc2a1-134">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
