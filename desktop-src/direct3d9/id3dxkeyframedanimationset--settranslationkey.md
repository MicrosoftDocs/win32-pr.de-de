---
description: Legen Sie Übersetzungs Informationen für einen bestimmten Keyframe im Animations Satz fest.
ms.assetid: 4a926c0f-6d57-48d4-bb3b-60766fc78e40
title: 'ID3DXKeyframedAnimationSet:: settranslationkey-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5bdfb8fb02a2b06dc797317d35cc14e75bd6f221
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353398"
---
# <a name="id3dxkeyframedanimationsetsettranslationkey-method"></a><span data-ttu-id="5aaa3-103">ID3DXKeyframedAnimationSet:: settranslationkey-Methode</span><span class="sxs-lookup"><span data-stu-id="5aaa3-103">ID3DXKeyframedAnimationSet::SetTranslationKey method</span></span>

<span data-ttu-id="5aaa3-104">Legen Sie Übersetzungs Informationen für einen bestimmten Keyframe im Animations Satz fest.</span><span class="sxs-lookup"><span data-stu-id="5aaa3-104">Set translation information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aaa3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5aaa3-105">Syntax</span></span>


```C++
HRESULT SetTranslationKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pTranslationKey
);
```



## <a name="parameters"></a><span data-ttu-id="5aaa3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5aaa3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aaa3-107">*Animation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5aaa3-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aaa3-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5aaa3-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5aaa3-109">Animations Index.</span><span class="sxs-lookup"><span data-stu-id="5aaa3-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="5aaa3-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5aaa3-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aaa3-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5aaa3-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5aaa3-112">Keyframe.</span><span class="sxs-lookup"><span data-stu-id="5aaa3-112">Key Frame.</span></span>

</dd> <dt>

<span data-ttu-id="5aaa3-113">*ptranslationkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5aaa3-113">*pTranslationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aaa3-114">Typ: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="5aaa3-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="5aaa3-115">Zeiger auf die Übersetzungs Daten.</span><span class="sxs-lookup"><span data-stu-id="5aaa3-115">Pointer to the translation data.</span></span> <span data-ttu-id="5aaa3-116">Siehe [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="5aaa3-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aaa3-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5aaa3-117">Return value</span></span>

<span data-ttu-id="5aaa3-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5aaa3-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5aaa3-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5aaa3-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5aaa3-120">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="5aaa3-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aaa3-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5aaa3-121">Requirements</span></span>



| <span data-ttu-id="5aaa3-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5aaa3-122">Requirement</span></span> | <span data-ttu-id="5aaa3-123">Wert</span><span class="sxs-lookup"><span data-stu-id="5aaa3-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5aaa3-124">Header</span><span class="sxs-lookup"><span data-stu-id="5aaa3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5aaa3-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="5aaa3-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="5aaa3-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5aaa3-126">Library</span></span><br/> | <dl> <span data-ttu-id="5aaa3-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5aaa3-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5aaa3-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5aaa3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aaa3-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="5aaa3-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
