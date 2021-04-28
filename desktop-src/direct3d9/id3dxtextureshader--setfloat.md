---
description: 'ID3DXTextureShader::SetFloat-Methode: Legt eine Gleitkommazahl fest.'
ms.assetid: 69bb9b15-5d66-4b1a-9559-29bcb38a965f
title: ID3DXTextureShader::SetFloat-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6230b0736cb3bc623b0413f7b5a1cb9635f00e07
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107168"
---
# <a name="id3dxtextureshadersetfloat-method"></a><span data-ttu-id="6899a-103">ID3DXTextureShader::SetFloat-Methode</span><span class="sxs-lookup"><span data-stu-id="6899a-103">ID3DXTextureShader::SetFloat method</span></span>

<span data-ttu-id="6899a-104">Legt eine Gleitkommazahl fest.</span><span class="sxs-lookup"><span data-stu-id="6899a-104">Sets a floating-point number.</span></span>

## <a name="syntax"></a><span data-ttu-id="6899a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6899a-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] D3DXHANDLE hConstant,
  [in] FLOAT      f
);
```



## <a name="parameters"></a><span data-ttu-id="6899a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6899a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6899a-107">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6899a-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6899a-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6899a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6899a-109">Eindeutiger Bezeichner für die Konstante.</span><span class="sxs-lookup"><span data-stu-id="6899a-109">Unique identifier to the constant.</span></span> <span data-ttu-id="6899a-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="6899a-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="6899a-111">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6899a-111">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6899a-112">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6899a-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6899a-113">Gleitkommazahl.</span><span class="sxs-lookup"><span data-stu-id="6899a-113">Floating-point number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6899a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6899a-114">Return value</span></span>

<span data-ttu-id="6899a-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6899a-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6899a-116">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6899a-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6899a-117">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="6899a-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6899a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6899a-118">Requirements</span></span>



| <span data-ttu-id="6899a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6899a-119">Requirement</span></span> | <span data-ttu-id="6899a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="6899a-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6899a-121">Header</span><span class="sxs-lookup"><span data-stu-id="6899a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6899a-122"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="6899a-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6899a-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6899a-123">Library</span></span><br/> | <dl> <span data-ttu-id="6899a-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6899a-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6899a-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6899a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6899a-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="6899a-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
