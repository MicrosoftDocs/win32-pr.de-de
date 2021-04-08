---
description: Legt die markveroffsetmatrix fest.
ms.assetid: f8ac1117-510d-42af-a6bf-422cbaaf6b74
title: 'ID3DXSkinInfo:: setboneoffsetmatrix-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 283d36bb68e33cfa0e2349bab304b0cdde7ef77e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761919"
---
# <a name="id3dxskininfosetboneoffsetmatrix-method"></a><span data-ttu-id="34334-103">ID3DXSkinInfo:: setboneoffsetmatrix-Methode</span><span class="sxs-lookup"><span data-stu-id="34334-103">ID3DXSkinInfo::SetBoneOffsetMatrix method</span></span>

<span data-ttu-id="34334-104">Legt die markveroffsetmatrix fest.</span><span class="sxs-lookup"><span data-stu-id="34334-104">Sets the bone offset matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="34334-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="34334-105">Syntax</span></span>


```C++
HRESULT SetBoneOffsetMatrix(
  [in]       DWORD      Bone,
  [in] const D3DXMATRIX *pBoneTransform
);
```



## <a name="parameters"></a><span data-ttu-id="34334-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="34334-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34334-107">*Knochen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34334-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34334-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34334-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34334-109">Die Knochen Nummer.</span><span class="sxs-lookup"><span data-stu-id="34334-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="34334-110">*pbonetransform* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34334-110">*pBoneTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34334-111">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="34334-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="34334-112">Ein Zeiger auf die-markveroffset-Matrix.</span><span class="sxs-lookup"><span data-stu-id="34334-112">Pointer to the bone offset matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34334-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34334-113">Return value</span></span>

<span data-ttu-id="34334-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="34334-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="34334-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="34334-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="34334-116">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="34334-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="34334-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34334-117">Remarks</span></span>

<span data-ttu-id="34334-118">Die Feldnamen werden von [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="34334-118">Bone names are returned by [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="34334-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34334-119">Requirements</span></span>



| <span data-ttu-id="34334-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34334-120">Requirement</span></span> | <span data-ttu-id="34334-121">Wert</span><span class="sxs-lookup"><span data-stu-id="34334-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="34334-122">Header</span><span class="sxs-lookup"><span data-stu-id="34334-122">Header</span></span><br/>  | <dl> <span data-ttu-id="34334-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="34334-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="34334-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="34334-124">Library</span></span><br/> | <dl> <span data-ttu-id="34334-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34334-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="34334-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34334-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34334-127">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="34334-127">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="34334-128">**ID3DXSkinInfo:: getboneoffsetmatrix**</span><span class="sxs-lookup"><span data-stu-id="34334-128">**ID3DXSkinInfo::GetBoneOffsetMatrix**</span></span>](id3dxskininfo--getboneoffsetmatrix.md)
</dt> </dl>

 

 
