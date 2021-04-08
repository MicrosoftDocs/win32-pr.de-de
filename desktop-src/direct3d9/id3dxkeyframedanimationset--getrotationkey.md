---
description: Sie erhalten die Rotations Informationen für einen bestimmten Keyframe im Animations Satz.
ms.assetid: d62b8d5e-328e-4227-b2e8-cb6e5ccc4b3f
title: 'ID3DXKeyframedAnimationSet:: getrotationkey-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetRotationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8f5bf30eaf261e4baa032ed1411b3d70bddc706c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762312"
---
# <a name="id3dxkeyframedanimationsetgetrotationkey-method"></a><span data-ttu-id="95695-103">ID3DXKeyframedAnimationSet:: getrotationkey-Methode</span><span class="sxs-lookup"><span data-stu-id="95695-103">ID3DXKeyframedAnimationSet::GetRotationKey method</span></span>

<span data-ttu-id="95695-104">Sie erhalten die Rotations Informationen für einen bestimmten Keyframe im Animations Satz.</span><span class="sxs-lookup"><span data-stu-id="95695-104">Get rotation information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="95695-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="95695-105">Syntax</span></span>


```C++
HRESULT GetRotationKey(
  [in] UINT                 Animation,
  [in] UINT                 Key,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="95695-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="95695-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95695-107">*Animation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95695-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95695-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95695-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95695-109">Animations Index.</span><span class="sxs-lookup"><span data-stu-id="95695-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="95695-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95695-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95695-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95695-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95695-112">Keyframe.</span><span class="sxs-lookup"><span data-stu-id="95695-112">Key frame.</span></span>

</dd> <dt>

<span data-ttu-id="95695-113">" *protationkeys* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="95695-113">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95695-114">Typ: **[ **LPD3DXKEY \_ Quaternion**](d3dxkey-quaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="95695-114">Type: **[**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)**</span></span>

<span data-ttu-id="95695-115">Zeiger auf die Rotationsdaten.</span><span class="sxs-lookup"><span data-stu-id="95695-115">Pointer to the rotation data.</span></span> <span data-ttu-id="95695-116">Siehe [**D3DXKEY \_ Quaternion**](d3dxkey-quaternion.md).</span><span class="sxs-lookup"><span data-stu-id="95695-116">See [**D3DXKEY\_QUATERNION**](d3dxkey-quaternion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95695-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95695-117">Return value</span></span>

<span data-ttu-id="95695-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95695-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95695-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="95695-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="95695-120">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="95695-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="95695-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95695-121">Requirements</span></span>



| <span data-ttu-id="95695-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95695-122">Requirement</span></span> | <span data-ttu-id="95695-123">Wert</span><span class="sxs-lookup"><span data-stu-id="95695-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95695-124">Header</span><span class="sxs-lookup"><span data-stu-id="95695-124">Header</span></span><br/>  | <dl> <span data-ttu-id="95695-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="95695-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="95695-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="95695-126">Library</span></span><br/> | <dl> <span data-ttu-id="95695-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95695-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="95695-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95695-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95695-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="95695-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
