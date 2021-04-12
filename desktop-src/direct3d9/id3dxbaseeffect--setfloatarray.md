---
description: Legt ein Array von Gleit Komma Werten fest.
ms.assetid: 4b9c27b4-0255-4bbf-9168-491936d64fb9
title: 'ID3DXBaseEffect:: setfloatarray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetFloatArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9927f3cd79d7950a94e62881089fb06c67395bac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219431"
---
# <a name="id3dxbaseeffectsetfloatarray-method"></a><span data-ttu-id="99fb6-103">ID3DXBaseEffect:: setfloatarray-Methode</span><span class="sxs-lookup"><span data-stu-id="99fb6-103">ID3DXBaseEffect::SetFloatArray method</span></span>

<span data-ttu-id="99fb6-104">Legt ein Array von Gleit Komma Werten fest.</span><span class="sxs-lookup"><span data-stu-id="99fb6-104">Sets an array of floating point values.</span></span>

## <a name="syntax"></a><span data-ttu-id="99fb6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="99fb6-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hParameter,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="99fb6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="99fb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99fb6-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99fb6-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99fb6-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="99fb6-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="99fb6-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="99fb6-109">Unique identifier.</span></span> <span data-ttu-id="99fb6-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="99fb6-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="99fb6-111">*PF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99fb6-111">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99fb6-112">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="99fb6-112">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="99fb6-113">Array von Gleit Komma Werten.</span><span class="sxs-lookup"><span data-stu-id="99fb6-113">Array of floating point values.</span></span>

</dd> <dt>

<span data-ttu-id="99fb6-114">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99fb6-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99fb6-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99fb6-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99fb6-116">Anzahl von Gleit Komma Werten im Array.</span><span class="sxs-lookup"><span data-stu-id="99fb6-116">Number of floating point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99fb6-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99fb6-117">Return value</span></span>

<span data-ttu-id="99fb6-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99fb6-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99fb6-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="99fb6-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="99fb6-120">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="99fb6-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="99fb6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99fb6-121">Requirements</span></span>



| <span data-ttu-id="99fb6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99fb6-122">Requirement</span></span> | <span data-ttu-id="99fb6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="99fb6-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="99fb6-124">Header</span><span class="sxs-lookup"><span data-stu-id="99fb6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="99fb6-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="99fb6-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="99fb6-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="99fb6-126">Library</span></span><br/> | <dl> <span data-ttu-id="99fb6-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99fb6-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="99fb6-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99fb6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99fb6-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="99fb6-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="99fb6-130">**Getfloatarray**</span><span class="sxs-lookup"><span data-stu-id="99fb6-130">**GetFloatArray**</span></span>](id3dxbaseeffect--getfloatarray.md)
</dt> </dl>

 

 
