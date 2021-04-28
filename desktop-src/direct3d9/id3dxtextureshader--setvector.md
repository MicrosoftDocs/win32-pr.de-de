---
description: 'ID3DXTextureShader::SetVector-Methode: Legt einen 4D-Vektor fest.'
ms.assetid: befed2a8-7695-4f06-a6ee-aff466d1940a
title: ID3DXTextureShader::SetVector-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetVector
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e917e4ff13cf7c03de264542dc1995364f1dc526
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090158"
---
# <a name="id3dxtextureshadersetvector-method"></a><span data-ttu-id="8ae0f-103">ID3DXTextureShader::SetVector-Methode</span><span class="sxs-lookup"><span data-stu-id="8ae0f-103">ID3DXTextureShader::SetVector method</span></span>

<span data-ttu-id="8ae0f-104">Legt einen 4D-Vektor fest.</span><span class="sxs-lookup"><span data-stu-id="8ae0f-104">Sets a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ae0f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ae0f-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="8ae0f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ae0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ae0f-107">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8ae0f-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae0f-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae0f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8ae0f-109">Eindeutiger Bezeichner für die Vektorkonstante.</span><span class="sxs-lookup"><span data-stu-id="8ae0f-109">Unique identifier to the vector constant.</span></span> <span data-ttu-id="8ae0f-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="8ae0f-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ae0f-111">*pVector* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8ae0f-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae0f-112">Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="8ae0f-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8ae0f-113">Zeiger auf einen 4D-Vektor.</span><span class="sxs-lookup"><span data-stu-id="8ae0f-113">Pointer to a 4D vector.</span></span> <span data-ttu-id="8ae0f-114">Siehe [**D3DXVECTOR4.**](d3dxvector4.md)</span><span class="sxs-lookup"><span data-stu-id="8ae0f-114">See [**D3DXVECTOR4**](d3dxvector4.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ae0f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ae0f-115">Return value</span></span>

<span data-ttu-id="8ae0f-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8ae0f-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8ae0f-117">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8ae0f-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8ae0f-118">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="8ae0f-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ae0f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ae0f-119">Requirements</span></span>



| <span data-ttu-id="8ae0f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ae0f-120">Requirement</span></span> | <span data-ttu-id="8ae0f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8ae0f-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae0f-122">Header</span><span class="sxs-lookup"><span data-stu-id="8ae0f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8ae0f-123"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="8ae0f-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8ae0f-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8ae0f-124">Library</span></span><br/> | <dl> <span data-ttu-id="8ae0f-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ae0f-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8ae0f-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8ae0f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ae0f-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="8ae0f-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




