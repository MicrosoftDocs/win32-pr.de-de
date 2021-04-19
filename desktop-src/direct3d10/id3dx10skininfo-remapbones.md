---
description: Ändern Sie, welche Knochen welche Scheitel Punkte beeinflussen.
ms.assetid: 0955e0ba-ffc5-408b-ab38-2abd39e1c429
title: 'ID3DX10SkinInfo:: remapbones-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapBones
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 238e4628740fa74e055312c82de2635316f5bde5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350690"
---
# <a name="id3dx10skininforemapbones-method"></a><span data-ttu-id="3235f-103">ID3DX10SkinInfo:: remapbones-Methode</span><span class="sxs-lookup"><span data-stu-id="3235f-103">ID3DX10SkinInfo::RemapBones method</span></span>

<span data-ttu-id="3235f-104">Ändern Sie, welche Knochen welche Scheitel Punkte beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="3235f-104">Change which bones influence which vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="3235f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3235f-105">Syntax</span></span>


```C++
HRESULT RemapBones(
  [in] UINT NewBoneCount,
  [in] UINT *pBoneRemap
);
```



## <a name="parameters"></a><span data-ttu-id="3235f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3235f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3235f-107">*Newbonecount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3235f-107">*NewBoneCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3235f-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3235f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3235f-109">Die neue Anzahl von Knochen.</span><span class="sxs-lookup"><span data-stu-id="3235f-109">The new number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="3235f-110">*pboneremap* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3235f-110">*pBoneRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3235f-111">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3235f-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3235f-112">Ein Zeiger auf ein Array von Bone-Indizes, die die Neuzuordnung beschreiben.</span><span class="sxs-lookup"><span data-stu-id="3235f-112">A pointer to an array of bone indices, which describe the remapping.</span></span> <span data-ttu-id="3235f-113">Beispiel: "skininfo" enthält einige Gedanken, dass "bone0" von "v0", "bone1" und "bone2" zu "V2" und "Array mit 2, 1, 0" für "pboneremap" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3235f-113">For example, say SkinInfo contains some bones such that bone0 is mapped to v0, bone1 to v1, and bone2 to v2, and array with 2,1,0 is specified for pBoneRemap.</span></span> <span data-ttu-id="3235f-114">Dies bewirkt, dass bone0 v2, bone1 zu v1 und bone2 zu v0 zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="3235f-114">This will cause bone0 to be mapped to v2, bone1 to v1, and bone2 to v0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3235f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3235f-115">Return value</span></span>

<span data-ttu-id="3235f-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3235f-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3235f-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3235f-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3235f-118">Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: e \_ outo-Memory oder e \_ invalidArg.</span><span class="sxs-lookup"><span data-stu-id="3235f-118">If the method fails, the return value can be: E\_OUTOFMEMORY or E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="3235f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3235f-119">Requirements</span></span>



| <span data-ttu-id="3235f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3235f-120">Requirement</span></span> | <span data-ttu-id="3235f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="3235f-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3235f-122">Header</span><span class="sxs-lookup"><span data-stu-id="3235f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3235f-123"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="3235f-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3235f-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3235f-124">Library</span></span><br/> | <dl> <span data-ttu-id="3235f-125"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3235f-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3235f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3235f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3235f-127">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="3235f-127">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="3235f-128">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="3235f-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
