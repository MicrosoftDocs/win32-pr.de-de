---
description: Entfernt einen Animations Satz aus dem Animations Controller.
ms.assetid: 2ca99651-8249-44c2-9560-b3cfaa930862
title: 'ID3DXAnimationController:: unregisteranimationset-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnregisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 35c70552f16daac6d2cfed5cbccf268179526ae1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351990"
---
# <a name="id3dxanimationcontrollerunregisteranimationset-method"></a><span data-ttu-id="47fd3-103">ID3DXAnimationController:: unregisteranimationset-Methode</span><span class="sxs-lookup"><span data-stu-id="47fd3-103">ID3DXAnimationController::UnregisterAnimationSet method</span></span>

<span data-ttu-id="47fd3-104">Entfernt einen Animations Satz aus dem Animations Controller.</span><span class="sxs-lookup"><span data-stu-id="47fd3-104">Removes an animation set from the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="47fd3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="47fd3-105">Syntax</span></span>


```C++
HRESULT UnregisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="47fd3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="47fd3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47fd3-107">*panimset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47fd3-107">*pAnimSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47fd3-108">Typ: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span><span class="sxs-lookup"><span data-stu-id="47fd3-108">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span></span>

<span data-ttu-id="47fd3-109">Zeiger auf den [**ID3DXAnimationSet**](id3dxanimationset.md) -Animations Satz, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="47fd3-109">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47fd3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47fd3-110">Return value</span></span>

<span data-ttu-id="47fd3-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="47fd3-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="47fd3-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="47fd3-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="47fd3-113">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, D3DERR \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="47fd3-113">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="47fd3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47fd3-114">Requirements</span></span>



| <span data-ttu-id="47fd3-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47fd3-115">Requirement</span></span> | <span data-ttu-id="47fd3-116">Wert</span><span class="sxs-lookup"><span data-stu-id="47fd3-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47fd3-117">Header</span><span class="sxs-lookup"><span data-stu-id="47fd3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="47fd3-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="47fd3-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="47fd3-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="47fd3-119">Library</span></span><br/> | <dl> <span data-ttu-id="47fd3-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47fd3-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="47fd3-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47fd3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47fd3-122">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="47fd3-122">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




