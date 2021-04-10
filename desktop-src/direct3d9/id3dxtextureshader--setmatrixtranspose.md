---
description: Legt eine übersetzte Matrix fest.
ms.assetid: 5339a9de-528f-4404-880b-73964192b766
title: 'ID3DXTextureShader:: setmatrixtransform-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTranspose
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf5507d935d2fea1b6210624e70344a2c4a1da81
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961620"
---
# <a name="id3dxtextureshadersetmatrixtranspose-method"></a><span data-ttu-id="3a014-103">ID3DXTextureShader:: setmatrixtransform-Methode</span><span class="sxs-lookup"><span data-stu-id="3a014-103">ID3DXTextureShader::SetMatrixTranspose method</span></span>

<span data-ttu-id="3a014-104">Legt eine übersetzte Matrix fest.</span><span class="sxs-lookup"><span data-stu-id="3a014-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a014-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a014-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="3a014-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a014-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a014-107">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a014-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a014-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="3a014-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="3a014-109">Eindeutiger Bezeichner für die Matrix der Konstanten.</span><span class="sxs-lookup"><span data-stu-id="3a014-109">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="3a014-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="3a014-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a014-111">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a014-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a014-112">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="3a014-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3a014-113">Zeiger auf eine umgesetzte Matrix.</span><span class="sxs-lookup"><span data-stu-id="3a014-113">Pointer to a transposed matrix.</span></span> <span data-ttu-id="3a014-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="3a014-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a014-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a014-115">Return value</span></span>

<span data-ttu-id="3a014-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3a014-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3a014-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3a014-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3a014-118">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="3a014-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a014-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a014-119">Remarks</span></span>

<span data-ttu-id="3a014-120">Eine umgesetzte Matrix enthält Spalten Hauptdaten. Das heißt, jeder Vektor ist in einer Spalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="3a014-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a014-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a014-121">Requirements</span></span>



| <span data-ttu-id="3a014-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a014-122">Requirement</span></span> | <span data-ttu-id="3a014-123">Wert</span><span class="sxs-lookup"><span data-stu-id="3a014-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a014-124">Header</span><span class="sxs-lookup"><span data-stu-id="3a014-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3a014-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a014-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="3a014-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3a014-126">Library</span></span><br/> | <dl> <span data-ttu-id="3a014-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a014-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3a014-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a014-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a014-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="3a014-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




