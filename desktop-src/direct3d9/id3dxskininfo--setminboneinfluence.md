---
description: Legt den minimalen Knochen Einfluss fest. Werte, die kleiner als dieser Wert sind, werden ignoriert.
ms.assetid: 9af19c9e-bb6e-4f93-973f-5c38f88eea3d
title: 'ID3DXSkinInfo:: setminboneingefluence-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetMinBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03e3aeeed31a58231644784ba5070bc9422f7820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354973"
---
# <a name="id3dxskininfosetminboneinfluence-method"></a><span data-ttu-id="e7129-104">ID3DXSkinInfo:: setminboneingefluence-Methode</span><span class="sxs-lookup"><span data-stu-id="e7129-104">ID3DXSkinInfo::SetMinBoneInfluence method</span></span>

<span data-ttu-id="e7129-105">Legt den minimalen Knochen Einfluss fest.</span><span class="sxs-lookup"><span data-stu-id="e7129-105">Sets the minimum bone influence.</span></span> <span data-ttu-id="e7129-106">Werte, die kleiner als dieser Wert sind, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e7129-106">Influence values smaller than this are ignored.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7129-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7129-107">Syntax</span></span>


```C++
HRESULT SetMinBoneInfluence(
  [in] FLOAT MinInfl
);
```



## <a name="parameters"></a><span data-ttu-id="e7129-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7129-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7129-109">*Mininfl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7129-109">*MinInfl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7129-110">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7129-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7129-111">Minimaler Einfluss Wert.</span><span class="sxs-lookup"><span data-stu-id="e7129-111">Minimum influence value.</span></span> <span data-ttu-id="e7129-112">Werte, die kleiner als dieser Wert sind, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e7129-112">Influence values smaller than this are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7129-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7129-113">Return value</span></span>

<span data-ttu-id="e7129-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e7129-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e7129-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e7129-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e7129-116">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="e7129-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7129-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7129-117">Requirements</span></span>



| <span data-ttu-id="e7129-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7129-118">Requirement</span></span> | <span data-ttu-id="e7129-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e7129-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7129-120">Header</span><span class="sxs-lookup"><span data-stu-id="e7129-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e7129-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7129-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e7129-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e7129-122">Library</span></span><br/> | <dl> <span data-ttu-id="e7129-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7129-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e7129-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7129-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7129-125">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="e7129-125">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="e7129-126">**ID3DXSkinInfo:: getminboneingefluence**</span><span class="sxs-lookup"><span data-stu-id="e7129-126">**ID3DXSkinInfo::GetMinBoneInfluence**</span></span>](id3dxskininfo--getminboneinfluence.md)
</dt> </dl>

 

 
