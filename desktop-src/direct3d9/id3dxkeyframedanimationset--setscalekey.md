---
description: Legen Sie Skalierungsinformationen für einen bestimmten Keyframe im Animations Satz fest.
ms.assetid: b606e5d3-11c9-4997-ad3c-d3ae21c32e10
title: 'ID3DXKeyframedAnimationSet:: setscalekey-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 12ac4d46a2719e452d44d2da67f178e6146b799b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355229"
---
# <a name="id3dxkeyframedanimationsetsetscalekey-method"></a><span data-ttu-id="fa3f4-103">ID3DXKeyframedAnimationSet:: setscalekey-Methode</span><span class="sxs-lookup"><span data-stu-id="fa3f4-103">ID3DXKeyframedAnimationSet::SetScaleKey method</span></span>

<span data-ttu-id="fa3f4-104">Legen Sie Skalierungsinformationen für einen bestimmten Keyframe im Animations Satz fest.</span><span class="sxs-lookup"><span data-stu-id="fa3f4-104">Set scale information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa3f4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa3f4-105">Syntax</span></span>


```C++
HRESULT SetScaleKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a><span data-ttu-id="fa3f4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa3f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa3f4-107">*Animation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa3f4-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa3f4-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fa3f4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fa3f4-109">Animations Index.</span><span class="sxs-lookup"><span data-stu-id="fa3f4-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="fa3f4-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa3f4-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa3f4-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fa3f4-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fa3f4-112">Keyframe.</span><span class="sxs-lookup"><span data-stu-id="fa3f4-112">Key frame.</span></span>

</dd> <dt>

<span data-ttu-id="fa3f4-113">*pscalekeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa3f4-113">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa3f4-114">Typ: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="fa3f4-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="fa3f4-115">Zeiger auf die Skalierungs Daten.</span><span class="sxs-lookup"><span data-stu-id="fa3f4-115">Pointer to the scale data.</span></span> <span data-ttu-id="fa3f4-116">Siehe [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="fa3f4-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa3f4-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa3f4-117">Return value</span></span>

<span data-ttu-id="fa3f4-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fa3f4-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fa3f4-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fa3f4-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="fa3f4-120">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="fa3f4-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa3f4-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa3f4-121">Requirements</span></span>



| <span data-ttu-id="fa3f4-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa3f4-122">Requirement</span></span> | <span data-ttu-id="fa3f4-123">Wert</span><span class="sxs-lookup"><span data-stu-id="fa3f4-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa3f4-124">Header</span><span class="sxs-lookup"><span data-stu-id="fa3f4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fa3f4-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa3f4-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="fa3f4-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fa3f4-126">Library</span></span><br/> | <dl> <span data-ttu-id="fa3f4-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa3f4-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fa3f4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa3f4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa3f4-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="fa3f4-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
