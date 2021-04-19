---
description: Legt ein Array von booleschen Werten fest.
ms.assetid: 920b3482-cc30-4ab2-bfce-59f03afe11da
title: 'ID3DXBaseEffect:: setboolarray-Methode (D3DX9Shader. h)'
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
ms.openlocfilehash: 813259fc9fcca954c4d7a992c7542387be33bb6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350657"
---
# <a name="id3dxbaseeffectsetboolarray-method"></a><span data-ttu-id="825ed-103">ID3DXBaseEffect:: setboolarray-Methode</span><span class="sxs-lookup"><span data-stu-id="825ed-103">ID3DXBaseEffect::SetBoolArray method</span></span>

<span data-ttu-id="825ed-104">Legt ein Array von booleschen Werten fest.</span><span class="sxs-lookup"><span data-stu-id="825ed-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="825ed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="825ed-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       D3DXHANDLE hParameter,
  [in] const BOOL       *pB,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="825ed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="825ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="825ed-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="825ed-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="825ed-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="825ed-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="825ed-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="825ed-109">Unique identifier.</span></span> <span data-ttu-id="825ed-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="825ed-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="825ed-111">*PB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="825ed-111">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="825ed-112">Typ: Konstante **[**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="825ed-112">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="825ed-113">Array von booleschen Werten.</span><span class="sxs-lookup"><span data-stu-id="825ed-113">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="825ed-114">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="825ed-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="825ed-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="825ed-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="825ed-116">Anzahl von booleschen Werten im Array.</span><span class="sxs-lookup"><span data-stu-id="825ed-116">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="825ed-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="825ed-117">Return value</span></span>

<span data-ttu-id="825ed-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="825ed-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="825ed-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="825ed-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="825ed-120">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="825ed-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="825ed-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="825ed-121">Requirements</span></span>



| <span data-ttu-id="825ed-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="825ed-122">Requirement</span></span> | <span data-ttu-id="825ed-123">Wert</span><span class="sxs-lookup"><span data-stu-id="825ed-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="825ed-124">Header</span><span class="sxs-lookup"><span data-stu-id="825ed-124">Header</span></span><br/>  | <dl> <span data-ttu-id="825ed-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="825ed-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="825ed-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="825ed-126">Library</span></span><br/> | <dl> <span data-ttu-id="825ed-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="825ed-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="825ed-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="825ed-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="825ed-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="825ed-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="825ed-130">**Getboolarray**</span><span class="sxs-lookup"><span data-stu-id="825ed-130">**GetBoolArray**</span></span>](id3dxbaseeffect--getboolarray.md)
</dt> </dl>

 

 
