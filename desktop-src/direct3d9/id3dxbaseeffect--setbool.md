---
description: 'ID3DXBaseEffect::SetBool-Methode: Legt einen BOOL-Wert fest.'
ms.assetid: bb7c4860-50a0-416a-b9e0-5a2bec113e3c
title: ID3DXBaseEffect::SetBool-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetBool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5045c26f521da289899c8f8bc0d97b7eaf01826f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097518"
---
# <a name="id3dxbaseeffectsetbool-method"></a><span data-ttu-id="5153f-103">ID3DXBaseEffect::SetBool-Methode</span><span class="sxs-lookup"><span data-stu-id="5153f-103">ID3DXBaseEffect::SetBool method</span></span>

<span data-ttu-id="5153f-104">Legt einen BOOL-Wert fest.</span><span class="sxs-lookup"><span data-stu-id="5153f-104">Sets a BOOL value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5153f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5153f-105">Syntax</span></span>


```C++
HRESULT SetBool(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       b
);
```



## <a name="parameters"></a><span data-ttu-id="5153f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5153f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5153f-107">*hParameter* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5153f-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5153f-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5153f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5153f-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="5153f-109">Unique identifier.</span></span> <span data-ttu-id="5153f-110">Siehe [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="5153f-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="5153f-111">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5153f-111">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5153f-112">Typ: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5153f-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5153f-113">Boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="5153f-113">Boolean value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5153f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5153f-114">Return value</span></span>

<span data-ttu-id="5153f-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5153f-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5153f-116">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5153f-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5153f-117">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="5153f-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5153f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5153f-118">Requirements</span></span>



| <span data-ttu-id="5153f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5153f-119">Requirement</span></span> | <span data-ttu-id="5153f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5153f-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5153f-121">Header</span><span class="sxs-lookup"><span data-stu-id="5153f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5153f-122"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="5153f-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5153f-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5153f-123">Library</span></span><br/> | <dl> <span data-ttu-id="5153f-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5153f-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5153f-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5153f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5153f-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="5153f-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="5153f-127">**GetBool**</span><span class="sxs-lookup"><span data-stu-id="5153f-127">**GetBool**</span></span>](id3dxbaseeffect--getbool.md)
</dt> </dl>

 

 
