---
description: 'ID3DXTextureShader::SetMatrixTransposePointerArray-Methode: Legt ein Array von Zeigern auf transponierte Matrizen fest.'
ms.assetid: 2b9f1efe-b2ea-416b-a370-202db57b1925
title: ID3DXTextureShader::SetMatrixTransposePointerArray-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 46e04c8c86bd0cdf7acea44872d00ad19f620ee6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090148"
---
# <a name="id3dxtextureshadersetmatrixtransposepointerarray-method"></a><span data-ttu-id="19e60-103">ID3DXTextureShader::SetMatrixTransposePointerArray-Methode</span><span class="sxs-lookup"><span data-stu-id="19e60-103">ID3DXTextureShader::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="19e60-104">Legt ein Array von Zeigern auf transponierte Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="19e60-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="19e60-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="19e60-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="19e60-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="19e60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19e60-107">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="19e60-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19e60-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="19e60-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="19e60-109">Eindeutiger Bezeichner für das Array von Matrixkonstanten.</span><span class="sxs-lookup"><span data-stu-id="19e60-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="19e60-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="19e60-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="19e60-111">*ppMatrix* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="19e60-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19e60-112">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="19e60-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="19e60-113">Array von Zeigern auf transponierte Matrizen.</span><span class="sxs-lookup"><span data-stu-id="19e60-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="19e60-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="19e60-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="19e60-115">*Anzahl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="19e60-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19e60-116">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19e60-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19e60-117">Anzahl der Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="19e60-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19e60-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19e60-118">Return value</span></span>

<span data-ttu-id="19e60-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19e60-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19e60-120">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="19e60-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="19e60-121">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="19e60-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="19e60-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19e60-122">Remarks</span></span>

<span data-ttu-id="19e60-123">Eine transponierte Matrix enthält Spaltenhauptdaten. Das heißt, jeder Vektor ist in einer Spalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="19e60-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="19e60-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19e60-124">Requirements</span></span>



| <span data-ttu-id="19e60-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19e60-125">Requirement</span></span> | <span data-ttu-id="19e60-126">Wert</span><span class="sxs-lookup"><span data-stu-id="19e60-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="19e60-127">Header</span><span class="sxs-lookup"><span data-stu-id="19e60-127">Header</span></span><br/>  | <dl> <span data-ttu-id="19e60-128"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="19e60-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="19e60-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="19e60-129">Library</span></span><br/> | <dl> <span data-ttu-id="19e60-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="19e60-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="19e60-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="19e60-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19e60-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="19e60-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
