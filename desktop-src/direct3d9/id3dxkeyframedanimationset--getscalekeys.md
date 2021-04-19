---
description: Füllt ein Array mit Skalierungs Schlüsseldaten, die für die Keyframe-Animation verwendet werden.
ms.assetid: 0d595510-6d8c-4bc9-b5ca-0d6f73be3439
title: 'ID3DXKeyframedAnimationSet:: getscalekeys-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 88c907bc9b45b1203917b092f565096be3ed1fb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350728"
---
# <a name="id3dxkeyframedanimationsetgetscalekeys-method"></a><span data-ttu-id="a6e0d-103">ID3DXKeyframedAnimationSet:: getscalekeys-Methode</span><span class="sxs-lookup"><span data-stu-id="a6e0d-103">ID3DXKeyframedAnimationSet::GetScaleKeys method</span></span>

<span data-ttu-id="a6e0d-104">Füllt ein Array mit Skalierungs Schlüsseldaten, die für die Keyframe-Animation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6e0d-104">Fills an array with scale key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6e0d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6e0d-105">Syntax</span></span>


```C++
HRESULT GetScaleKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a><span data-ttu-id="a6e0d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6e0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6e0d-107">*Animation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6e0d-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6e0d-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a6e0d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a6e0d-109">Animations Index.</span><span class="sxs-lookup"><span data-stu-id="a6e0d-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="a6e0d-110">*pscalekeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6e0d-110">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6e0d-111">Typ: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="a6e0d-111">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="a6e0d-112">Zeiger auf ein vom Benutzer zugeordneter Array von [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) Vektoren, das von der Methode mit Animations Skalierungs Daten ausgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a6e0d-112">Pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method is to fill with animation scale data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6e0d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6e0d-113">Return value</span></span>

<span data-ttu-id="a6e0d-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a6e0d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a6e0d-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a6e0d-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a6e0d-116">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="a6e0d-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6e0d-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6e0d-117">Requirements</span></span>



| <span data-ttu-id="a6e0d-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6e0d-118">Requirement</span></span> | <span data-ttu-id="a6e0d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a6e0d-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6e0d-120">Header</span><span class="sxs-lookup"><span data-stu-id="a6e0d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a6e0d-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6e0d-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a6e0d-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a6e0d-122">Library</span></span><br/> | <dl> <span data-ttu-id="a6e0d-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6e0d-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a6e0d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6e0d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6e0d-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="a6e0d-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="a6e0d-126">**ID3DXKeyframedAnimationSet:: getnumscalekeys**</span><span class="sxs-lookup"><span data-stu-id="a6e0d-126">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span></span>](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> </dl>

 

 
