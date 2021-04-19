---
description: Ruft den Feldnamen aus dem-MarkerIndex ab.
ms.assetid: f56faf41-c119-4cdd-bb8a-86fc99ff5893
title: 'ID3DXSkinInfo:: getbonename-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0566d423d277dc3f39f36f8c1fda297ec917eb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361176"
---
# <a name="id3dxskininfogetbonename-method"></a><span data-ttu-id="946a5-103">ID3DXSkinInfo:: getbonename-Methode</span><span class="sxs-lookup"><span data-stu-id="946a5-103">ID3DXSkinInfo::GetBoneName method</span></span>

<span data-ttu-id="946a5-104">Ruft den Feldnamen aus dem-MarkerIndex ab.</span><span class="sxs-lookup"><span data-stu-id="946a5-104">Gets the bone name, from the bone index.</span></span>

## <a name="syntax"></a><span data-ttu-id="946a5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="946a5-105">Syntax</span></span>


```C++
LPCSTR GetBoneName(
  [in] DWORD Bone
);
```



## <a name="parameters"></a><span data-ttu-id="946a5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="946a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="946a5-107">*Knochen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="946a5-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="946a5-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="946a5-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="946a5-109">Die Knochen Nummer.</span><span class="sxs-lookup"><span data-stu-id="946a5-109">Bone number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="946a5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="946a5-110">Return value</span></span>

<span data-ttu-id="946a5-111">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="946a5-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="946a5-112">Gibt den Feldnamen zurück.</span><span class="sxs-lookup"><span data-stu-id="946a5-112">Returns the bone name.</span></span> <span data-ttu-id="946a5-113">Diese Zeichenfolge nicht freigeben.</span><span class="sxs-lookup"><span data-stu-id="946a5-113">Do not free this string.</span></span>

## <a name="requirements"></a><span data-ttu-id="946a5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="946a5-114">Requirements</span></span>



| <span data-ttu-id="946a5-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="946a5-115">Requirement</span></span> | <span data-ttu-id="946a5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="946a5-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="946a5-117">Header</span><span class="sxs-lookup"><span data-stu-id="946a5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="946a5-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="946a5-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="946a5-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="946a5-119">Library</span></span><br/> | <dl> <span data-ttu-id="946a5-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="946a5-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="946a5-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="946a5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="946a5-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="946a5-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="946a5-123">**ID3DXSkinInfo:: setbonename**</span><span class="sxs-lookup"><span data-stu-id="946a5-123">**ID3DXSkinInfo::SetBoneName**</span></span>](id3dxskininfo--setbonename.md)
</dt> <dt>

[<span data-ttu-id="946a5-124">**ID3DXSkinInfo:: getnumbones**</span><span class="sxs-lookup"><span data-stu-id="946a5-124">**ID3DXSkinInfo::GetNumBones**</span></span>](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
