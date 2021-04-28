---
description: 'ID3DXBaseEffect::SetMatrixArray-Methode: Legt ein Array von nicht übersetzten Matrizen fest.'
ms.assetid: 008de62c-3a36-4499-8a0b-9075756395e9
title: ID3DXBaseEffect::SetMatrixArray-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ae603708be4b34c9aa12722fe282df470c85d476
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107428"
---
# <a name="id3dxbaseeffectsetmatrixarray-method"></a><span data-ttu-id="c9eff-103">ID3DXBaseEffect::SetMatrixArray-Methode</span><span class="sxs-lookup"><span data-stu-id="c9eff-103">ID3DXBaseEffect::SetMatrixArray method</span></span>

<span data-ttu-id="c9eff-104">Legt ein Array von nicht transposierten Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="c9eff-104">Sets an array of nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9eff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9eff-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="c9eff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9eff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9eff-107">*hParameter* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c9eff-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9eff-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c9eff-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c9eff-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="c9eff-109">Unique identifier.</span></span> <span data-ttu-id="c9eff-110">Siehe [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="c9eff-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9eff-111">*pMatrix* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c9eff-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9eff-112">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c9eff-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c9eff-113">Array von nicht transposed Matrizen.</span><span class="sxs-lookup"><span data-stu-id="c9eff-113">Array of nontransposed matrices.</span></span> <span data-ttu-id="c9eff-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="c9eff-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9eff-115">*Anzahl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c9eff-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9eff-116">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9eff-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9eff-117">Anzahl der Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="c9eff-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9eff-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9eff-118">Return value</span></span>

<span data-ttu-id="c9eff-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c9eff-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c9eff-120">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c9eff-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c9eff-121">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="c9eff-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9eff-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9eff-122">Remarks</span></span>

<span data-ttu-id="c9eff-123">Eine nicht transposed Matrix enthält Zeilen-Hauptdaten. Das heißt, jeder Vektor ist in einer Zeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="c9eff-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="c9eff-124">Wenn die Zielmatrizen kleiner als die Quellmatrizen sind, werden die zusätzlichen Komponenten der Quellmatrizen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c9eff-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9eff-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9eff-125">Requirements</span></span>



| <span data-ttu-id="c9eff-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9eff-126">Requirement</span></span> | <span data-ttu-id="c9eff-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c9eff-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9eff-128">Header</span><span class="sxs-lookup"><span data-stu-id="c9eff-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c9eff-129"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="c9eff-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c9eff-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c9eff-130">Library</span></span><br/> | <dl> <span data-ttu-id="c9eff-131"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9eff-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c9eff-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c9eff-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9eff-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="c9eff-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="c9eff-134">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="c9eff-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
