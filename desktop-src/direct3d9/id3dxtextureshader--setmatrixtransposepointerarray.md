---
description: Legt ein Array von Zeigern auf umgesetzte Matrizen fest.
ms.assetid: 2b9f1efe-b2ea-416b-a370-202db57b1925
title: 'ID3DXTextureShader:: setmatrixtransposepointerarray-Methode (D3DX9Shader. h)'
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
ms.openlocfilehash: cd7c81dcb0fd9b9354c2536a91abaebfe8e4315b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365099"
---
# <a name="id3dxtextureshadersetmatrixtransposepointerarray-method"></a><span data-ttu-id="b9347-103">ID3DXTextureShader:: setmatrixtransposepointerarray-Methode</span><span class="sxs-lookup"><span data-stu-id="b9347-103">ID3DXTextureShader::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="b9347-104">Legt ein Array von Zeigern auf umgesetzte Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="b9347-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9347-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9347-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="b9347-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9347-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9347-107">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9347-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9347-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b9347-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b9347-109">Eindeutiger Bezeichner für das Array von Matrix Konstanten.</span><span class="sxs-lookup"><span data-stu-id="b9347-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="b9347-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="b9347-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9347-111">*ppmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9347-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9347-112">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="b9347-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="b9347-113">Array von Zeigern auf umgesetzte Matrizen.</span><span class="sxs-lookup"><span data-stu-id="b9347-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="b9347-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="b9347-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9347-115">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9347-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9347-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9347-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b9347-117">Anzahl von Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="b9347-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9347-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9347-118">Return value</span></span>

<span data-ttu-id="b9347-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b9347-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b9347-120">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b9347-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b9347-121">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="b9347-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9347-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9347-122">Remarks</span></span>

<span data-ttu-id="b9347-123">Eine umgesetzte Matrix enthält Spalten Hauptdaten. Das heißt, jeder Vektor ist in einer Spalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="b9347-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9347-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9347-124">Requirements</span></span>



| <span data-ttu-id="b9347-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9347-125">Requirement</span></span> | <span data-ttu-id="b9347-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b9347-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9347-127">Header</span><span class="sxs-lookup"><span data-stu-id="b9347-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b9347-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9347-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b9347-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b9347-129">Library</span></span><br/> | <dl> <span data-ttu-id="b9347-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9347-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b9347-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9347-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9347-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="b9347-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
