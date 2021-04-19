---
description: Ruft ein Array von booleschen Werten ab.
ms.assetid: 4a5e2f48-fa82-47dc-a388-02a8679585d2
title: 'ID3DXBaseEffect:: getboolarray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetBoolArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f714dfa91baba14524f12b6c3b2cb85211484cf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355841"
---
# <a name="id3dxbaseeffectgetboolarray-method"></a><span data-ttu-id="31544-103">ID3DXBaseEffect:: getboolarray-Methode</span><span class="sxs-lookup"><span data-stu-id="31544-103">ID3DXBaseEffect::GetBoolArray method</span></span>

<span data-ttu-id="31544-104">Ruft ein Array von booleschen Werten ab.</span><span class="sxs-lookup"><span data-stu-id="31544-104">Gets an array of BOOL values.</span></span>

## <a name="syntax"></a><span data-ttu-id="31544-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="31544-105">Syntax</span></span>


```C++
HRESULT GetBoolArray(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pB,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="31544-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="31544-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31544-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31544-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31544-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="31544-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="31544-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="31544-109">Unique identifier.</span></span> <span data-ttu-id="31544-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="31544-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="31544-111">*PB* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="31544-111">*pB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31544-112">Typ: **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="31544-112">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="31544-113">Gibt ein Array von booleschen Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="31544-113">Returns an array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="31544-114">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31544-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31544-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31544-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31544-116">Anzahl von booleschen Werten im Array.</span><span class="sxs-lookup"><span data-stu-id="31544-116">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31544-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31544-117">Return value</span></span>

<span data-ttu-id="31544-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="31544-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="31544-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="31544-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="31544-120">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="31544-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="31544-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31544-121">Requirements</span></span>



| <span data-ttu-id="31544-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31544-122">Requirement</span></span> | <span data-ttu-id="31544-123">Wert</span><span class="sxs-lookup"><span data-stu-id="31544-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="31544-124">Header</span><span class="sxs-lookup"><span data-stu-id="31544-124">Header</span></span><br/>  | <dl> <span data-ttu-id="31544-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="31544-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="31544-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="31544-126">Library</span></span><br/> | <dl> <span data-ttu-id="31544-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31544-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="31544-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31544-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31544-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="31544-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="31544-130">**Setboolarray**</span><span class="sxs-lookup"><span data-stu-id="31544-130">**SetBoolArray**</span></span>](id3dxbaseeffect--setboolarray.md)
</dt> </dl>

 

 
