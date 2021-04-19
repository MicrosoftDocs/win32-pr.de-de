---
description: Sie erhalten Übersetzungs Informationen für einen bestimmten Keyframe im Animations Satz.
ms.assetid: 757af408-8a9c-4294-9343-91f52d4cc1ab
title: 'ID3DXKeyframedAnimationSet:: gettranslationkey-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f61d1caecb46477d16be4367588ab5609bfd6224
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367486"
---
# <a name="id3dxkeyframedanimationsetgettranslationkey-method"></a><span data-ttu-id="e29b9-103">ID3DXKeyframedAnimationSet:: gettranslationkey-Methode</span><span class="sxs-lookup"><span data-stu-id="e29b9-103">ID3DXKeyframedAnimationSet::GetTranslationKey method</span></span>

<span data-ttu-id="e29b9-104">Sie erhalten Übersetzungs Informationen für einen bestimmten Keyframe im Animations Satz.</span><span class="sxs-lookup"><span data-stu-id="e29b9-104">Get translation information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="e29b9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e29b9-105">Syntax</span></span>


```C++
HRESULT GetTranslationKey(
  [in]  UINT              Animation,
  [in]  UINT              Key,
  [out] LPD3DXKEY_VECTOR3 pTranslationKey
);
```



## <a name="parameters"></a><span data-ttu-id="e29b9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e29b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e29b9-107">*Animation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e29b9-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e29b9-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e29b9-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e29b9-109">Animations Index.</span><span class="sxs-lookup"><span data-stu-id="e29b9-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="e29b9-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e29b9-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e29b9-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e29b9-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e29b9-112">Keyframe.</span><span class="sxs-lookup"><span data-stu-id="e29b9-112">Key Frame.</span></span>

</dd> <dt>

<span data-ttu-id="e29b9-113">*ptranslationkey* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e29b9-113">*pTranslationKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e29b9-114">Typ: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="e29b9-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="e29b9-115">Zeiger auf die Rotations Informationen.</span><span class="sxs-lookup"><span data-stu-id="e29b9-115">Pointer to the rotation information.</span></span> <span data-ttu-id="e29b9-116">Siehe [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="e29b9-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e29b9-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e29b9-117">Return value</span></span>

<span data-ttu-id="e29b9-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e29b9-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e29b9-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e29b9-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e29b9-120">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="e29b9-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e29b9-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e29b9-121">Requirements</span></span>



| <span data-ttu-id="e29b9-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e29b9-122">Requirement</span></span> | <span data-ttu-id="e29b9-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e29b9-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e29b9-124">Header</span><span class="sxs-lookup"><span data-stu-id="e29b9-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e29b9-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e29b9-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e29b9-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e29b9-126">Library</span></span><br/> | <dl> <span data-ttu-id="e29b9-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e29b9-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e29b9-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e29b9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e29b9-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="e29b9-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
