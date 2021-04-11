---
description: Ruft ein Array von Zeigern auf umgesetzte Matrizen ab.
ms.assetid: b859ff2f-cf62-4619-b8be-b940fa0513b3
title: 'ID3DXBaseEffect:: getmatrixtranspotarpointerarray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTransposePointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e69c01395582691e6fdd0a695991ff1f726a362b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219695"
---
# <a name="id3dxbaseeffectgetmatrixtransposepointerarray-method"></a><span data-ttu-id="dab75-103">ID3DXBaseEffect:: getmatrixtranspotarpointerarray-Methode</span><span class="sxs-lookup"><span data-stu-id="dab75-103">ID3DXBaseEffect::GetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="dab75-104">Ruft ein Array von Zeigern auf umgesetzte Matrizen ab.</span><span class="sxs-lookup"><span data-stu-id="dab75-104">Gets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="dab75-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dab75-105">Syntax</span></span>


```C++
HRESULT GetMatrixTransposePointerArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX **ppMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="dab75-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dab75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dab75-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dab75-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dab75-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="dab75-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="dab75-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="dab75-109">Unique identifier.</span></span> <span data-ttu-id="dab75-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="dab75-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="dab75-111">*ppmatrix* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dab75-111">*ppMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dab75-112">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="dab75-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="dab75-113">Array von Zeigern auf umgesetzte Matrizen.</span><span class="sxs-lookup"><span data-stu-id="dab75-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="dab75-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="dab75-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="dab75-115">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dab75-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dab75-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dab75-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dab75-117">Anzahl von Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="dab75-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dab75-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dab75-118">Return value</span></span>

<span data-ttu-id="dab75-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dab75-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dab75-120">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dab75-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dab75-121">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="dab75-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="dab75-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dab75-122">Remarks</span></span>

<span data-ttu-id="dab75-123">Eine umgesetzte Matrix enthält Spalten Hauptdaten. Das heißt, jeder Vektor ist in einer Spalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="dab75-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="dab75-124">Wenn die Ziel Matrizen größer als die Quell Matrizen sind, werden nur die linken oberen Komponenten der einzelnen Ziel Matrix gefüllt, und die restlichen Ziel Matrixkomponenten werden auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dab75-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="dab75-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dab75-125">Requirements</span></span>



| <span data-ttu-id="dab75-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dab75-126">Requirement</span></span> | <span data-ttu-id="dab75-127">Wert</span><span class="sxs-lookup"><span data-stu-id="dab75-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dab75-128">Header</span><span class="sxs-lookup"><span data-stu-id="dab75-128">Header</span></span><br/>  | <dl> <span data-ttu-id="dab75-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="dab75-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="dab75-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dab75-130">Library</span></span><br/> | <dl> <span data-ttu-id="dab75-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dab75-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="dab75-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dab75-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dab75-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="dab75-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="dab75-134">**Getmatrixtransposearray**</span><span class="sxs-lookup"><span data-stu-id="dab75-134">**GetMatrixTransposeArray**</span></span>](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
