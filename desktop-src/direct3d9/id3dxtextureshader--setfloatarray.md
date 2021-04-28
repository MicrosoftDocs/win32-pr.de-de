---
description: 'ID3DXTextureShader::SetFloatArray-Methode: Legt ein Array von Gleitkommazahlen fest.'
ms.assetid: 8e64b569-a6bf-4925-9d21-4df0b6661ee2
title: ID3DXTextureShader::SetFloatArray-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetFloatArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd42455e16cbfc203f76de868a82935e0e25401f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090248"
---
# <a name="id3dxtextureshadersetfloatarray-method"></a><span data-ttu-id="deff2-103">ID3DXTextureShader::SetFloatArray-Methode</span><span class="sxs-lookup"><span data-stu-id="deff2-103">ID3DXTextureShader::SetFloatArray method</span></span>

<span data-ttu-id="deff2-104">Legt ein Array von Gleitkommazahlen fest.</span><span class="sxs-lookup"><span data-stu-id="deff2-104">Sets an array of floating-point numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="deff2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="deff2-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hConstant,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="deff2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="deff2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deff2-107">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="deff2-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deff2-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="deff2-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="deff2-109">Eindeutiger Bezeichner für das Array von Konstanten.</span><span class="sxs-lookup"><span data-stu-id="deff2-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="deff2-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="deff2-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="deff2-111">*pf* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="deff2-111">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deff2-112">Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="deff2-112">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="deff2-113">Array von Gleitkommazahlen.</span><span class="sxs-lookup"><span data-stu-id="deff2-113">Array of floating-point numbers.</span></span>

</dd> <dt>

<span data-ttu-id="deff2-114">*Anzahl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="deff2-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deff2-115">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="deff2-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="deff2-116">Anzahl der Gleitkommawerte im Array.</span><span class="sxs-lookup"><span data-stu-id="deff2-116">Number of floating-point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deff2-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="deff2-117">Return value</span></span>

<span data-ttu-id="deff2-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="deff2-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="deff2-119">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="deff2-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="deff2-120">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="deff2-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="deff2-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="deff2-121">Requirements</span></span>



| <span data-ttu-id="deff2-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="deff2-122">Requirement</span></span> | <span data-ttu-id="deff2-123">Wert</span><span class="sxs-lookup"><span data-stu-id="deff2-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="deff2-124">Header</span><span class="sxs-lookup"><span data-stu-id="deff2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="deff2-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="deff2-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="deff2-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="deff2-126">Library</span></span><br/> | <dl> <span data-ttu-id="deff2-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="deff2-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="deff2-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="deff2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deff2-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="deff2-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
