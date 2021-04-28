---
description: 'ID3DXTextureShader::SetMatrixTransposeArray-Methode: Legt ein Array von transponierten Matrizen fest.'
ms.assetid: 100288f2-44f0-4e75-bffb-78732c50a55c
title: ID3DXTextureShader::SetMatrixTransposeArray-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTransposeArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 663f49f600c000ff37974c8ecd4da56ba59630d1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090208"
---
# <a name="id3dxtextureshadersetmatrixtransposearray-method"></a><span data-ttu-id="ae4bd-103">ID3DXTextureShader::SetMatrixTransposeArray-Methode</span><span class="sxs-lookup"><span data-stu-id="ae4bd-103">ID3DXTextureShader::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="ae4bd-104">Legt ein Array transponierte Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="ae4bd-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae4bd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae4bd-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="ae4bd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae4bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae4bd-107">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ae4bd-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae4bd-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ae4bd-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ae4bd-109">Eindeutiger Bezeichner für das Array von Matrixkonstatoren.</span><span class="sxs-lookup"><span data-stu-id="ae4bd-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="ae4bd-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="ae4bd-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae4bd-111">*pMatrix* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ae4bd-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae4bd-112">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="ae4bd-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ae4bd-113">Array transponierte Matrizen.</span><span class="sxs-lookup"><span data-stu-id="ae4bd-113">Array of transposed matrices.</span></span> <span data-ttu-id="ae4bd-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="ae4bd-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae4bd-115">*Anzahl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ae4bd-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae4bd-116">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae4bd-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae4bd-117">Anzahl der Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="ae4bd-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae4bd-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae4bd-118">Return value</span></span>

<span data-ttu-id="ae4bd-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ae4bd-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ae4bd-120">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ae4bd-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ae4bd-121">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="ae4bd-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae4bd-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae4bd-122">Remarks</span></span>

<span data-ttu-id="ae4bd-123">Eine transponierte Matrix enthält Spalten-Hauptdaten. Das heißt, jeder Vektor ist in einer Spalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="ae4bd-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae4bd-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae4bd-124">Requirements</span></span>



| <span data-ttu-id="ae4bd-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae4bd-125">Requirement</span></span> | <span data-ttu-id="ae4bd-126">Wert</span><span class="sxs-lookup"><span data-stu-id="ae4bd-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae4bd-127">Header</span><span class="sxs-lookup"><span data-stu-id="ae4bd-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ae4bd-128"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="ae4bd-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ae4bd-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ae4bd-129">Library</span></span><br/> | <dl> <span data-ttu-id="ae4bd-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae4bd-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ae4bd-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ae4bd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae4bd-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="ae4bd-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
