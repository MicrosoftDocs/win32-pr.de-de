---
description: 'ID3DXBaseEffect::SetIntArray-Methode: Legt ein Array von ganzen Zahlen fest.'
ms.assetid: 4491bffd-ce5e-4f84-ac11-0314a1b16d63
title: ID3DXBaseEffect::SetIntArray-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetIntArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a14e837a0903290c3197bbb17ec4b2da3f68b419
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093758"
---
# <a name="id3dxbaseeffectsetintarray-method"></a><span data-ttu-id="553a2-103">ID3DXBaseEffect::SetIntArray-Methode</span><span class="sxs-lookup"><span data-stu-id="553a2-103">ID3DXBaseEffect::SetIntArray method</span></span>

<span data-ttu-id="553a2-104">Legt ein Array von ganzen Zahlen fest.</span><span class="sxs-lookup"><span data-stu-id="553a2-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="553a2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="553a2-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hParameter,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="553a2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="553a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="553a2-107">*hParameter* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="553a2-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="553a2-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="553a2-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="553a2-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="553a2-109">Unique identifier.</span></span> <span data-ttu-id="553a2-110">Siehe [Handles (Direct3D 9).](handles.md)</span><span class="sxs-lookup"><span data-stu-id="553a2-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="553a2-111">*pn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="553a2-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="553a2-112">Typ: **const [**INT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="553a2-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="553a2-113">Array von ganzen Zahlen.</span><span class="sxs-lookup"><span data-stu-id="553a2-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="553a2-114">*Anzahl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="553a2-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="553a2-115">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="553a2-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="553a2-116">Anzahl der ganzen Zahlen im Array.</span><span class="sxs-lookup"><span data-stu-id="553a2-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="553a2-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="553a2-117">Return value</span></span>

<span data-ttu-id="553a2-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="553a2-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="553a2-119">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="553a2-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="553a2-120">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="553a2-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="553a2-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="553a2-121">Requirements</span></span>



| <span data-ttu-id="553a2-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="553a2-122">Requirement</span></span> | <span data-ttu-id="553a2-123">Wert</span><span class="sxs-lookup"><span data-stu-id="553a2-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="553a2-124">Header</span><span class="sxs-lookup"><span data-stu-id="553a2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="553a2-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="553a2-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="553a2-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="553a2-126">Library</span></span><br/> | <dl> <span data-ttu-id="553a2-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="553a2-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="553a2-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="553a2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="553a2-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="553a2-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="553a2-130">**GetIntArray**</span><span class="sxs-lookup"><span data-stu-id="553a2-130">**GetIntArray**</span></span>](id3dxbaseeffect--getintarray.md)
</dt> </dl>

 

 
