---
description: 'ID3DXCompressedAnimationSet::GetCallbackKeys-Methode: Füllt ein Array mit Rückrufschlüsseldaten aus, die für die Keyframe-Animation verwendet werden.'
ms.assetid: 0dc30c1f-9ffb-42ec-8074-84293f16c344
title: ID3DXCompressedAnimationSet::GetCallbackKeys-Methode (D3dx9anim.h)
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
ms.openlocfilehash: d7c430358b5ba7f66c5a79b08ae01925141e659f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115328"
---
# <a name="id3dxcompressedanimationsetgetcallbackkeys-method"></a><span data-ttu-id="8e4b9-103">ID3DXCompressedAnimationSet::GetCallbackKeys-Methode</span><span class="sxs-lookup"><span data-stu-id="8e4b9-103">ID3DXCompressedAnimationSet::GetCallbackKeys method</span></span>

<span data-ttu-id="8e4b9-104">Füllt ein Array mit Rückrufschlüsseldaten aus, die für die Keyframe-Animation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e4b9-104">Fills an array with callback key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e4b9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e4b9-105">Syntax</span></span>


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="8e4b9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e4b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e4b9-107">*pCallbackKeys* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8e4b9-107">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e4b9-108">Typ: **[ **LPD3DXKEY \_ CALLBACK**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="8e4b9-108">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="8e4b9-109">Zeiger auf ein vom Benutzer zugeordnetes Array von [**D3DXKEY \_ CALLBACK-Strukturen,**](d3dxkey-callback.md) das die Methode mit Rückrufdaten füllen soll.</span><span class="sxs-lookup"><span data-stu-id="8e4b9-109">Pointer to a user-allocated array of [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structures that the method is to fill with callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e4b9-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e4b9-110">Return value</span></span>

<span data-ttu-id="8e4b9-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8e4b9-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8e4b9-112">Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8e4b9-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8e4b9-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8e4b9-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e4b9-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e4b9-114">Requirements</span></span>



| <span data-ttu-id="8e4b9-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e4b9-115">Requirement</span></span> | <span data-ttu-id="8e4b9-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8e4b9-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e4b9-117">Header</span><span class="sxs-lookup"><span data-stu-id="8e4b9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8e4b9-118"><dt>D3dx9anim.h</dt></span><span class="sxs-lookup"><span data-stu-id="8e4b9-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="8e4b9-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8e4b9-119">Library</span></span><br/> | <dl> <span data-ttu-id="8e4b9-120"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e4b9-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8e4b9-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8e4b9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e4b9-122">ID3DXCompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="8e4b9-122">ID3DXCompressedAnimationSet</span></span>](id3dxcompressedanimationset.md)
</dt> <dt>

[<span data-ttu-id="8e4b9-123">**ID3DXCompressedAnimationSet::GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="8e4b9-123">**ID3DXCompressedAnimationSet::GetNumCallbackKeys**</span></span>](id3dxcompressedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




