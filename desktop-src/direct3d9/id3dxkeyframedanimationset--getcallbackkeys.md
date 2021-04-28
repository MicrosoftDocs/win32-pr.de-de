---
description: 'ID3DXKeyframedAnimationSet::GetCallbackKeys-Methode: Füllt ein Array mit Rückrufschlüsseldaten auf, die für die Keyframeanimation verwendet werden.'
ms.assetid: 2a2aa04a-a889-415b-8aa2-cc5f2bed1f9a
title: ID3DXKeyframedAnimationSet::GetCallbackKeys-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f3bdb7049de3b5d6aad10b5ff5100d01d05e3ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093718"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkeys-method"></a><span data-ttu-id="b1da2-103">ID3DXKeyframedAnimationSet::GetCallbackKeys-Methode</span><span class="sxs-lookup"><span data-stu-id="b1da2-103">ID3DXKeyframedAnimationSet::GetCallbackKeys method</span></span>

<span data-ttu-id="b1da2-104">Füllt ein Array mit Rückrufschlüsseldaten, die für die Keyframe-Animation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b1da2-104">Fills an array with callback key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1da2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1da2-105">Syntax</span></span>


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="b1da2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1da2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1da2-107">*pCallbackKeys* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b1da2-107">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1da2-108">Typ: **[ **LPD3DXKEY \_ CALLBACK**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="b1da2-108">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="b1da2-109">Zeiger auf ein vom Benutzer zugewiesenes Array von [**D3DXKEY \_ CALLBACK-Strukturen,**](d3dxkey-callback.md) die von der -Methode mit Rückrufdaten auffüllt werden.</span><span class="sxs-lookup"><span data-stu-id="b1da2-109">Pointer to a user-allocated array of [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structures that the method is to fill with callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1da2-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1da2-110">Return value</span></span>

<span data-ttu-id="b1da2-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b1da2-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b1da2-112">Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b1da2-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b1da2-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b1da2-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1da2-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1da2-114">Requirements</span></span>



| <span data-ttu-id="b1da2-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1da2-115">Requirement</span></span> | <span data-ttu-id="b1da2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b1da2-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1da2-117">Header</span><span class="sxs-lookup"><span data-stu-id="b1da2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b1da2-118"><dt>D3dx9anim.h</dt></span><span class="sxs-lookup"><span data-stu-id="b1da2-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="b1da2-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b1da2-119">Library</span></span><br/> | <dl> <span data-ttu-id="b1da2-120"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1da2-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b1da2-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b1da2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1da2-122">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="b1da2-122">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="b1da2-123">**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="b1da2-123">**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**</span></span>](id3dxkeyframedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




