---
description: Legen Sie den Umfang der Auswirkung fest, den ein bestimmter Knochen über einem bestimmten Scheitelpunkt hat.
ms.assetid: adbdc784-c6b4-4e10-85c8-5e0b794d946f
title: 'ID3DX10SkinInfo:: setboneingefluence-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d136ddf4491a2a00c029422512c671a5439ba47c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355215"
---
# <a name="id3dx10skininfosetboneinfluence-method"></a><span data-ttu-id="b7c47-103">ID3DX10SkinInfo:: setboneingefluence-Methode</span><span class="sxs-lookup"><span data-stu-id="b7c47-103">ID3DX10SkinInfo::SetBoneInfluence method</span></span>

<span data-ttu-id="b7c47-104">Legen Sie den Umfang der Auswirkung fest, den ein bestimmter Knochen über einem bestimmten Scheitelpunkt hat.</span><span class="sxs-lookup"><span data-stu-id="b7c47-104">Set the amount of influence a given bone has over a given vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7c47-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7c47-105">Syntax</span></span>


```C++
HRESULT SetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float Weight
);
```



## <a name="parameters"></a><span data-ttu-id="b7c47-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7c47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7c47-107">*Boneingedex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7c47-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7c47-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7c47-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7c47-109">Ein Index, der einen vorhandenen Knochen Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="b7c47-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="b7c47-110">Muss zwischen 0 und dem von [**ID3DX10SkinInfo:: getnumbones**](id3dx10skininfo-getnumbones.md)zurückgegebenen Wert liegen.</span><span class="sxs-lookup"><span data-stu-id="b7c47-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7c47-111">*Einflussfaktor ceindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7c47-111">*InfluenceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7c47-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7c47-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7c47-113">Ein Index in der Liste der in der Liste der von ihm Einfluss enden Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="b7c47-113">An index into the bone's list of vertices that it influences.</span></span>

</dd> <dt>

<span data-ttu-id="b7c47-114">*Gewichtung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7c47-114">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7c47-115">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="b7c47-115">Type: **float**</span></span>

<span data-ttu-id="b7c47-116">Die Menge der Auswirkung zwischen 0 und 1, die der Knochen über dem Scheitelpunkt hat.</span><span class="sxs-lookup"><span data-stu-id="b7c47-116">The amount of influence, between 0 and 1, that the bone has over the vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7c47-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7c47-117">Return value</span></span>

<span data-ttu-id="b7c47-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b7c47-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b7c47-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b7c47-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b7c47-120">Wenn die Methode fehlschlägt, kann der Rückgabewert E \_ invalidArg lauten.</span><span class="sxs-lookup"><span data-stu-id="b7c47-120">If the method fails, the return value can be E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7c47-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7c47-121">Requirements</span></span>



| <span data-ttu-id="b7c47-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7c47-122">Requirement</span></span> | <span data-ttu-id="b7c47-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b7c47-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7c47-124">Header</span><span class="sxs-lookup"><span data-stu-id="b7c47-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b7c47-125"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7c47-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7c47-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b7c47-126">Library</span></span><br/> | <dl> <span data-ttu-id="b7c47-127"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7c47-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7c47-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7c47-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7c47-129">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="b7c47-129">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="b7c47-130">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b7c47-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
