---
description: Füllt ein Array mit rotierenden Schlüsseldaten, die für die Keyframe-Animation verwendet werden.
ms.assetid: 9ae8bc28-d231-4d50-98f0-762b2d2c04e8
title: 'ID3DXKeyframedAnimationSet:: getrotationkeys-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetRotationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af9242ccf75bc1e5443f040399ffbd8a939ed92e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762309"
---
# <a name="id3dxkeyframedanimationsetgetrotationkeys-method"></a><span data-ttu-id="e2402-103">ID3DXKeyframedAnimationSet:: getrotationkeys-Methode</span><span class="sxs-lookup"><span data-stu-id="e2402-103">ID3DXKeyframedAnimationSet::GetRotationKeys method</span></span>

<span data-ttu-id="e2402-104">Füllt ein Array mit rotierenden Schlüsseldaten, die für die Keyframe-Animation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e2402-104">Fills an array with rotational key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2402-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2402-105">Syntax</span></span>


```C++
HRESULT GetRotationKeys(
  [in] UINT                 Animation,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="e2402-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2402-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2402-107">*Animation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2402-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2402-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2402-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e2402-109">Animations Index.</span><span class="sxs-lookup"><span data-stu-id="e2402-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="e2402-110">" *protationkeys* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="e2402-110">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2402-111">Typ: **[ **LPD3DXKEY \_ Quaternion**](d3dxkey-quaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="e2402-111">Type: **[**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)**</span></span>

<span data-ttu-id="e2402-112">Zeiger auf ein vom Benutzer zugewiesenes Array von [**D3DXKEY \_ Quaternion**](d3dxkey-quaternion.md) Quaternionen, das die Methode mit Animations Rotationsdaten ausfüllen soll.</span><span class="sxs-lookup"><span data-stu-id="e2402-112">Pointer to a user-allocated array of [**D3DXKEY\_QUATERNION**](d3dxkey-quaternion.md) quaternions that the method is to fill with animation rotation data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2402-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2402-113">Return value</span></span>

<span data-ttu-id="e2402-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e2402-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e2402-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e2402-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e2402-116">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="e2402-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2402-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2402-117">Requirements</span></span>



| <span data-ttu-id="e2402-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2402-118">Requirement</span></span> | <span data-ttu-id="e2402-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e2402-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2402-120">Header</span><span class="sxs-lookup"><span data-stu-id="e2402-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e2402-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2402-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e2402-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e2402-122">Library</span></span><br/> | <dl> <span data-ttu-id="e2402-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2402-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e2402-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2402-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2402-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="e2402-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="e2402-126">**ID3DXKeyframedAnimationSet:: getnumrotationkeys**</span><span class="sxs-lookup"><span data-stu-id="e2402-126">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> </dl>

 

 
