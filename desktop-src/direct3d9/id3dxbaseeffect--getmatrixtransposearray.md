---
description: Ruft ein Array der übersetzten Matrizen ab.
ms.assetid: fbfcb2e4-82ca-4f79-923e-35749c5b9586
title: 'ID3DXBaseEffect:: getmatrixtransposearray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTransposeArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c5f3709a31067b82e9752a9e97db6f3a2a323a19
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762357"
---
# <a name="id3dxbaseeffectgetmatrixtransposearray-method"></a><span data-ttu-id="c7a5e-103">ID3DXBaseEffect:: getmatrixtransposearray-Methode</span><span class="sxs-lookup"><span data-stu-id="c7a5e-103">ID3DXBaseEffect::GetMatrixTransposeArray method</span></span>

<span data-ttu-id="c7a5e-104">Ruft ein Array der übersetzten Matrizen ab.</span><span class="sxs-lookup"><span data-stu-id="c7a5e-104">Gets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7a5e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7a5e-105">Syntax</span></span>


```C++
HRESULT GetMatrixTransposeArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="c7a5e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7a5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7a5e-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7a5e-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7a5e-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c7a5e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c7a5e-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="c7a5e-109">Unique identifier.</span></span> <span data-ttu-id="c7a5e-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="c7a5e-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a5e-111">*pmatrix* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c7a5e-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7a5e-112">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c7a5e-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c7a5e-113">Gibt ein Array der übersetzten Matrizen zurück.</span><span class="sxs-lookup"><span data-stu-id="c7a5e-113">Returns an array of transposed matrices.</span></span> <span data-ttu-id="c7a5e-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="c7a5e-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a5e-115">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7a5e-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7a5e-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7a5e-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c7a5e-117">Anzahl von Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="c7a5e-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7a5e-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7a5e-118">Return value</span></span>

<span data-ttu-id="c7a5e-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c7a5e-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c7a5e-120">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c7a5e-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c7a5e-121">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="c7a5e-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7a5e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7a5e-122">Remarks</span></span>

<span data-ttu-id="c7a5e-123">Eine umgesetzte Matrix enthält Spalten Hauptdaten. Das heißt, jeder Vektor ist in einer Spalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7a5e-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="c7a5e-124">Wenn die Ziel Matrizen größer als die Quell Matrizen sind, werden nur die linken oberen Komponenten der einzelnen Ziel Matrix gefüllt, und die restlichen Ziel Matrixkomponenten werden auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c7a5e-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7a5e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7a5e-125">Requirements</span></span>



| <span data-ttu-id="c7a5e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7a5e-126">Requirement</span></span> | <span data-ttu-id="c7a5e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c7a5e-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7a5e-128">Header</span><span class="sxs-lookup"><span data-stu-id="c7a5e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c7a5e-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7a5e-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c7a5e-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c7a5e-130">Library</span></span><br/> | <dl> <span data-ttu-id="c7a5e-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7a5e-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c7a5e-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7a5e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7a5e-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="c7a5e-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="c7a5e-134">**Setmatrixtransposearray**</span><span class="sxs-lookup"><span data-stu-id="c7a5e-134">**SetMatrixTransposeArray**</span></span>](id3dxbaseeffect--setmatrixtransposearray.md)
</dt> </dl>

 

 
