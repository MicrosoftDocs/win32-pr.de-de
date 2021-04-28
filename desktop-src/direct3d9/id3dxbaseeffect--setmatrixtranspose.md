---
description: 'ID3DXBaseEffect::SetMatrixTranspose-Methode: Legt eine transponierte Matrix fest.'
ms.assetid: d340b058-6ba5-43ec-b398-111064965730
title: ID3DXBaseEffect::SetMatrixTranspose-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 384d4a7ed5e1b769218b9290ed6cc0f7f060bd66
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107398"
---
# <a name="id3dxbaseeffectsetmatrixtranspose-method"></a><span data-ttu-id="2ef23-103">ID3DXBaseEffect::SetMatrixTranspose-Methode</span><span class="sxs-lookup"><span data-stu-id="2ef23-103">ID3DXBaseEffect::SetMatrixTranspose method</span></span>

<span data-ttu-id="2ef23-104">Legt eine transponierte Matrix fest.</span><span class="sxs-lookup"><span data-stu-id="2ef23-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ef23-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ef23-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="2ef23-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ef23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ef23-107">*hParameter* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2ef23-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef23-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2ef23-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2ef23-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="2ef23-109">Unique identifier.</span></span> <span data-ttu-id="2ef23-110">Siehe [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2ef23-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ef23-111">*pMatrix* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2ef23-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef23-112">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2ef23-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2ef23-113">Zeiger auf eine transponierte Matrix.</span><span class="sxs-lookup"><span data-stu-id="2ef23-113">Pointer to a transposed matrix.</span></span> <span data-ttu-id="2ef23-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="2ef23-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ef23-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ef23-115">Return value</span></span>

<span data-ttu-id="2ef23-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2ef23-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2ef23-117">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2ef23-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2ef23-118">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="2ef23-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ef23-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ef23-119">Remarks</span></span>

<span data-ttu-id="2ef23-120">Eine transponierte Matrix enthält Spaltenhauptdaten. Das heißt, jeder Vektor ist in einer Spalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="2ef23-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="2ef23-121">Wenn die Zielmatrix kleiner als die Quellmatrix ist, werden die zusätzlichen Komponenten der Quellmatrix ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2ef23-121">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ef23-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ef23-122">Requirements</span></span>



| <span data-ttu-id="2ef23-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ef23-123">Requirement</span></span> | <span data-ttu-id="2ef23-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2ef23-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ef23-125">Header</span><span class="sxs-lookup"><span data-stu-id="2ef23-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2ef23-126"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="2ef23-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2ef23-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2ef23-127">Library</span></span><br/> | <dl> <span data-ttu-id="2ef23-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ef23-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2ef23-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2ef23-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ef23-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="2ef23-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="2ef23-131">**GetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="2ef23-131">**GetMatrixTranspose**</span></span>](id3dxbaseeffect--getmatrixtranspose.md)
</dt> </dl>

 

 




