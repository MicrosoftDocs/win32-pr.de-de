---
description: Entfernt die Skalierungs Daten am angegebenen Keyframe.
ms.assetid: b0bf5665-ccfb-4b87-8e88-9a717ef57955
title: 'ID3DXKeyframedAnimationSet:: unregisterscalekey-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6d1ac3f500b80d8922646fddff9f05d8c91d9c48
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961742"
---
# <a name="id3dxkeyframedanimationsetunregisterscalekey-method"></a><span data-ttu-id="4e1cd-103">ID3DXKeyframedAnimationSet:: unregisterscalekey-Methode</span><span class="sxs-lookup"><span data-stu-id="4e1cd-103">ID3DXKeyframedAnimationSet::UnregisterScaleKey method</span></span>

<span data-ttu-id="4e1cd-104">Entfernt die Skalierungs Daten am angegebenen Keyframe.</span><span class="sxs-lookup"><span data-stu-id="4e1cd-104">Removes the scale data at the specified key frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e1cd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e1cd-105">Syntax</span></span>


```C++
HRESULT UnregisterScaleKey(
  [in] UINT Animation,
  [in] UINT Key
);
```



## <a name="parameters"></a><span data-ttu-id="4e1cd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e1cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e1cd-107">*Animation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e1cd-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1cd-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e1cd-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e1cd-109">Animations Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="4e1cd-109">Animation identifier.</span></span>

</dd> <dt>

<span data-ttu-id="4e1cd-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e1cd-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1cd-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e1cd-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e1cd-112">Keyframe.</span><span class="sxs-lookup"><span data-stu-id="4e1cd-112">Key frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e1cd-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e1cd-113">Return value</span></span>

<span data-ttu-id="4e1cd-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4e1cd-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4e1cd-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4e1cd-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4e1cd-116">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="4e1cd-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e1cd-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e1cd-117">Remarks</span></span>

<span data-ttu-id="4e1cd-118">Diese Methode ist langsam und sollte nicht verwendet werden, nachdem die Wiedergabe einer Animation begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="4e1cd-118">This method is slow and should not be used after an animation has begun to play.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e1cd-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e1cd-119">Requirements</span></span>



| <span data-ttu-id="4e1cd-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e1cd-120">Requirement</span></span> | <span data-ttu-id="4e1cd-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4e1cd-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e1cd-122">Header</span><span class="sxs-lookup"><span data-stu-id="4e1cd-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4e1cd-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e1cd-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4e1cd-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4e1cd-124">Library</span></span><br/> | <dl> <span data-ttu-id="4e1cd-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e1cd-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4e1cd-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e1cd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e1cd-127">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="4e1cd-127">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
