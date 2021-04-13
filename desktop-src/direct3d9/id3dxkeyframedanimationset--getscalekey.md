---
description: Skalierungsinformationen für einen bestimmten Keyframe im Animations Satz erhalten.
ms.assetid: 7f4a0bf3-2922-4fd7-bb85-b387d3e983a7
title: 'ID3DXKeyframedAnimationSet:: getscalekey-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58cbd432404fcd511140a7368999161f5e44f77f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355726"
---
# <a name="id3dxkeyframedanimationsetgetscalekey-method"></a><span data-ttu-id="dfa22-103">ID3DXKeyframedAnimationSet:: getscalekey-Methode</span><span class="sxs-lookup"><span data-stu-id="dfa22-103">ID3DXKeyframedAnimationSet::GetScaleKey method</span></span>

<span data-ttu-id="dfa22-104">Skalierungsinformationen für einen bestimmten Keyframe im Animations Satz erhalten.</span><span class="sxs-lookup"><span data-stu-id="dfa22-104">Get scale information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfa22-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfa22-105">Syntax</span></span>


```C++
HRESULT GetScaleKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a><span data-ttu-id="dfa22-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfa22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfa22-107">*Animation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfa22-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa22-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dfa22-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dfa22-109">Animations Index.</span><span class="sxs-lookup"><span data-stu-id="dfa22-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="dfa22-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfa22-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa22-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dfa22-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dfa22-112">Keyframe.</span><span class="sxs-lookup"><span data-stu-id="dfa22-112">Key frame.</span></span>

</dd> <dt>

<span data-ttu-id="dfa22-113">*pscalekeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfa22-113">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa22-114">Typ: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="dfa22-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="dfa22-115">Zeiger auf die Skalierungs Daten.</span><span class="sxs-lookup"><span data-stu-id="dfa22-115">Pointer to the scale data.</span></span> <span data-ttu-id="dfa22-116">Siehe [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="dfa22-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfa22-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dfa22-117">Return value</span></span>

<span data-ttu-id="dfa22-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dfa22-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dfa22-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dfa22-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="dfa22-120">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="dfa22-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfa22-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dfa22-121">Requirements</span></span>



| <span data-ttu-id="dfa22-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dfa22-122">Requirement</span></span> | <span data-ttu-id="dfa22-123">Wert</span><span class="sxs-lookup"><span data-stu-id="dfa22-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa22-124">Header</span><span class="sxs-lookup"><span data-stu-id="dfa22-124">Header</span></span><br/>  | <dl> <span data-ttu-id="dfa22-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfa22-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="dfa22-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dfa22-126">Library</span></span><br/> | <dl> <span data-ttu-id="dfa22-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dfa22-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dfa22-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfa22-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfa22-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="dfa22-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
