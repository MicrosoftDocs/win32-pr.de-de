---
description: Legt ein Array von umsetzten Matrizen fest.
ms.assetid: 5dc65424-b0cd-490d-900e-60b9f7536ace
title: 'ID3DXBaseEffect:: setmatrixtransposearray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTransposeArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e646761435f75688fe652683281297ca2b8de99e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350702"
---
# <a name="id3dxbaseeffectsetmatrixtransposearray-method"></a><span data-ttu-id="33e5e-103">ID3DXBaseEffect:: setmatrixtransposearray-Methode</span><span class="sxs-lookup"><span data-stu-id="33e5e-103">ID3DXBaseEffect::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="33e5e-104">Legt ein Array von umsetzten Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="33e5e-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="33e5e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="33e5e-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="33e5e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="33e5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33e5e-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33e5e-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33e5e-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="33e5e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="33e5e-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="33e5e-109">Unique identifier.</span></span> <span data-ttu-id="33e5e-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="33e5e-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="33e5e-111">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33e5e-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33e5e-112">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="33e5e-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="33e5e-113">Array der übersetzten Matrizen.</span><span class="sxs-lookup"><span data-stu-id="33e5e-113">Array of transposed matrices.</span></span> <span data-ttu-id="33e5e-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="33e5e-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="33e5e-115">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33e5e-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33e5e-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33e5e-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33e5e-117">Anzahl von Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="33e5e-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33e5e-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33e5e-118">Return value</span></span>

<span data-ttu-id="33e5e-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="33e5e-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="33e5e-120">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="33e5e-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="33e5e-121">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="33e5e-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="33e5e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33e5e-122">Remarks</span></span>

<span data-ttu-id="33e5e-123">Eine umgesetzte Matrix enthält Spalten Hauptdaten. Das heißt, jeder Vektor ist in einer Spalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="33e5e-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="33e5e-124">Wenn die Ziel Matrizen kleiner als die Quell Matrizen sind, werden die zusätzlichen Komponenten der Quell Matrizen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="33e5e-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="33e5e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33e5e-125">Requirements</span></span>



| <span data-ttu-id="33e5e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33e5e-126">Requirement</span></span> | <span data-ttu-id="33e5e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="33e5e-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="33e5e-128">Header</span><span class="sxs-lookup"><span data-stu-id="33e5e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="33e5e-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="33e5e-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="33e5e-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="33e5e-130">Library</span></span><br/> | <dl> <span data-ttu-id="33e5e-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33e5e-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="33e5e-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33e5e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33e5e-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="33e5e-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="33e5e-134">**Getmatrixtransposearray**</span><span class="sxs-lookup"><span data-stu-id="33e5e-134">**GetMatrixTransposeArray**</span></span>](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
