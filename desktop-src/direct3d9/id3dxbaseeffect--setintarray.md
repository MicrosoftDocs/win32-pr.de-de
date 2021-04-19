---
description: Legt ein Array von ganzen Zahlen fest.
ms.assetid: 4491bffd-ce5e-4f84-ac11-0314a1b16d63
title: 'ID3DXBaseEffect:: tartintarray-Methode (D3DX9Shader. h)'
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
ms.openlocfilehash: f76ff0d7f4bcc68d7cce85f3d02f2bc207a5f4b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367342"
---
# <a name="id3dxbaseeffectsetintarray-method"></a><span data-ttu-id="dcfd4-103">ID3DXBaseEffect:: tartintarray-Methode</span><span class="sxs-lookup"><span data-stu-id="dcfd4-103">ID3DXBaseEffect::SetIntArray method</span></span>

<span data-ttu-id="dcfd4-104">Legt ein Array von ganzen Zahlen fest.</span><span class="sxs-lookup"><span data-stu-id="dcfd4-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcfd4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dcfd4-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hParameter,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="dcfd4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dcfd4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcfd4-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcfd4-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcfd4-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="dcfd4-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="dcfd4-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="dcfd4-109">Unique identifier.</span></span> <span data-ttu-id="dcfd4-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="dcfd4-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="dcfd4-111">*PN* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcfd4-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcfd4-112">Typ: Konstante **[**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="dcfd4-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dcfd4-113">Array von ganzen Zahlen.</span><span class="sxs-lookup"><span data-stu-id="dcfd4-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="dcfd4-114">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcfd4-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcfd4-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dcfd4-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dcfd4-116">Anzahl von ganzen Zahlen im Array.</span><span class="sxs-lookup"><span data-stu-id="dcfd4-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcfd4-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dcfd4-117">Return value</span></span>

<span data-ttu-id="dcfd4-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dcfd4-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dcfd4-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dcfd4-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dcfd4-120">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="dcfd4-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcfd4-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dcfd4-121">Requirements</span></span>



| <span data-ttu-id="dcfd4-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dcfd4-122">Requirement</span></span> | <span data-ttu-id="dcfd4-123">Wert</span><span class="sxs-lookup"><span data-stu-id="dcfd4-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcfd4-124">Header</span><span class="sxs-lookup"><span data-stu-id="dcfd4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="dcfd4-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcfd4-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="dcfd4-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dcfd4-126">Library</span></span><br/> | <dl> <span data-ttu-id="dcfd4-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcfd4-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="dcfd4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcfd4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcfd4-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="dcfd4-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="dcfd4-130">**Getintarray**</span><span class="sxs-lookup"><span data-stu-id="dcfd4-130">**GetIntArray**</span></span>](id3dxbaseeffect--getintarray.md)
</dt> </dl>

 

 
