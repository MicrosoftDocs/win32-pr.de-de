---
description: Legt ein Array von Zeigern auf nicht übersetzte Matrizen fest.
ms.assetid: 5ad83abd-1895-4838-85b5-c437c23a3d91
title: 'ID3DXTextureShader:: setmatrixpointerarray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixPointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1bde5250ae8ceeab7522b9df15c99070e9471608
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354496"
---
# <a name="id3dxtextureshadersetmatrixpointerarray-method"></a><span data-ttu-id="ce56e-103">ID3DXTextureShader:: setmatrixpointerarray-Methode</span><span class="sxs-lookup"><span data-stu-id="ce56e-103">ID3DXTextureShader::SetMatrixPointerArray method</span></span>

<span data-ttu-id="ce56e-104">Legt ein Array von Zeigern auf nicht übersetzte Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="ce56e-104">Sets an array of pointers to non-transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce56e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce56e-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="ce56e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce56e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce56e-107">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce56e-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce56e-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ce56e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ce56e-109">Eindeutiger Bezeichner für ein Array konstanter Matrizen.</span><span class="sxs-lookup"><span data-stu-id="ce56e-109">Unique identifier to an array of constant matrices.</span></span> <span data-ttu-id="ce56e-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="ce56e-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce56e-111">*ppmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce56e-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce56e-112">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="ce56e-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="ce56e-113">Array von Zeigern auf nicht übersetzte Matrizen.</span><span class="sxs-lookup"><span data-stu-id="ce56e-113">Array of pointers to non-transposed matrices.</span></span> <span data-ttu-id="ce56e-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="ce56e-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce56e-115">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce56e-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce56e-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce56e-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce56e-117">Anzahl von Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="ce56e-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce56e-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce56e-118">Return value</span></span>

<span data-ttu-id="ce56e-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ce56e-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ce56e-120">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ce56e-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ce56e-121">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="ce56e-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce56e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce56e-122">Remarks</span></span>

<span data-ttu-id="ce56e-123">Eine nicht übersetzte Matrix enthält Zeilen Hauptdaten; Das heißt, jeder Vektor ist in einer Zeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="ce56e-123">A non-transposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce56e-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce56e-124">Requirements</span></span>



| <span data-ttu-id="ce56e-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce56e-125">Requirement</span></span> | <span data-ttu-id="ce56e-126">Wert</span><span class="sxs-lookup"><span data-stu-id="ce56e-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce56e-127">Header</span><span class="sxs-lookup"><span data-stu-id="ce56e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ce56e-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce56e-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ce56e-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ce56e-129">Library</span></span><br/> | <dl> <span data-ttu-id="ce56e-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce56e-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ce56e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce56e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce56e-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="ce56e-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
