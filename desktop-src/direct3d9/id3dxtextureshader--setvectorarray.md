---
description: Legt ein Array von 4D-Vektoren fest.
ms.assetid: 45bc5cb1-b44a-468b-8c80-a639da8a033f
title: 'ID3DXTextureShader:: setvectorarray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetVectorArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c91a012cda9d1aa992682b5cb5aa769bf41de180
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370425"
---
# <a name="id3dxtextureshadersetvectorarray-method"></a><span data-ttu-id="c0b27-103">ID3DXTextureShader:: setvectorarray-Methode</span><span class="sxs-lookup"><span data-stu-id="c0b27-103">ID3DXTextureShader::SetVectorArray method</span></span>

<span data-ttu-id="c0b27-104">Legt ein Array von 4D-Vektoren fest.</span><span class="sxs-lookup"><span data-stu-id="c0b27-104">Sets an array of 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0b27-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0b27-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector,
  [in]       UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="c0b27-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0b27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0b27-107">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c0b27-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b27-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c0b27-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c0b27-109">Eindeutiger Bezeichner für das Array von Vektor Konstanten.</span><span class="sxs-lookup"><span data-stu-id="c0b27-109">Unique identifier to the array of vector constants.</span></span> <span data-ttu-id="c0b27-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="c0b27-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0b27-111">*pvector* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c0b27-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b27-112">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="c0b27-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c0b27-113">Array von 4D-Vektoren.</span><span class="sxs-lookup"><span data-stu-id="c0b27-113">Array of 4D vectors.</span></span> <span data-ttu-id="c0b27-114">Siehe [**D3DXVECTOR4**](d3dxvector4.md).</span><span class="sxs-lookup"><span data-stu-id="c0b27-114">See [**D3DXVECTOR4**](d3dxvector4.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0b27-115">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c0b27-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b27-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0b27-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c0b27-117">Anzahl der Vektoren im Array.</span><span class="sxs-lookup"><span data-stu-id="c0b27-117">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0b27-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0b27-118">Return value</span></span>

<span data-ttu-id="c0b27-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c0b27-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c0b27-120">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c0b27-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c0b27-121">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="c0b27-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0b27-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0b27-122">Requirements</span></span>



| <span data-ttu-id="c0b27-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0b27-123">Requirement</span></span> | <span data-ttu-id="c0b27-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c0b27-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b27-125">Header</span><span class="sxs-lookup"><span data-stu-id="c0b27-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c0b27-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0b27-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c0b27-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c0b27-127">Library</span></span><br/> | <dl> <span data-ttu-id="c0b27-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0b27-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c0b27-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0b27-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0b27-130">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="c0b27-130">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
