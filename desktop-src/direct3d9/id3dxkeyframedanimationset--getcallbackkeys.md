---
description: Füllt ein Array mit Rückruf Schlüsseldaten, die für die Keyframe-Animation verwendet werden.
ms.assetid: 2a2aa04a-a889-415b-8aa2-cc5f2bed1f9a
title: 'ID3DXKeyframedAnimationSet:: getcallbackkeys-Methode (D3dx9anim. h)'
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
ms.openlocfilehash: d3f8dbc771fcdde6d1c07a1bf810b322b0a70a30
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219457"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkeys-method"></a><span data-ttu-id="ffba9-103">ID3DXKeyframedAnimationSet:: getcallbackkeys-Methode</span><span class="sxs-lookup"><span data-stu-id="ffba9-103">ID3DXKeyframedAnimationSet::GetCallbackKeys method</span></span>

<span data-ttu-id="ffba9-104">Füllt ein Array mit Rückruf Schlüsseldaten, die für die Keyframe-Animation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ffba9-104">Fills an array with callback key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffba9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffba9-105">Syntax</span></span>


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="ffba9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffba9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffba9-107">*pcallbackkeys* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ffba9-107">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffba9-108">Typ: **[ **LPD3DXKEY- \_ Rückruf**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="ffba9-108">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="ffba9-109">Zeiger auf ein vom Benutzer zugeordneter Array von [**D3DXKEY- \_ Rückruf**](d3dxkey-callback.md) Strukturen, die die Methode mit Rückruf Daten ausfüllen soll.</span><span class="sxs-lookup"><span data-stu-id="ffba9-109">Pointer to a user-allocated array of [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structures that the method is to fill with callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffba9-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ffba9-110">Return value</span></span>

<span data-ttu-id="ffba9-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ffba9-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ffba9-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ffba9-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ffba9-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="ffba9-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffba9-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffba9-114">Requirements</span></span>



| <span data-ttu-id="ffba9-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffba9-115">Requirement</span></span> | <span data-ttu-id="ffba9-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ffba9-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffba9-117">Header</span><span class="sxs-lookup"><span data-stu-id="ffba9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ffba9-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffba9-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ffba9-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ffba9-119">Library</span></span><br/> | <dl> <span data-ttu-id="ffba9-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ffba9-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ffba9-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffba9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffba9-122">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="ffba9-122">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="ffba9-123">**ID3DXKeyframedAnimationSet:: getnumcallbackkeys**</span><span class="sxs-lookup"><span data-stu-id="ffba9-123">**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**</span></span>](id3dxkeyframedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




