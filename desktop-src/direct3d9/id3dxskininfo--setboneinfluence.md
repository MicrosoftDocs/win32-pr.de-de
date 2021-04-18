---
description: Legt den Wert für den Einfluss für einen Knochen Wert fest.
ms.assetid: c6dc8a33-8f5c-47d0-8637-a2492b1e3089
title: 'ID3DXSkinInfo:: setboneingefluence-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16ed3514c986dee89f964074d18a646bcf3a1249
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354975"
---
# <a name="id3dxskininfosetboneinfluence-method"></a><span data-ttu-id="7d3b0-103">ID3DXSkinInfo:: setboneingefluence-Methode</span><span class="sxs-lookup"><span data-stu-id="7d3b0-103">ID3DXSkinInfo::SetBoneInfluence method</span></span>

<span data-ttu-id="7d3b0-104">Legt den Wert für den Einfluss für einen Knochen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="7d3b0-104">Sets the influence value for a bone.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d3b0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d3b0-105">Syntax</span></span>


```C++
HRESULT SetBoneInfluence(
  [in]       DWORD Bone,
  [in]       DWORD numInfluences,
  [in] const DWORD *vertices,
  [in] const FLOAT *weights
);
```



## <a name="parameters"></a><span data-ttu-id="7d3b0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d3b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d3b0-107">*Knochen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d3b0-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d3b0-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7d3b0-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7d3b0-109">Die Knochen Nummer.</span><span class="sxs-lookup"><span data-stu-id="7d3b0-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="7d3b0-110">*numeinflüsse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d3b0-110">*numInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d3b0-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7d3b0-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7d3b0-112">Anzahl der Einflüsse.</span><span class="sxs-lookup"><span data-stu-id="7d3b0-112">Number of influences.</span></span>

</dd> <dt>

<span data-ttu-id="7d3b0-113">*Vertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d3b0-113">*vertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d3b0-114">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="7d3b0-114">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7d3b0-115">Das Array der Scheitel Punkte, die von einem Knochen beeinflusst werden.</span><span class="sxs-lookup"><span data-stu-id="7d3b0-115">The array of vertices influenced by a bone.</span></span>

</dd> <dt>

<span data-ttu-id="7d3b0-116">*Gewichtungen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d3b0-116">*weights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d3b0-117">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="7d3b0-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7d3b0-118">Das Array von Gewichtungen, die von einem Knochen beeinflusst werden.</span><span class="sxs-lookup"><span data-stu-id="7d3b0-118">The array of weights influenced by a bone.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d3b0-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d3b0-119">Return value</span></span>

<span data-ttu-id="7d3b0-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7d3b0-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7d3b0-121">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7d3b0-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7d3b0-122">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="7d3b0-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d3b0-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d3b0-123">Requirements</span></span>



| <span data-ttu-id="7d3b0-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d3b0-124">Requirement</span></span> | <span data-ttu-id="7d3b0-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7d3b0-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d3b0-126">Header</span><span class="sxs-lookup"><span data-stu-id="7d3b0-126">Header</span></span><br/>  | <dl> <span data-ttu-id="7d3b0-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d3b0-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7d3b0-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7d3b0-128">Library</span></span><br/> | <dl> <span data-ttu-id="7d3b0-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d3b0-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7d3b0-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d3b0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d3b0-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="7d3b0-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="7d3b0-132">**ID3DXSkinInfo:: getboneingefluence**</span><span class="sxs-lookup"><span data-stu-id="7d3b0-132">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> <dt>

[<span data-ttu-id="7d3b0-133">**ID3DXSkinInfo:: getnumboneingefluences**</span><span class="sxs-lookup"><span data-stu-id="7d3b0-133">**ID3DXSkinInfo::GetNumBoneInfluences**</span></span>](id3dxskininfo--getnumboneinfluences.md)
</dt> </dl>

 

 
