---
description: Legt ein Array von Vektoren fest.
ms.assetid: 7a9c61b4-7bfc-4879-abd2-a42d40e9b2a7
title: 'ID3DXBaseEffect:: setvectorarray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetVectorArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4c5deace65608ee547b8fdcc4fb236b11d38c810
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961676"
---
# <a name="id3dxbaseeffectsetvectorarray-method"></a><span data-ttu-id="64f34-103">ID3DXBaseEffect:: setvectorarray-Methode</span><span class="sxs-lookup"><span data-stu-id="64f34-103">ID3DXBaseEffect::SetVectorArray method</span></span>

<span data-ttu-id="64f34-104">Legt ein Array von Vektoren fest.</span><span class="sxs-lookup"><span data-stu-id="64f34-104">Sets an array of vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="64f34-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="64f34-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       D3DXHANDLE  hParameter,
  [in] const D3DXVECTOR4 *pVector,
  [in]       UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="64f34-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="64f34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64f34-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64f34-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f34-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="64f34-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="64f34-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="64f34-109">Unique identifier.</span></span> <span data-ttu-id="64f34-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="64f34-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="64f34-111">*pvector* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64f34-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f34-112">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="64f34-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="64f34-113">Array von 4D-Gleit Komma Vektoren.</span><span class="sxs-lookup"><span data-stu-id="64f34-113">Array of 4D floating point vectors.</span></span>

</dd> <dt>

<span data-ttu-id="64f34-114">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64f34-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f34-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64f34-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64f34-116">Anzahl der Vektoren im Array.</span><span class="sxs-lookup"><span data-stu-id="64f34-116">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64f34-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64f34-117">Return value</span></span>

<span data-ttu-id="64f34-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="64f34-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="64f34-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="64f34-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="64f34-120">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="64f34-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="64f34-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64f34-121">Remarks</span></span>

<span data-ttu-id="64f34-122">Wenn die Ziel Vektoren kleiner als die Quell Vektoren sind, werden die zusätzlichen Komponenten der Quell Vektoren ignoriert.</span><span class="sxs-lookup"><span data-stu-id="64f34-122">If the destination vectors are smaller than the source vectors, the additional components of the source vectors will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="64f34-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64f34-123">Requirements</span></span>



| <span data-ttu-id="64f34-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64f34-124">Requirement</span></span> | <span data-ttu-id="64f34-125">Wert</span><span class="sxs-lookup"><span data-stu-id="64f34-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="64f34-126">Header</span><span class="sxs-lookup"><span data-stu-id="64f34-126">Header</span></span><br/>  | <dl> <span data-ttu-id="64f34-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="64f34-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="64f34-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="64f34-128">Library</span></span><br/> | <dl> <span data-ttu-id="64f34-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64f34-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="64f34-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64f34-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64f34-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="64f34-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="64f34-132">**Getvector Array**</span><span class="sxs-lookup"><span data-stu-id="64f34-132">**GetVectorArray**</span></span>](id3dxbaseeffect--getvectorarray.md)
</dt> </dl>

 

 
