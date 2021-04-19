---
description: Füllt ein Array mit Translational Key-Daten, die für die Keyframe-Animation verwendet werden.
ms.assetid: ecb791ad-e586-4057-9239-facd37a47637
title: 'ID3DXKeyframedAnimationSet:: gettranslationkeys-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetTranslationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6cc56e5538eb45c01ba7c35115e94719119bc4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353400"
---
# <a name="id3dxkeyframedanimationsetgettranslationkeys-method"></a><span data-ttu-id="9f2bb-103">ID3DXKeyframedAnimationSet:: gettranslationkeys-Methode</span><span class="sxs-lookup"><span data-stu-id="9f2bb-103">ID3DXKeyframedAnimationSet::GetTranslationKeys method</span></span>

<span data-ttu-id="9f2bb-104">Füllt ein Array mit Translational Key-Daten, die für die Keyframe-Animation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f2bb-104">Fills an array with translational key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f2bb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f2bb-105">Syntax</span></span>


```C++
HRESULT GetTranslationKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pTranslationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="9f2bb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f2bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f2bb-107">*Animation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f2bb-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f2bb-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9f2bb-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9f2bb-109">Animations Index.</span><span class="sxs-lookup"><span data-stu-id="9f2bb-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="9f2bb-110">*ptranslationkeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f2bb-110">*pTranslationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f2bb-111">Typ: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="9f2bb-111">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="9f2bb-112">Zeiger auf ein vom Benutzer zugewiesenes Array von [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) Vektoren, das die Methode mit Animations Übersetzungs Daten ausfüllen soll.</span><span class="sxs-lookup"><span data-stu-id="9f2bb-112">Pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method is to fill with animation translation data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f2bb-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f2bb-113">Return value</span></span>

<span data-ttu-id="9f2bb-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9f2bb-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9f2bb-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9f2bb-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9f2bb-116">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="9f2bb-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f2bb-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f2bb-117">Requirements</span></span>



| <span data-ttu-id="9f2bb-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f2bb-118">Requirement</span></span> | <span data-ttu-id="9f2bb-119">Wert</span><span class="sxs-lookup"><span data-stu-id="9f2bb-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f2bb-120">Header</span><span class="sxs-lookup"><span data-stu-id="9f2bb-120">Header</span></span><br/>  | <dl> <span data-ttu-id="9f2bb-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f2bb-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="9f2bb-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9f2bb-122">Library</span></span><br/> | <dl> <span data-ttu-id="9f2bb-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f2bb-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9f2bb-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f2bb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f2bb-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="9f2bb-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="9f2bb-126">**ID3DXKeyframedAnimationSet:: getnumtranslationkeys**</span><span class="sxs-lookup"><span data-stu-id="9f2bb-126">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span></span>](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
