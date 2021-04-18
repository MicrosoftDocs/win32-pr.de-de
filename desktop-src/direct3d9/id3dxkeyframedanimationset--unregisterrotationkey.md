---
description: Entfernt die Rotationsdaten am angegebenen Keyframe.
ms.assetid: 8e95d684-fa22-4eba-a721-e7551e8f393b
title: 'ID3DXKeyframedAnimationSet:: unregisterrotationkey-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterRotationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 420a15d0086f94def7db8c7d558640d03b69562f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371943"
---
# <a name="id3dxkeyframedanimationsetunregisterrotationkey-method"></a><span data-ttu-id="4ee2e-103">ID3DXKeyframedAnimationSet:: unregisterrotationkey-Methode</span><span class="sxs-lookup"><span data-stu-id="4ee2e-103">ID3DXKeyframedAnimationSet::UnregisterRotationKey method</span></span>

<span data-ttu-id="4ee2e-104">Entfernt die Rotationsdaten am angegebenen Keyframe.</span><span class="sxs-lookup"><span data-stu-id="4ee2e-104">Removes the rotation data at the specified key frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ee2e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ee2e-105">Syntax</span></span>


```C++
HRESULT UnregisterRotationKey(
  [in] UINT Animation,
  [in] UINT Key
);
```



## <a name="parameters"></a><span data-ttu-id="4ee2e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ee2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ee2e-107">*Animation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ee2e-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ee2e-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ee2e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ee2e-109">Animations Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="4ee2e-109">Animation identifier.</span></span>

</dd> <dt>

<span data-ttu-id="4ee2e-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ee2e-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ee2e-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ee2e-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ee2e-112">Keyframe.</span><span class="sxs-lookup"><span data-stu-id="4ee2e-112">Key frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ee2e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4ee2e-113">Return value</span></span>

<span data-ttu-id="4ee2e-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4ee2e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4ee2e-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4ee2e-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4ee2e-116">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="4ee2e-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ee2e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ee2e-117">Remarks</span></span>

<span data-ttu-id="4ee2e-118">Diese Methode ist langsam und sollte nicht verwendet werden, nachdem die Wiedergabe einer Animation begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="4ee2e-118">This method is slow and should not be used after an animation has begun to play.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ee2e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ee2e-119">Requirements</span></span>



| <span data-ttu-id="4ee2e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ee2e-120">Requirement</span></span> | <span data-ttu-id="4ee2e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4ee2e-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee2e-122">Header</span><span class="sxs-lookup"><span data-stu-id="4ee2e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4ee2e-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ee2e-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4ee2e-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4ee2e-124">Library</span></span><br/> | <dl> <span data-ttu-id="4ee2e-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ee2e-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4ee2e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ee2e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ee2e-127">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="4ee2e-127">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
