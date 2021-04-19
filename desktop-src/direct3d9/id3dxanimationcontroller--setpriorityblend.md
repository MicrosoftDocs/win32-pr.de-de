---
description: Legt die vom Animations Controller verwendete Prioritäts Mischungs Gewichtung fest.
ms.assetid: b053024b-f219-48b3-906e-161d9cf47556
title: 'ID3DXAnimationController:: setpriorityblend-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4c820858041c730f971ce2821698f86e6ff2c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366675"
---
# <a name="id3dxanimationcontrollersetpriorityblend-method"></a><span data-ttu-id="4647f-103">ID3DXAnimationController:: setpriorityblend-Methode</span><span class="sxs-lookup"><span data-stu-id="4647f-103">ID3DXAnimationController::SetPriorityBlend method</span></span>

<span data-ttu-id="4647f-104">Legt die vom Animations Controller verwendete Prioritäts Mischungs Gewichtung fest.</span><span class="sxs-lookup"><span data-stu-id="4647f-104">Sets the priority blending weight used by the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="4647f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4647f-105">Syntax</span></span>


```C++
HRESULT SetPriorityBlend(
  [in] FLOAT BlendWeight
);
```



## <a name="parameters"></a><span data-ttu-id="4647f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4647f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4647f-107">*Blendweight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4647f-107">*BlendWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4647f-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4647f-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4647f-109">Das vom Animations Controller verwendete Gewicht für die Prioritäts Mischung.</span><span class="sxs-lookup"><span data-stu-id="4647f-109">Priority blending weight used by the animation controller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4647f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4647f-110">Return value</span></span>

<span data-ttu-id="4647f-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4647f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4647f-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4647f-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4647f-113">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="4647f-113">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4647f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4647f-114">Remarks</span></span>

<span data-ttu-id="4647f-115">Die Blend-Gewichtung wird verwendet, um nachverfolgen mit hoher und niedriger Priorität zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="4647f-115">The blend weight is used to blend high and low priority tracks together.</span></span>

## <a name="requirements"></a><span data-ttu-id="4647f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4647f-116">Requirements</span></span>



| <span data-ttu-id="4647f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4647f-117">Requirement</span></span> | <span data-ttu-id="4647f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4647f-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4647f-119">Header</span><span class="sxs-lookup"><span data-stu-id="4647f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4647f-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4647f-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4647f-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4647f-121">Library</span></span><br/> | <dl> <span data-ttu-id="4647f-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4647f-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4647f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4647f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4647f-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="4647f-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> <dt>

[<span data-ttu-id="4647f-125">**Getpriorityblend**</span><span class="sxs-lookup"><span data-stu-id="4647f-125">**GetPriorityBlend**</span></span>](id3dxanimationcontroller--getpriorityblend.md)
</dt> </dl>

 

 
