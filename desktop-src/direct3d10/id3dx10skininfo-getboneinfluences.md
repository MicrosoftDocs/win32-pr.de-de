---
description: Eine Liste der Scheitel Punkte, die von einem bestimmten Knochen beeinflusst werden, und eine Liste der Auswirkungen von Bone auf jeden Scheitelpunkt erhalten.
ms.assetid: d1dea694-874d-4f21-87a8-f6b013617544
title: 'ID3DX10SkinInfo:: getboneingefluences-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9aead6b1dd381011a922c5bfbc1874976a78417c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219708"
---
# <a name="id3dx10skininfogetboneinfluences-method"></a><span data-ttu-id="b439e-103">ID3DX10SkinInfo:: getboneingefluences-Methode</span><span class="sxs-lookup"><span data-stu-id="b439e-103">ID3DX10SkinInfo::GetBoneInfluences method</span></span>

<span data-ttu-id="b439e-104">Eine Liste der Scheitel Punkte, die von einem bestimmten Knochen beeinflusst werden, und eine Liste der Auswirkungen von Bone auf jeden Scheitelpunkt erhalten.</span><span class="sxs-lookup"><span data-stu-id="b439e-104">Get a list of vertices that a given bone influences and a list of the amount of influence that bone has on each vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="b439e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b439e-105">Syntax</span></span>


```C++
HRESULT GetBoneInfluences(
  [in]      UINT  BoneIndex,
  [in]      UINT  Offset,
  [in]      UINT  Count,
  [in, out] UINT  *pDestIndices,
  [in, out] float *pDestWeights
);
```



## <a name="parameters"></a><span data-ttu-id="b439e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b439e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b439e-107">*Boneingedex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b439e-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b439e-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b439e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b439e-109">Ein Index, der einen vorhandenen Knochen Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="b439e-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="b439e-110">Muss zwischen 0 und dem von [**ID3DX10SkinInfo:: getnumbones**](id3dx10skininfo-getnumbones.md)zurückgegebenen Wert liegen.</span><span class="sxs-lookup"><span data-stu-id="b439e-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="b439e-111">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b439e-111">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b439e-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b439e-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b439e-113">Ein Offset vom oberen Rand der Liste der von ihm beeinflussten Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="b439e-113">An offset from the top of the bone's list of influenced vertices.</span></span> <span data-ttu-id="b439e-114">Dieser Wert muss zwischen 0 und dem von [**ID3DX10SkinInfo:: getboneinfluscecount**](id3dx10skininfo-getboneinfluencecount.md)zurückgegebenen Wert liegen.</span><span class="sxs-lookup"><span data-stu-id="b439e-114">This must be between 0 and the value returned by [**ID3DX10SkinInfo::GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md).</span></span>

</dd> <dt>

<span data-ttu-id="b439e-115">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b439e-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b439e-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b439e-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b439e-117">Die Anzahl der Indizes und Gewichtungen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b439e-117">The number of indices and weights to retrieve.</span></span> <span data-ttu-id="b439e-118">Muss zwischen 0 und dem von ID3DX10SkinInfo:: getboneinfluscecount zurückgegebenen Wert liegen.</span><span class="sxs-lookup"><span data-stu-id="b439e-118">Must be between 0 and the value returned by ID3DX10SkinInfo::GetBoneInfluenceCount.</span></span>

</dd> <dt>

<span data-ttu-id="b439e-119">*pdestindices* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b439e-119">*pDestIndices* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b439e-120">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b439e-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b439e-121">Eine Liste von Indizes in den Scheitelpunkt Puffer, die jeweils einen Vertex darstellen, der durch den Knochen beeinflusst wird.</span><span class="sxs-lookup"><span data-stu-id="b439e-121">A list of indices into the vertex buffer, each one representing a vertex influenced by the bone.</span></span> <span data-ttu-id="b439e-122">Diese Werte entsprechen den Werten in "pdestgewichtungen", sodass "pdestindices \[ i" \] pdestgewichtungen \[ i entspricht \] .</span><span class="sxs-lookup"><span data-stu-id="b439e-122">These values correspond to the values in pDestWeights, such that pDestIndices\[i\] corresponds to pDestWeights\[i\].</span></span>

</dd> <dt>

<span data-ttu-id="b439e-123">*pdestgewichtungen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b439e-123">*pDestWeights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b439e-124">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="b439e-124">Type: **float\***</span></span>

<span data-ttu-id="b439e-125">Eine Liste der Auswirkungen, die der Knochen auf jedem Scheitelpunkt hat.</span><span class="sxs-lookup"><span data-stu-id="b439e-125">A list of the amount of influence the bone has on each vertex.</span></span> <span data-ttu-id="b439e-126">Diese Werte entsprechen den Werten in pdestindices, sodass pdestgewichtungen \[ ich \] pdestindices \[ i \] . f verwende.</span><span class="sxs-lookup"><span data-stu-id="b439e-126">These values correspond to the values in pDestIndices, such that pDestWeights\[i\] corresponds to pDestIndices\[i\].f</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b439e-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b439e-127">Return value</span></span>

<span data-ttu-id="b439e-128">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b439e-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b439e-129">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b439e-129">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b439e-130">Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: E \_ invalidArg oder e \_ oudef Memory.</span><span class="sxs-lookup"><span data-stu-id="b439e-130">If the method fails, the return value can be: E\_INVALIDARG or E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b439e-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b439e-131">Requirements</span></span>



| <span data-ttu-id="b439e-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b439e-132">Requirement</span></span> | <span data-ttu-id="b439e-133">Wert</span><span class="sxs-lookup"><span data-stu-id="b439e-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b439e-134">Header</span><span class="sxs-lookup"><span data-stu-id="b439e-134">Header</span></span><br/>  | <dl> <span data-ttu-id="b439e-135"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b439e-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b439e-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b439e-136">Library</span></span><br/> | <dl> <span data-ttu-id="b439e-137"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b439e-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b439e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b439e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b439e-139">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="b439e-139">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="b439e-140">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b439e-140">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
