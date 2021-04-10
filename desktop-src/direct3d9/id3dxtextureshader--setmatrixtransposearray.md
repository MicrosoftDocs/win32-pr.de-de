---
description: Legt ein Array von umsetzten Matrizen fest.
ms.assetid: 100288f2-44f0-4e75-bffb-78732c50a55c
title: 'ID3DXTextureShader:: setmatrixtransposearray-Methode (D3DX9Shader. h)'
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
ms.openlocfilehash: c9efd0c81cef8a72880a9755ca40e4dd8b4950ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961580"
---
# <a name="id3dxtextureshadersetmatrixtransposearray-method"></a><span data-ttu-id="c744d-103">ID3DXTextureShader:: setmatrixtransposearray-Methode</span><span class="sxs-lookup"><span data-stu-id="c744d-103">ID3DXTextureShader::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="c744d-104">Legt ein Array von umsetzten Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="c744d-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="c744d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c744d-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="c744d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c744d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c744d-107">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c744d-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c744d-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c744d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c744d-109">Eindeutiger Bezeichner für das Array von Matrix Konstanten.</span><span class="sxs-lookup"><span data-stu-id="c744d-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="c744d-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="c744d-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="c744d-111">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c744d-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c744d-112">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c744d-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c744d-113">Array der übersetzten Matrizen.</span><span class="sxs-lookup"><span data-stu-id="c744d-113">Array of transposed matrices.</span></span> <span data-ttu-id="c744d-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="c744d-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="c744d-115">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c744d-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c744d-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c744d-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c744d-117">Anzahl von Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="c744d-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c744d-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c744d-118">Return value</span></span>

<span data-ttu-id="c744d-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c744d-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c744d-120">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c744d-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c744d-121">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="c744d-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c744d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c744d-122">Remarks</span></span>

<span data-ttu-id="c744d-123">Eine umgesetzte Matrix enthält Spalten Hauptdaten. Das heißt, jeder Vektor ist in einer Spalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="c744d-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="c744d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c744d-124">Requirements</span></span>



| <span data-ttu-id="c744d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c744d-125">Requirement</span></span> | <span data-ttu-id="c744d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c744d-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c744d-127">Header</span><span class="sxs-lookup"><span data-stu-id="c744d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c744d-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c744d-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c744d-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c744d-129">Library</span></span><br/> | <dl> <span data-ttu-id="c744d-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c744d-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c744d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c744d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c744d-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="c744d-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
