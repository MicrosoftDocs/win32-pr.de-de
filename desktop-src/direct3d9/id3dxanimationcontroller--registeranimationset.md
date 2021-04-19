---
description: Fügt dem Animations Controller einen Animations Satz hinzu.
ms.assetid: 93351d61-b7f4-4bd1-a5bf-313911cf6b61
title: 'ID3DXAnimationController:: registeranimationset-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ca70baf55a3dae19422c9026575d75f63eed4bde
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353389"
---
# <a name="id3dxanimationcontrollerregisteranimationset-method"></a><span data-ttu-id="93eb4-103">ID3DXAnimationController:: registeranimationset-Methode</span><span class="sxs-lookup"><span data-stu-id="93eb4-103">ID3DXAnimationController::RegisterAnimationSet method</span></span>

<span data-ttu-id="93eb4-104">Fügt dem Animations Controller einen Animations Satz hinzu.</span><span class="sxs-lookup"><span data-stu-id="93eb4-104">Adds an animation set to the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="93eb4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="93eb4-105">Syntax</span></span>


```C++
HRESULT RegisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="93eb4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="93eb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93eb4-107">*panimset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93eb4-107">*pAnimSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93eb4-108">Typ: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span><span class="sxs-lookup"><span data-stu-id="93eb4-108">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span></span>

<span data-ttu-id="93eb4-109">Zeiger auf den hinzu zufügenden [**ID3DXAnimationSet**](id3dxanimationset.md) -Animations Satz.</span><span class="sxs-lookup"><span data-stu-id="93eb4-109">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93eb4-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93eb4-110">Return value</span></span>

<span data-ttu-id="93eb4-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="93eb4-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="93eb4-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="93eb4-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="93eb4-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="93eb4-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="93eb4-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93eb4-114">Requirements</span></span>



| <span data-ttu-id="93eb4-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93eb4-115">Requirement</span></span> | <span data-ttu-id="93eb4-116">Wert</span><span class="sxs-lookup"><span data-stu-id="93eb4-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93eb4-117">Header</span><span class="sxs-lookup"><span data-stu-id="93eb4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="93eb4-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="93eb4-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="93eb4-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="93eb4-119">Library</span></span><br/> | <dl> <span data-ttu-id="93eb4-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93eb4-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="93eb4-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93eb4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93eb4-122">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="93eb4-122">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




