---
description: Legt eine nicht übersetzte Matrix fest.
ms.assetid: 891441ea-09d5-43b6-a080-578d7f8e4586
title: 'ID3DXTextureShader:: setMatrix-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c52fa8d363200222197ac40563fb0dd66e71f7a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132313"
---
# <a name="id3dxtextureshadersetmatrix-method"></a><span data-ttu-id="cdae4-103">ID3DXTextureShader:: setMatrix-Methode</span><span class="sxs-lookup"><span data-stu-id="cdae4-103">ID3DXTextureShader::SetMatrix method</span></span>

<span data-ttu-id="cdae4-104">Legt eine nicht übersetzte Matrix fest.</span><span class="sxs-lookup"><span data-stu-id="cdae4-104">Sets a non-transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdae4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdae4-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="cdae4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdae4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdae4-107">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdae4-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdae4-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="cdae4-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="cdae4-109">Eindeutiger Bezeichner für die Matrix der Konstanten.</span><span class="sxs-lookup"><span data-stu-id="cdae4-109">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="cdae4-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="cdae4-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdae4-111">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdae4-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdae4-112">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="cdae4-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cdae4-113">Zeiger auf eine nicht durchgesetzte Matrix.</span><span class="sxs-lookup"><span data-stu-id="cdae4-113">Pointer to a non-transposed matrix.</span></span> <span data-ttu-id="cdae4-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="cdae4-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdae4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cdae4-115">Return value</span></span>

<span data-ttu-id="cdae4-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cdae4-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cdae4-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cdae4-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cdae4-118">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="cdae4-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdae4-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cdae4-119">Remarks</span></span>

<span data-ttu-id="cdae4-120">Eine nicht übersetzte Matrix enthält Zeilen Hauptdaten; Das heißt, jeder Vektor ist in einer Zeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="cdae4-120">A non-transposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdae4-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdae4-121">Requirements</span></span>



| <span data-ttu-id="cdae4-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cdae4-122">Requirement</span></span> | <span data-ttu-id="cdae4-123">Wert</span><span class="sxs-lookup"><span data-stu-id="cdae4-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdae4-124">Header</span><span class="sxs-lookup"><span data-stu-id="cdae4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="cdae4-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdae4-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="cdae4-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cdae4-126">Library</span></span><br/> | <dl> <span data-ttu-id="cdae4-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cdae4-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cdae4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdae4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdae4-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="cdae4-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




