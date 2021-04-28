---
description: 'ID3DXTextureShader::SetIntArray-Methode: Legt ein Array von ganzen Zahlen fest.'
ms.assetid: 1ceb8bb0-d168-49cf-8964-8ae582b5ec2e
title: ID3DXTextureShader::SetIntArray-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetIntArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ddc00637bddf2810e73be7755a9dcfb8696053e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097488"
---
# <a name="id3dxtextureshadersetintarray-method"></a><span data-ttu-id="cc056-103">ID3DXTextureShader::SetIntArray-Methode</span><span class="sxs-lookup"><span data-stu-id="cc056-103">ID3DXTextureShader::SetIntArray method</span></span>

<span data-ttu-id="cc056-104">Legt ein Array von ganzen Zahlen fest.</span><span class="sxs-lookup"><span data-stu-id="cc056-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc056-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc056-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hConstant,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="cc056-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc056-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc056-107">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="cc056-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc056-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="cc056-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="cc056-109">Eindeutiger Bezeichner für das Array von Konstanten.</span><span class="sxs-lookup"><span data-stu-id="cc056-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="cc056-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="cc056-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc056-111">*pn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="cc056-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc056-112">Typ: **const [**INT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="cc056-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cc056-113">Array von ganzen Zahlen.</span><span class="sxs-lookup"><span data-stu-id="cc056-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="cc056-114">*Anzahl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="cc056-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc056-115">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc056-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc056-116">Anzahl von ganzen Zahlen im Array.</span><span class="sxs-lookup"><span data-stu-id="cc056-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc056-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc056-117">Return value</span></span>

<span data-ttu-id="cc056-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cc056-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cc056-119">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cc056-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cc056-120">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="cc056-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc056-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc056-121">Requirements</span></span>



| <span data-ttu-id="cc056-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc056-122">Requirement</span></span> | <span data-ttu-id="cc056-123">Wert</span><span class="sxs-lookup"><span data-stu-id="cc056-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc056-124">Header</span><span class="sxs-lookup"><span data-stu-id="cc056-124">Header</span></span><br/>  | <dl> <span data-ttu-id="cc056-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="cc056-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="cc056-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cc056-126">Library</span></span><br/> | <dl> <span data-ttu-id="cc056-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc056-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cc056-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cc056-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc056-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="cc056-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
