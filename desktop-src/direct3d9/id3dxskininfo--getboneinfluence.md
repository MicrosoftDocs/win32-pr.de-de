---
description: Ruft die Scheitel Punkte und Gewichtungen ab, die ein Knochen beeinflusst.
ms.assetid: 84cb064b-b6b2-402d-81cc-8c02de6f8b52
title: 'ID3DXSkinInfo:: getboneingefluence-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b4b31ab08aca476ced1cb28dfc5ed5bfe61d044
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350654"
---
# <a name="id3dxskininfogetboneinfluence-method"></a><span data-ttu-id="31277-103">ID3DXSkinInfo:: getboneingefluence-Methode</span><span class="sxs-lookup"><span data-stu-id="31277-103">ID3DXSkinInfo::GetBoneInfluence method</span></span>

<span data-ttu-id="31277-104">Ruft die Scheitel Punkte und Gewichtungen ab, die ein Knochen beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="31277-104">Gets the vertices and weights that a bone influences.</span></span>

## <a name="syntax"></a><span data-ttu-id="31277-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="31277-105">Syntax</span></span>


```C++
HRESULT GetBoneInfluence(
  [in]      DWORD Bone,
  [in, out] DWORD *vertices,
  [in, out] FLOAT *weights
);
```



## <a name="parameters"></a><span data-ttu-id="31277-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="31277-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31277-107">*Knochen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31277-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31277-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31277-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31277-109">Die Knochen Nummer.</span><span class="sxs-lookup"><span data-stu-id="31277-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="31277-110">*Vertices* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="31277-110">*vertices* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="31277-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="31277-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="31277-112">Das Array der Scheitel Punkte, die von einem Knochen beeinflusst werden.</span><span class="sxs-lookup"><span data-stu-id="31277-112">Get the array of vertices influenced by a bone.</span></span>

</dd> <dt>

<span data-ttu-id="31277-113">*Gewichtungen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="31277-113">*weights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="31277-114">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="31277-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="31277-115">Das Array der Gewichtungen, die von einem Knochen beeinflusst werden.</span><span class="sxs-lookup"><span data-stu-id="31277-115">Get the array of weights influenced by a bone.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31277-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31277-116">Return value</span></span>

<span data-ttu-id="31277-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="31277-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="31277-118">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="31277-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="31277-119">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="31277-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="31277-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31277-120">Remarks</span></span>

<span data-ttu-id="31277-121">Verwenden Sie [**ID3DXSkinInfo:: getnumboneingefluences**](id3dxskininfo--getnumboneinfluences.md) , um herauszufinden, wie viele Scheitel Punkte der Knochen Einfluss hat.</span><span class="sxs-lookup"><span data-stu-id="31277-121">Use [**ID3DXSkinInfo::GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md) to find out how many vertices the bone influences.</span></span>

## <a name="requirements"></a><span data-ttu-id="31277-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31277-122">Requirements</span></span>



| <span data-ttu-id="31277-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31277-123">Requirement</span></span> | <span data-ttu-id="31277-124">Wert</span><span class="sxs-lookup"><span data-stu-id="31277-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31277-125">Header</span><span class="sxs-lookup"><span data-stu-id="31277-125">Header</span></span><br/>  | <dl> <span data-ttu-id="31277-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="31277-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="31277-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="31277-127">Library</span></span><br/> | <dl> <span data-ttu-id="31277-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31277-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="31277-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31277-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31277-130">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="31277-130">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="31277-131">**ID3DXSkinInfo:: setboneingefluence**</span><span class="sxs-lookup"><span data-stu-id="31277-131">**ID3DXSkinInfo::SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
