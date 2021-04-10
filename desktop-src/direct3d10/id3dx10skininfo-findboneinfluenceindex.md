---
description: Suchen Sie nach dem Index, der angibt, wo sich ein bestimmter Scheitelpunkt in der Liste der beeinflussten Scheitel Punkte eines bestimmten Knotens befindet.
ms.assetid: vs|directx_sdk|~\id3dx10skininfo_findboneinfluenceindex.htm
title: 'ID3DX10SkinInfo:: findboneinfludenceindex-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.FindBoneInfluenceIndex
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1468fed3c0cf999e7635ba0f5ae53cee72fe70c6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219607"
---
# <a name="id3dx10skininfofindboneinfluenceindex-method"></a><span data-ttu-id="f45cd-103">ID3DX10SkinInfo:: findboneinfludenceindex-Methode</span><span class="sxs-lookup"><span data-stu-id="f45cd-103">ID3DX10SkinInfo::FindBoneInfluenceIndex method</span></span>

<span data-ttu-id="f45cd-104">Suchen Sie nach dem Index, der angibt, wo sich ein bestimmter Scheitelpunkt in der Liste der beeinflussten Scheitel Punkte eines bestimmten Knotens befindet.</span><span class="sxs-lookup"><span data-stu-id="f45cd-104">Find the index that indicates where a given vertex is in a given bone's list of influenced vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="f45cd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f45cd-105">Syntax</span></span>


```C++
HRESULT FindBoneInfluenceIndex(
  [in] UINT BoneIndex,
  [in] UINT VertexIndex,
  [in] UINT *pInfluenceIndex
);
```



## <a name="parameters"></a><span data-ttu-id="f45cd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f45cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f45cd-107">*Boneingedex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f45cd-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f45cd-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f45cd-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f45cd-109">Ein Index, der einen vorhandenen Knochen Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="f45cd-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="f45cd-110">Muss zwischen 0 und dem von [**ID3DX10SkinInfo:: getnumbones**](id3dx10skininfo-getnumbones.md)zurückgegebenen Wert liegen.</span><span class="sxs-lookup"><span data-stu-id="f45cd-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="f45cd-111">*Vertexindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f45cd-111">*VertexIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f45cd-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f45cd-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f45cd-113">Der Index des Scheitel Punkts im Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="f45cd-113">The index of the vertex in the vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f45cd-114">*pinfluendceindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f45cd-114">*pInfluenceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f45cd-115">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f45cd-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f45cd-116">Der Index des Scheitel Punkts in der Liste der von ihm beeinflussten Vertices in der Liste.</span><span class="sxs-lookup"><span data-stu-id="f45cd-116">The index of the vertex in the bone's list of influenced vertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f45cd-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f45cd-117">Return value</span></span>

<span data-ttu-id="f45cd-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f45cd-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f45cd-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f45cd-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f45cd-120">Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: E \_ invalidArg.</span><span class="sxs-lookup"><span data-stu-id="f45cd-120">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="f45cd-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f45cd-121">Requirements</span></span>



| <span data-ttu-id="f45cd-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f45cd-122">Requirement</span></span> | <span data-ttu-id="f45cd-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f45cd-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f45cd-124">Header</span><span class="sxs-lookup"><span data-stu-id="f45cd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f45cd-125"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f45cd-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f45cd-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f45cd-126">Library</span></span><br/> | <dl> <span data-ttu-id="f45cd-127"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f45cd-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f45cd-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f45cd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f45cd-129">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="f45cd-129">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="f45cd-130">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f45cd-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
