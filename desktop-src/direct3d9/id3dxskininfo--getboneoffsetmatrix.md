---
description: Ruft die markveroffsetmatrix ab.
ms.assetid: 99d47635-ffae-4668-a37c-b15442148fa1
title: 'ID3DXSkinInfo:: getboneoffsetmatrix-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fce108dc1d0eb08f198ae9375ac35ed149c5e760
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354096"
---
# <a name="id3dxskininfogetboneoffsetmatrix-method"></a><span data-ttu-id="b4595-103">ID3DXSkinInfo:: getboneoffsetmatrix-Methode</span><span class="sxs-lookup"><span data-stu-id="b4595-103">ID3DXSkinInfo::GetBoneOffsetMatrix method</span></span>

<span data-ttu-id="b4595-104">Ruft die markveroffsetmatrix ab.</span><span class="sxs-lookup"><span data-stu-id="b4595-104">Gets the bone offset matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4595-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4595-105">Syntax</span></span>


```C++
LPD3DXMATRIX GetBoneOffsetMatrix(
  [in] DWORD Bone
);
```



## <a name="parameters"></a><span data-ttu-id="b4595-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4595-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4595-107">*Knochen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4595-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4595-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4595-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b4595-109">Die Knochen Nummer.</span><span class="sxs-lookup"><span data-stu-id="b4595-109">Bone number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4595-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4595-110">Return value</span></span>

<span data-ttu-id="b4595-111">Typ: **[ **LPD3DXMATRIX**](d3dxmatrix.md)**</span><span class="sxs-lookup"><span data-stu-id="b4595-111">Type: **[**LPD3DXMATRIX**](d3dxmatrix.md)**</span></span>

<span data-ttu-id="b4595-112">Gibt einen Zeiger auf die Knochen Offset Matrix zurück.</span><span class="sxs-lookup"><span data-stu-id="b4595-112">Returns a pointer to the bone offset matrix.</span></span> <span data-ttu-id="b4595-113">Diesen Zeiger nicht freigeben.</span><span class="sxs-lookup"><span data-stu-id="b4595-113">Do not free this pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4595-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4595-114">Requirements</span></span>



| <span data-ttu-id="b4595-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4595-115">Requirement</span></span> | <span data-ttu-id="b4595-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b4595-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4595-117">Header</span><span class="sxs-lookup"><span data-stu-id="b4595-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b4595-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4595-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b4595-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b4595-119">Library</span></span><br/> | <dl> <span data-ttu-id="b4595-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4595-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b4595-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4595-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4595-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="b4595-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="b4595-123">**Setboneoffsetmatrix**</span><span class="sxs-lookup"><span data-stu-id="b4595-123">**SetBoneOffsetMatrix**</span></span>](id3dxskininfo--setboneoffsetmatrix.md)
</dt> <dt>

[<span data-ttu-id="b4595-124">**Getnumbones**</span><span class="sxs-lookup"><span data-stu-id="b4595-124">**GetNumBones**</span></span>](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
