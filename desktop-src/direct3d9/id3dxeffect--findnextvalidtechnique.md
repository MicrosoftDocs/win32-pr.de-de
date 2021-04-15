---
description: Sucht das nächste gültige Verfahren, beginnend bei der Technik nach der angegebenen Technik.
ms.assetid: 0d2f3f80-90fd-495d-acb8-075f50e9a974
title: 'ID3DXEffect:: findnextvalidtechnique-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.FindNextValidTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: adcaaa5194abeb17d110118de922811eb84af7fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394145"
---
# <a name="id3dxeffectfindnextvalidtechnique-method"></a><span data-ttu-id="429fa-103">ID3DXEffect:: findnextvalidtechnique-Methode</span><span class="sxs-lookup"><span data-stu-id="429fa-103">ID3DXEffect::FindNextValidTechnique method</span></span>

<span data-ttu-id="429fa-104">Sucht das nächste gültige Verfahren, beginnend bei der Technik nach der angegebenen Technik.</span><span class="sxs-lookup"><span data-stu-id="429fa-104">Searches for the next valid technique, starting at the technique after the specified technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="429fa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="429fa-105">Syntax</span></span>


```C++
HRESULT FindNextValidTechnique(
  [in]  D3DXHANDLE hTechnique,
  [out] D3DXHANDLE *pTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="429fa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="429fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="429fa-107">*htechnik* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="429fa-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="429fa-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="429fa-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="429fa-109">Eindeutiger Bezeichner für eine Technik.</span><span class="sxs-lookup"><span data-stu-id="429fa-109">Unique identifier to a technique.</span></span> <span data-ttu-id="429fa-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="429fa-110">See [Handles (Direct3D 9)](handles.md).</span></span> <span data-ttu-id="429fa-111">Geben Sie **null** für diesen Parameter an, um das erste gültige Verfahren zu suchen.</span><span class="sxs-lookup"><span data-stu-id="429fa-111">Specify **NULL** for this parameter to find the first valid technique.</span></span>

</dd> <dt>

<span data-ttu-id="429fa-112">*ptechnique* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="429fa-112">*pTechnique* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="429fa-113">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***</span><span class="sxs-lookup"><span data-stu-id="429fa-113">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***</span></span>

<span data-ttu-id="429fa-114">Zeiger auf einen Bezeichner für die nächste Technik.</span><span class="sxs-lookup"><span data-stu-id="429fa-114">Pointer to an identifier for the next technique.</span></span> <span data-ttu-id="429fa-115">**Null** wird zurückgegeben, wenn dies die letzte Methode ist.</span><span class="sxs-lookup"><span data-stu-id="429fa-115">**NULL** is returned if this is the last technique.</span></span> <span data-ttu-id="429fa-116">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="429fa-116">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="429fa-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="429fa-117">Return value</span></span>

<span data-ttu-id="429fa-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="429fa-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="429fa-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="429fa-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="429fa-120">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="429fa-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="429fa-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="429fa-121">Requirements</span></span>



| <span data-ttu-id="429fa-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="429fa-122">Requirement</span></span> | <span data-ttu-id="429fa-123">Wert</span><span class="sxs-lookup"><span data-stu-id="429fa-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="429fa-124">Header</span><span class="sxs-lookup"><span data-stu-id="429fa-124">Header</span></span><br/>  | <dl> <span data-ttu-id="429fa-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="429fa-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="429fa-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="429fa-126">Library</span></span><br/> | <dl> <span data-ttu-id="429fa-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="429fa-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="429fa-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="429fa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="429fa-129">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="429fa-129">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="429fa-130">**D3DXTECHNIQUE- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="429fa-130">**D3DXTECHNIQUE\_DESC**</span></span>](d3dxtechnique-desc.md)
</dt> <dt>

[<span data-ttu-id="429fa-131">**ID3DXEffect:: validatetechnique**</span><span class="sxs-lookup"><span data-stu-id="429fa-131">**ID3DXEffect::ValidateTechnique**</span></span>](id3dxeffect--validatetechnique.md)
</dt> </dl>

 

 




