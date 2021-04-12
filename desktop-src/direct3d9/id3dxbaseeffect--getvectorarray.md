---
description: Ruft ein Array von Vektoren ab.
ms.assetid: 75fe454c-75f7-4f03-acd2-dd9cbf94fb96
title: 'ID3DXBaseEffect:: getvectorarray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVectorArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fa57553b993d5746b54e9a03c6b4e52f71937f0d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354126"
---
# <a name="id3dxbaseeffectgetvectorarray-method"></a><span data-ttu-id="c3174-103">ID3DXBaseEffect:: getvectorarray-Methode</span><span class="sxs-lookup"><span data-stu-id="c3174-103">ID3DXBaseEffect::GetVectorArray method</span></span>

<span data-ttu-id="c3174-104">Ruft ein Array von Vektoren ab.</span><span class="sxs-lookup"><span data-stu-id="c3174-104">Gets an array of vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3174-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3174-105">Syntax</span></span>


```C++
HRESULT GetVectorArray(
  [in]  D3DXHANDLE  hParameter,
  [out] D3DXVECTOR4 *pVector,
  [in]  UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="c3174-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3174-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3174-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3174-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3174-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c3174-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c3174-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="c3174-109">Unique identifier.</span></span> <span data-ttu-id="c3174-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="c3174-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3174-111">*pvector* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c3174-111">*pVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3174-112">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3174-112">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c3174-113">Gibt ein Array von 4D-Gleit Komma Vektoren zurück.</span><span class="sxs-lookup"><span data-stu-id="c3174-113">Returns an array of 4D floating point vectors.</span></span>

</dd> <dt>

<span data-ttu-id="c3174-114">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3174-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3174-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3174-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3174-116">Anzahl der Vektoren im Array.</span><span class="sxs-lookup"><span data-stu-id="c3174-116">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3174-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3174-117">Return value</span></span>

<span data-ttu-id="c3174-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c3174-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c3174-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c3174-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c3174-120">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="c3174-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3174-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3174-121">Remarks</span></span>

<span data-ttu-id="c3174-122">Wenn die Ziel Vektoren größer als die Quell Vektoren sind, werden nur die anfänglichen Komponenten der einzelnen Ziel Vektor gefüllt, und die restlichen Ziel Vektor Komponenten werden auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3174-122">If the destination vectors are larger than the source vectors, only the initial components of each destination vector will be filled, and the remaining destination vector components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3174-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3174-123">Requirements</span></span>



| <span data-ttu-id="c3174-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3174-124">Requirement</span></span> | <span data-ttu-id="c3174-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c3174-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3174-126">Header</span><span class="sxs-lookup"><span data-stu-id="c3174-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c3174-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3174-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c3174-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c3174-128">Library</span></span><br/> | <dl> <span data-ttu-id="c3174-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3174-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c3174-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3174-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3174-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="c3174-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="c3174-132">**Setvector Array**</span><span class="sxs-lookup"><span data-stu-id="c3174-132">**SetVectorArray**</span></span>](id3dxbaseeffect--setvectorarray.md)
</dt> </dl>

 

 
