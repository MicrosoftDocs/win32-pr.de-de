---
description: Legt einen Vektor fest.
ms.assetid: 7dae88fc-d5d3-4751-859a-fa1bde4d0ce8
title: 'ID3DXBaseEffect:: setvector-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetVector
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5d6fccc24410e06dd9bb4e6b0b1f1c36b03dd355
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363187"
---
# <a name="id3dxbaseeffectsetvector-method"></a><span data-ttu-id="de305-103">ID3DXBaseEffect:: setvector-Methode</span><span class="sxs-lookup"><span data-stu-id="de305-103">ID3DXBaseEffect::SetVector method</span></span>

<span data-ttu-id="de305-104">Legt einen Vektor fest.</span><span class="sxs-lookup"><span data-stu-id="de305-104">Sets a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="de305-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="de305-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       D3DXHANDLE  hParameter,
  [in] const D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="de305-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="de305-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de305-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de305-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de305-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="de305-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="de305-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="de305-109">Unique identifier.</span></span> <span data-ttu-id="de305-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="de305-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="de305-111">*pvector* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de305-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de305-112">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="de305-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="de305-113">Zeiger auf einen 4D-Vektor.</span><span class="sxs-lookup"><span data-stu-id="de305-113">Pointer to a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de305-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de305-114">Return value</span></span>

<span data-ttu-id="de305-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="de305-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="de305-116">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="de305-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="de305-117">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="de305-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="de305-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de305-118">Remarks</span></span>

<span data-ttu-id="de305-119">Wenn der Ziel Vektor kleiner als der Quell Vektor ist, werden die zusätzlichen Komponenten des Quell Vektors ignoriert.</span><span class="sxs-lookup"><span data-stu-id="de305-119">If the destination vector is smaller than the source vector, the additional components of the source vector will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="de305-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de305-120">Requirements</span></span>



| <span data-ttu-id="de305-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de305-121">Requirement</span></span> | <span data-ttu-id="de305-122">Wert</span><span class="sxs-lookup"><span data-stu-id="de305-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de305-123">Header</span><span class="sxs-lookup"><span data-stu-id="de305-123">Header</span></span><br/>  | <dl> <span data-ttu-id="de305-124"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="de305-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="de305-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="de305-125">Library</span></span><br/> | <dl> <span data-ttu-id="de305-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de305-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="de305-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de305-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de305-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="de305-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="de305-129">**Getvector**</span><span class="sxs-lookup"><span data-stu-id="de305-129">**GetVector**</span></span>](id3dxbaseeffect--getvector.md)
</dt> </dl>

 

 




