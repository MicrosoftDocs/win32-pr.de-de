---
description: Legt ein Array von nicht übersetzten Matrizen fest.
ms.assetid: 27f230bd-9aee-4673-aa70-5ecda541b1be
title: 'ID3DXTextureShader:: setmatrixarray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b0545d48e16698f44cc48ad467f9454ac94db030
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363975"
---
# <a name="id3dxtextureshadersetmatrixarray-method"></a><span data-ttu-id="448c4-103">ID3DXTextureShader:: setmatrixarray-Methode</span><span class="sxs-lookup"><span data-stu-id="448c4-103">ID3DXTextureShader::SetMatrixArray method</span></span>

<span data-ttu-id="448c4-104">Legt ein Array von nicht übersetzten Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="448c4-104">Sets an array of non-transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="448c4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="448c4-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="448c4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="448c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="448c4-107">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="448c4-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="448c4-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="448c4-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="448c4-109">Eindeutiger Bezeichner für das Array konstanter Matrizen.</span><span class="sxs-lookup"><span data-stu-id="448c4-109">Unique identifier to the array of constant matrices.</span></span> <span data-ttu-id="448c4-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="448c4-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="448c4-111">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="448c4-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="448c4-112">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="448c4-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="448c4-113">Array von nicht übersetzten Matrizen.</span><span class="sxs-lookup"><span data-stu-id="448c4-113">Array of non-transposed matrices.</span></span> <span data-ttu-id="448c4-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="448c4-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="448c4-115">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="448c4-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="448c4-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="448c4-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="448c4-117">Anzahl von Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="448c4-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="448c4-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="448c4-118">Return value</span></span>

<span data-ttu-id="448c4-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="448c4-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="448c4-120">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="448c4-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="448c4-121">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="448c4-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="448c4-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="448c4-122">Remarks</span></span>

<span data-ttu-id="448c4-123">Eine nicht übersetzte Matrix enthält Zeilen Hauptdaten; Das heißt, jeder Vektor ist in einer Zeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="448c4-123">A non-transposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="448c4-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="448c4-124">Requirements</span></span>



| <span data-ttu-id="448c4-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="448c4-125">Requirement</span></span> | <span data-ttu-id="448c4-126">Wert</span><span class="sxs-lookup"><span data-stu-id="448c4-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="448c4-127">Header</span><span class="sxs-lookup"><span data-stu-id="448c4-127">Header</span></span><br/>  | <dl> <span data-ttu-id="448c4-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="448c4-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="448c4-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="448c4-129">Library</span></span><br/> | <dl> <span data-ttu-id="448c4-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="448c4-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="448c4-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="448c4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="448c4-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="448c4-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
