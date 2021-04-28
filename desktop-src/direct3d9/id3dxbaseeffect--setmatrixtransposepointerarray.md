---
description: 'ID3DXBaseEffect::SetMatrixTransposePointerArray-Methode: Legt ein Array von Zeigern auf transponierte Matrizen fest.'
ms.assetid: 11a21077-eeee-4d52-ac16-41444e3eca4f
title: ID3DXBaseEffect::SetMatrixTransposePointerArray-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3f35afad1120a26a60f670d12410584b2f9db7f1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107388"
---
# <a name="id3dxbaseeffectsetmatrixtransposepointerarray-method"></a><span data-ttu-id="ead05-103">ID3DXBaseEffect::SetMatrixTransposePointerArray-Methode</span><span class="sxs-lookup"><span data-stu-id="ead05-103">ID3DXBaseEffect::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="ead05-104">Legt ein Array von Zeigern auf transponierte Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="ead05-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="ead05-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ead05-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="ead05-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ead05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ead05-107">*hParameter* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ead05-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ead05-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ead05-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ead05-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="ead05-109">Unique identifier.</span></span> <span data-ttu-id="ead05-110">Siehe [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="ead05-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="ead05-111">*ppMatrix* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ead05-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ead05-112">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="ead05-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="ead05-113">Array von Zeigern auf transponierte Matrizen.</span><span class="sxs-lookup"><span data-stu-id="ead05-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="ead05-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="ead05-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="ead05-115">*Anzahl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ead05-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ead05-116">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ead05-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ead05-117">Anzahl der Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="ead05-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ead05-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ead05-118">Return value</span></span>

<span data-ttu-id="ead05-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ead05-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ead05-120">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ead05-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ead05-121">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="ead05-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ead05-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ead05-122">Remarks</span></span>

<span data-ttu-id="ead05-123">Eine transponierte Matrix enthält Spaltenhauptdaten. Das heißt, jeder Vektor ist in einer Spalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="ead05-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="ead05-124">Wenn die Zielmatrizen kleiner als die Quellmatrizen sind, werden die zusätzlichen Komponenten der Quellmatrizen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ead05-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="ead05-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ead05-125">Requirements</span></span>



| <span data-ttu-id="ead05-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ead05-126">Requirement</span></span> | <span data-ttu-id="ead05-127">Wert</span><span class="sxs-lookup"><span data-stu-id="ead05-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ead05-128">Header</span><span class="sxs-lookup"><span data-stu-id="ead05-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ead05-129"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="ead05-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ead05-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ead05-130">Library</span></span><br/> | <dl> <span data-ttu-id="ead05-131"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ead05-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ead05-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ead05-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ead05-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="ead05-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="ead05-134">**GetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="ead05-134">**GetMatrixTransposeArray**</span></span>](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
