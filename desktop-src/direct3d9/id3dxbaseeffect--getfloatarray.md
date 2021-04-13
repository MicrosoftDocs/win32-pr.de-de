---
description: Ruft ein Array von Gleit Komma Werten ab.
ms.assetid: ba839129-c332-4ce8-b7c1-ea0ef4697ade
title: 'ID3DXBaseEffect:: getfloatarray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFloatArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2ea71daa3b207a8f7716bf0a0db3608554c0b9f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355917"
---
# <a name="id3dxbaseeffectgetfloatarray-method"></a><span data-ttu-id="0c11f-103">ID3DXBaseEffect:: getfloatarray-Methode</span><span class="sxs-lookup"><span data-stu-id="0c11f-103">ID3DXBaseEffect::GetFloatArray method</span></span>

<span data-ttu-id="0c11f-104">Ruft ein Array von Gleit Komma Werten ab.</span><span class="sxs-lookup"><span data-stu-id="0c11f-104">Gets an array of floating point values.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c11f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c11f-105">Syntax</span></span>


```C++
HRESULT GetFloatArray(
  [in]  D3DXHANDLE hParameter,
  [out] FLOAT      *pf,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="0c11f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c11f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c11f-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c11f-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c11f-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0c11f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0c11f-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="0c11f-109">Unique identifier.</span></span> <span data-ttu-id="0c11f-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="0c11f-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c11f-111">*PF* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0c11f-111">*pf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c11f-112">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0c11f-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0c11f-113">Gibt ein Array von Gleit Komma Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="0c11f-113">Returns an array of floating point values.</span></span>

</dd> <dt>

<span data-ttu-id="0c11f-114">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c11f-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c11f-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0c11f-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0c11f-116">Anzahl von Gleit Komma Werten im Array.</span><span class="sxs-lookup"><span data-stu-id="0c11f-116">Number of floating point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c11f-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c11f-117">Return value</span></span>

<span data-ttu-id="0c11f-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0c11f-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0c11f-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0c11f-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0c11f-120">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="0c11f-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c11f-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c11f-121">Requirements</span></span>



| <span data-ttu-id="0c11f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c11f-122">Requirement</span></span> | <span data-ttu-id="0c11f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0c11f-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c11f-124">Header</span><span class="sxs-lookup"><span data-stu-id="0c11f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0c11f-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c11f-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0c11f-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0c11f-126">Library</span></span><br/> | <dl> <span data-ttu-id="0c11f-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c11f-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0c11f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c11f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c11f-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="0c11f-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="0c11f-130">**Setfloatarray**</span><span class="sxs-lookup"><span data-stu-id="0c11f-130">**SetFloatArray**</span></span>](id3dxbaseeffect--setfloatarray.md)
</dt> </dl>

 

 
