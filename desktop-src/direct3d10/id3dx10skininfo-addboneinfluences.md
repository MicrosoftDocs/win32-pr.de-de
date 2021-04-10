---
description: Ermöglicht, dass ein vorhandener Arbeitsspeicher eine Gruppe von Scheitel Punkten beeinflusst und festlegt, wie viel Einfluss der Knochen auf jeden Scheitelpunkt hat.
ms.assetid: 37ba97a8-ba40-4700-b8b8-fa7cc9118307
title: 'ID3DX10SkinInfo:: addboneinfluences-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8531d70e301b0583309817ac23a36762cacf563f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219530"
---
# <a name="id3dx10skininfoaddboneinfluences-method"></a><span data-ttu-id="7985e-103">ID3DX10SkinInfo:: addboneinfluences-Methode</span><span class="sxs-lookup"><span data-stu-id="7985e-103">ID3DX10SkinInfo::AddBoneInfluences method</span></span>

<span data-ttu-id="7985e-104">Ermöglicht, dass ein vorhandener Arbeitsspeicher eine Gruppe von Scheitel Punkten beeinflusst und festlegt, wie viel Einfluss der Knochen auf jeden Scheitelpunkt hat.</span><span class="sxs-lookup"><span data-stu-id="7985e-104">Enable an existing bone to influence a group of vertices and define how much influence the bone has on each vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="7985e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7985e-105">Syntax</span></span>


```C++
HRESULT AddBoneInfluences(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceCount,
  [in] UINT  *pIndices,
  [in] float *pWeights
);
```



## <a name="parameters"></a><span data-ttu-id="7985e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7985e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7985e-107">*Boneingedex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7985e-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7985e-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7985e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7985e-109">Ein Index, der einen vorhandenen Knochen Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="7985e-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="7985e-110">Muss zwischen 0 und dem von [**ID3DX10SkinInfo:: getnumbones**](id3dx10skininfo-getnumbones.md)zurückgegebenen Wert liegen.</span><span class="sxs-lookup"><span data-stu-id="7985e-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="7985e-111">*Einfluss Zähler* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7985e-111">*InfluenceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7985e-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7985e-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7985e-113">Anzahl der Scheitel Punkte, die dem knochenwert hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7985e-113">Number of vertices to add to the bone's influence.</span></span>

</dd> <dt>

<span data-ttu-id="7985e-114">*PIndizes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7985e-114">*pIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7985e-115">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7985e-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7985e-116">Zeiger auf ein Array von Scheitelpunkt Indizes.</span><span class="sxs-lookup"><span data-stu-id="7985e-116">Pointer to an array of vertex indices.</span></span> <span data-ttu-id="7985e-117">Jedes Element dieses Arrays verfügt über einen entsprechenden Member in pgewichtungen, d. b., PIndizes \[ \] entsprechen den pgewichtungen \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="7985e-117">Each member of this array has a corresponding member in pWeights, such that pIndices\[i\] corresponds to pWeights\[i\].</span></span> <span data-ttu-id="7985e-118">Der entsprechende Wert in pgewichtungen \[ i legt fest, \] wie viel Einfluss boneindex auf den Scheitelpunkt hat, der von PIndizes i indiziert wird \[ \] .</span><span class="sxs-lookup"><span data-stu-id="7985e-118">The corresponding value in pWeights\[i\] determines how much influence BoneIndex will have on the vertex indexed by pIndices\[i\].</span></span> <span data-ttu-id="7985e-119">Die Größe des PIndizes-Arrays muss größer oder gleich "Einfluss Wert" sein.</span><span class="sxs-lookup"><span data-stu-id="7985e-119">The size of the pIndices array must be equal to or greater than InfluenceCount.</span></span>

</dd> <dt>

<span data-ttu-id="7985e-120">*pgewichtungen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7985e-120">*pWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7985e-121">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="7985e-121">Type: **float\***</span></span>

<span data-ttu-id="7985e-122">Zeiger auf ein Array von Knochen Gewichtungen.</span><span class="sxs-lookup"><span data-stu-id="7985e-122">Pointer to an array of bone weights.</span></span> <span data-ttu-id="7985e-123">Jedes Element dieses Arrays verfügt über einen entsprechenden Member in PIndizes, d. b., die pgewichtungen \[ \] entsprechen den PIndizes \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="7985e-123">Each member of this array has a corresponding member in pIndices, such that pWeights\[i\] corresponds to pIndices\[i\].</span></span> <span data-ttu-id="7985e-124">Jeder Wert in pgewichtungen liegt zwischen 0 und 1 und definiert den Umfang der Auswirkung, den der Knochen über jedem Scheitelpunkt hat.</span><span class="sxs-lookup"><span data-stu-id="7985e-124">Each value in pWeights is between 0 and 1 and defines the amount of influence the bone has over each vertex.</span></span> <span data-ttu-id="7985e-125">Die Größe der pgewichtungen muss gleich oder größer als Einfluss Wert sein.</span><span class="sxs-lookup"><span data-stu-id="7985e-125">The size of pWeights must be equal to or greater than InfluenceCount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7985e-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7985e-126">Return value</span></span>

<span data-ttu-id="7985e-127">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7985e-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7985e-128">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7985e-128">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7985e-129">Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: E \_ invalidArg oder e \_ oudef Memory.</span><span class="sxs-lookup"><span data-stu-id="7985e-129">If the method fails, the return value can be: E\_INVALIDARG or E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="7985e-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7985e-130">Requirements</span></span>



| <span data-ttu-id="7985e-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7985e-131">Requirement</span></span> | <span data-ttu-id="7985e-132">Wert</span><span class="sxs-lookup"><span data-stu-id="7985e-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7985e-133">Header</span><span class="sxs-lookup"><span data-stu-id="7985e-133">Header</span></span><br/>  | <dl> <span data-ttu-id="7985e-134"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="7985e-134"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="7985e-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7985e-135">Library</span></span><br/> | <dl> <span data-ttu-id="7985e-136"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7985e-136"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7985e-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7985e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7985e-138">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="7985e-138">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="7985e-139">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="7985e-139">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
