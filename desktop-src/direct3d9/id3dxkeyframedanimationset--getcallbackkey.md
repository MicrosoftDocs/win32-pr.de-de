---
description: 'ID3DXKeyframedAnimationSet::GetCallbackKey-Methode: Ruft Informationen zu einem bestimmten Rückruf im Animationssatz ab.'
ms.assetid: a1d3ca96-2852-420a-aa5c-a434970e5523
title: ID3DXKeyframedAnimationSet::GetCallbackKey-Methode (D3dx9anim.h)
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
ms.openlocfilehash: f3ebbf93bd482a2259ffdaaf272c65b5e86d5270
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090318"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkey-method"></a><span data-ttu-id="38bc6-103">ID3DXKeyframedAnimationSet::GetCallbackKey-Methode</span><span class="sxs-lookup"><span data-stu-id="38bc6-103">ID3DXKeyframedAnimationSet::GetCallbackKey method</span></span>

<span data-ttu-id="38bc6-104">Ruft Informationen zu einem bestimmten Rückruf im Animationssatz ab.</span><span class="sxs-lookup"><span data-stu-id="38bc6-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="38bc6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="38bc6-105">Syntax</span></span>


```C++
HRESULT GetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="38bc6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="38bc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38bc6-107">*Animation* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="38bc6-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38bc6-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38bc6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38bc6-109">Animationsindex.</span><span class="sxs-lookup"><span data-stu-id="38bc6-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="38bc6-110">*pCallbackKeys* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="38bc6-110">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38bc6-111">Typ: **[ **LPD3DXKEY \_ CALLBACK**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="38bc6-111">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="38bc6-112">Zeiger auf die [**Rückruffunktion**](d3dxkey-callback.md).</span><span class="sxs-lookup"><span data-stu-id="38bc6-112">Pointer to the [**callback function**](d3dxkey-callback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38bc6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38bc6-113">Return value</span></span>

<span data-ttu-id="38bc6-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="38bc6-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="38bc6-115">Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="38bc6-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="38bc6-116">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="38bc6-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="38bc6-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38bc6-117">Requirements</span></span>



| <span data-ttu-id="38bc6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38bc6-118">Requirement</span></span> | <span data-ttu-id="38bc6-119">Wert</span><span class="sxs-lookup"><span data-stu-id="38bc6-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="38bc6-120">Header</span><span class="sxs-lookup"><span data-stu-id="38bc6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="38bc6-121"><dt>D3dx9anim.h</dt></span><span class="sxs-lookup"><span data-stu-id="38bc6-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="38bc6-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="38bc6-122">Library</span></span><br/> | <dl> <span data-ttu-id="38bc6-123"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="38bc6-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="38bc6-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="38bc6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38bc6-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="38bc6-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
