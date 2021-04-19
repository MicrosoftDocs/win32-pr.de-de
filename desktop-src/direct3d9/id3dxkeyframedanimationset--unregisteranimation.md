---
description: Entfernen Sie die Animationsdaten aus dem Animations Satz.
ms.assetid: 9821d21e-fe8f-4742-b4f3-63b2578d29ec
title: 'ID3DXKeyframedAnimationSet:: unregisteranimation-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterAnimation
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f5ee7718fb73e441daacf9fdaff38499239915e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357277"
---
# <a name="id3dxkeyframedanimationsetunregisteranimation-method"></a><span data-ttu-id="031cc-103">ID3DXKeyframedAnimationSet:: unregisteranimation-Methode</span><span class="sxs-lookup"><span data-stu-id="031cc-103">ID3DXKeyframedAnimationSet::UnregisterAnimation method</span></span>

<span data-ttu-id="031cc-104">Entfernen Sie die Animationsdaten aus dem Animations Satz.</span><span class="sxs-lookup"><span data-stu-id="031cc-104">Remove the animation data from the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="031cc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="031cc-105">Syntax</span></span>


```C++
HRESULT UnregisterAnimation(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="031cc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="031cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="031cc-107">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="031cc-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="031cc-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="031cc-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="031cc-109">Der Animations Index.</span><span class="sxs-lookup"><span data-stu-id="031cc-109">The animation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="031cc-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="031cc-110">Return value</span></span>

<span data-ttu-id="031cc-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="031cc-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="031cc-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="031cc-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="031cc-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="031cc-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="031cc-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="031cc-114">Requirements</span></span>



| <span data-ttu-id="031cc-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="031cc-115">Requirement</span></span> | <span data-ttu-id="031cc-116">Wert</span><span class="sxs-lookup"><span data-stu-id="031cc-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="031cc-117">Header</span><span class="sxs-lookup"><span data-stu-id="031cc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="031cc-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="031cc-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="031cc-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="031cc-119">Library</span></span><br/> | <dl> <span data-ttu-id="031cc-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="031cc-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="031cc-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="031cc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="031cc-122">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="031cc-122">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
