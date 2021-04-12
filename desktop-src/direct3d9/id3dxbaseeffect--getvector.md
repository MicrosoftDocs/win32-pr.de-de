---
description: Ruft einen Vektor ab.
ms.assetid: 55f5512f-42f2-4588-abd4-1cdea530b9bf
title: 'ID3DXBaseEffect:: getvector-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVector
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ea50cb6bf8c3f5b08d408539eba6c9f7cb09efc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354127"
---
# <a name="id3dxbaseeffectgetvector-method"></a><span data-ttu-id="07e15-103">ID3DXBaseEffect:: getvector-Methode</span><span class="sxs-lookup"><span data-stu-id="07e15-103">ID3DXBaseEffect::GetVector method</span></span>

<span data-ttu-id="07e15-104">Ruft einen Vektor ab.</span><span class="sxs-lookup"><span data-stu-id="07e15-104">Gets a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="07e15-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="07e15-105">Syntax</span></span>


```C++
HRESULT GetVector(
  [in]  D3DXHANDLE  hParameter,
  [out] D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="07e15-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="07e15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07e15-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07e15-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07e15-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="07e15-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="07e15-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="07e15-109">Unique identifier.</span></span> <span data-ttu-id="07e15-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="07e15-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="07e15-111">*pvector* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="07e15-111">*pVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07e15-112">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="07e15-112">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="07e15-113">Gibt einen 4D-Vektor zurück.</span><span class="sxs-lookup"><span data-stu-id="07e15-113">Returns a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07e15-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07e15-114">Return value</span></span>

<span data-ttu-id="07e15-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="07e15-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="07e15-116">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="07e15-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="07e15-117">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="07e15-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="07e15-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07e15-118">Remarks</span></span>

<span data-ttu-id="07e15-119">Wenn der Ziel Vektor größer als der Quell Vektor ist, werden nur die ersten Komponenten des Ziel Vektors aufgefüllt, und die übrigen Komponenten werden auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="07e15-119">If the destination vector is larger than the source vector, only the initial components of the destination vector will be filled, and the remaining components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="07e15-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07e15-120">Requirements</span></span>



| <span data-ttu-id="07e15-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07e15-121">Requirement</span></span> | <span data-ttu-id="07e15-122">Wert</span><span class="sxs-lookup"><span data-stu-id="07e15-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="07e15-123">Header</span><span class="sxs-lookup"><span data-stu-id="07e15-123">Header</span></span><br/>  | <dl> <span data-ttu-id="07e15-124"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="07e15-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="07e15-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="07e15-125">Library</span></span><br/> | <dl> <span data-ttu-id="07e15-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07e15-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="07e15-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07e15-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07e15-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="07e15-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="07e15-129">**Setvector**</span><span class="sxs-lookup"><span data-stu-id="07e15-129">**SetVector**</span></span>](id3dxbaseeffect--setvector.md)
</dt> </dl>

 

 




