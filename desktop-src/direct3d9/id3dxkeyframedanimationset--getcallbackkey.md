---
description: Ruft Informationen zu einem bestimmten Rückruf im Animations Satz ab.
ms.assetid: a1d3ca96-2852-420a-aa5c-a434970e5523
title: 'ID3DXKeyframedAnimationSet:: getcallbackkey-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95a3f5a97b84862a66d18b60a3776e183df36444
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353768"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkey-method"></a><span data-ttu-id="e54d3-103">ID3DXKeyframedAnimationSet:: getcallbackkey-Methode</span><span class="sxs-lookup"><span data-stu-id="e54d3-103">ID3DXKeyframedAnimationSet::GetCallbackKey method</span></span>

<span data-ttu-id="e54d3-104">Ruft Informationen zu einem bestimmten Rückruf im Animations Satz ab.</span><span class="sxs-lookup"><span data-stu-id="e54d3-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="e54d3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e54d3-105">Syntax</span></span>


```C++
HRESULT GetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="e54d3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e54d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e54d3-107">*Animation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e54d3-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e54d3-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e54d3-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e54d3-109">Animations Index.</span><span class="sxs-lookup"><span data-stu-id="e54d3-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="e54d3-110">*pcallbackkeys* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e54d3-110">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e54d3-111">Typ: **[ **LPD3DXKEY- \_ Rückruf**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="e54d3-111">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="e54d3-112">Zeiger auf die [**Rückruffunktion**](d3dxkey-callback.md).</span><span class="sxs-lookup"><span data-stu-id="e54d3-112">Pointer to the [**callback function**](d3dxkey-callback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e54d3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e54d3-113">Return value</span></span>

<span data-ttu-id="e54d3-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e54d3-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e54d3-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e54d3-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e54d3-116">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="e54d3-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e54d3-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e54d3-117">Requirements</span></span>



| <span data-ttu-id="e54d3-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e54d3-118">Requirement</span></span> | <span data-ttu-id="e54d3-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e54d3-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e54d3-120">Header</span><span class="sxs-lookup"><span data-stu-id="e54d3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e54d3-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e54d3-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e54d3-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e54d3-122">Library</span></span><br/> | <dl> <span data-ttu-id="e54d3-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e54d3-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e54d3-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e54d3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e54d3-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="e54d3-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
