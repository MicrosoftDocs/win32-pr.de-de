---
description: Füllt ein Array mit Rückruf Schlüsseldaten, die für die Keyframe-Animation verwendet werden.
ms.assetid: 0dc30c1f-9ffb-42ec-8074-84293f16c344
title: 'ID3DXCompressedAnimationSet:: getcallbackkeys-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fe56a3dbdd7d019deb5d7111fa592470bffd244d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365103"
---
# <a name="id3dxcompressedanimationsetgetcallbackkeys-method"></a><span data-ttu-id="d3cd2-103">ID3DXCompressedAnimationSet:: getcallbackkeys-Methode</span><span class="sxs-lookup"><span data-stu-id="d3cd2-103">ID3DXCompressedAnimationSet::GetCallbackKeys method</span></span>

<span data-ttu-id="d3cd2-104">Füllt ein Array mit Rückruf Schlüsseldaten, die für die Keyframe-Animation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3cd2-104">Fills an array with callback key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3cd2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3cd2-105">Syntax</span></span>


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="d3cd2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3cd2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3cd2-107">*pcallbackkeys* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d3cd2-107">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3cd2-108">Typ: **[ **LPD3DXKEY- \_ Rückruf**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="d3cd2-108">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="d3cd2-109">Zeiger auf ein vom Benutzer zugeordneter Array von [**D3DXKEY- \_ Rückruf**](d3dxkey-callback.md) Strukturen, die die Methode mit Rückruf Daten ausfüllen soll.</span><span class="sxs-lookup"><span data-stu-id="d3cd2-109">Pointer to a user-allocated array of [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structures that the method is to fill with callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3cd2-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3cd2-110">Return value</span></span>

<span data-ttu-id="d3cd2-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d3cd2-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d3cd2-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d3cd2-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d3cd2-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="d3cd2-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3cd2-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3cd2-114">Requirements</span></span>



| <span data-ttu-id="d3cd2-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3cd2-115">Requirement</span></span> | <span data-ttu-id="d3cd2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d3cd2-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3cd2-117">Header</span><span class="sxs-lookup"><span data-stu-id="d3cd2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d3cd2-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3cd2-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d3cd2-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d3cd2-119">Library</span></span><br/> | <dl> <span data-ttu-id="d3cd2-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3cd2-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d3cd2-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3cd2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3cd2-122">ID3DXCompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="d3cd2-122">ID3DXCompressedAnimationSet</span></span>](id3dxcompressedanimationset.md)
</dt> <dt>

[<span data-ttu-id="d3cd2-123">**ID3DXCompressedAnimationSet:: getnumcallbackkeys**</span><span class="sxs-lookup"><span data-stu-id="d3cd2-123">**ID3DXCompressedAnimationSet::GetNumCallbackKeys**</span></span>](id3dxcompressedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




