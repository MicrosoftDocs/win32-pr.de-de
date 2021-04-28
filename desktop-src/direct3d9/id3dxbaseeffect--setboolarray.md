---
description: 'ID3DXBaseEffect::SetBoolArray-Methode: Legt ein Array von booleschen Werten fest.'
ms.assetid: 920b3482-cc30-4ab2-bfce-59f03afe11da
title: ID3DXBaseEffect::SetBoolArray-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetBoolArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cad6846914d348dd49d6362d70271c5af078e35d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093828"
---
# <a name="id3dxbaseeffectsetboolarray-method"></a><span data-ttu-id="b8344-103">ID3DXBaseEffect::SetBoolArray-Methode</span><span class="sxs-lookup"><span data-stu-id="b8344-103">ID3DXBaseEffect::SetBoolArray method</span></span>

<span data-ttu-id="b8344-104">Legt ein Array von booleschen Werten fest.</span><span class="sxs-lookup"><span data-stu-id="b8344-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8344-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8344-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       D3DXHANDLE hParameter,
  [in] const BOOL       *pB,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="b8344-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8344-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8344-107">*hParameter* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b8344-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8344-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b8344-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b8344-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="b8344-109">Unique identifier.</span></span> <span data-ttu-id="b8344-110">Siehe [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="b8344-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8344-111">*pB* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b8344-111">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8344-112">Typ: **const [**BOOL**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b8344-112">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b8344-113">Array von booleschen Werten.</span><span class="sxs-lookup"><span data-stu-id="b8344-113">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="b8344-114">*Anzahl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b8344-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8344-115">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8344-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8344-116">Anzahl der booleschen Werte im Array.</span><span class="sxs-lookup"><span data-stu-id="b8344-116">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8344-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8344-117">Return value</span></span>

<span data-ttu-id="b8344-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b8344-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b8344-119">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b8344-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b8344-120">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="b8344-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8344-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8344-121">Requirements</span></span>



| <span data-ttu-id="b8344-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8344-122">Requirement</span></span> | <span data-ttu-id="b8344-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b8344-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8344-124">Header</span><span class="sxs-lookup"><span data-stu-id="b8344-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b8344-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="b8344-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b8344-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b8344-126">Library</span></span><br/> | <dl> <span data-ttu-id="b8344-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8344-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b8344-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b8344-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8344-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="b8344-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="b8344-130">**GetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="b8344-130">**GetBoolArray**</span></span>](id3dxbaseeffect--getboolarray.md)
</dt> </dl>

 

 
