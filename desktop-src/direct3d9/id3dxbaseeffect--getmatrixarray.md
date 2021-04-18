---
description: Ruft ein Array von nicht umsetzten Matrizen ab.
ms.assetid: 37b08f55-22f1-4b60-8cd4-566a77e7dbd6
title: 'ID3DXBaseEffect:: getmatrixarray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 242b3c42976f9bfe4ad8ecad4d965c473839ffdd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365865"
---
# <a name="id3dxbaseeffectgetmatrixarray-method"></a><span data-ttu-id="02425-103">ID3DXBaseEffect:: getmatrixarray-Methode</span><span class="sxs-lookup"><span data-stu-id="02425-103">ID3DXBaseEffect::GetMatrixArray method</span></span>

<span data-ttu-id="02425-104">Ruft ein Array von nicht umsetzten Matrizen ab.</span><span class="sxs-lookup"><span data-stu-id="02425-104">Gets an array of nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="02425-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="02425-105">Syntax</span></span>


```C++
HRESULT GetMatrixArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="02425-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="02425-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02425-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02425-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02425-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="02425-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="02425-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="02425-109">Unique identifier.</span></span> <span data-ttu-id="02425-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="02425-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="02425-111">*pmatrix* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="02425-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02425-112">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="02425-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="02425-113">Gibt ein Array nicht umsetzbarer Matrizen zurück.</span><span class="sxs-lookup"><span data-stu-id="02425-113">Returns an array of nontransposed matrices.</span></span> <span data-ttu-id="02425-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="02425-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="02425-115">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02425-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02425-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02425-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02425-117">Anzahl von Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="02425-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02425-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02425-118">Return value</span></span>

<span data-ttu-id="02425-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="02425-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="02425-120">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="02425-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="02425-121">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="02425-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="02425-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02425-122">Remarks</span></span>

<span data-ttu-id="02425-123">Eine nicht umgesetzte Matrix enthält Zeilen Hauptdaten; Das heißt, jeder Vektor ist in einer Zeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="02425-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="02425-124">Wenn die Ziel Matrizen größer als die Quell Matrizen sind, werden nur die linken oberen Komponenten der einzelnen Ziel Matrix gefüllt, und die restlichen Ziel Matrixkomponenten werden auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="02425-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="02425-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02425-125">Requirements</span></span>



| <span data-ttu-id="02425-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02425-126">Requirement</span></span> | <span data-ttu-id="02425-127">Wert</span><span class="sxs-lookup"><span data-stu-id="02425-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="02425-128">Header</span><span class="sxs-lookup"><span data-stu-id="02425-128">Header</span></span><br/>  | <dl> <span data-ttu-id="02425-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="02425-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="02425-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="02425-130">Library</span></span><br/> | <dl> <span data-ttu-id="02425-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02425-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="02425-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02425-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02425-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="02425-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="02425-134">**Setmatrixarray**</span><span class="sxs-lookup"><span data-stu-id="02425-134">**SetMatrixArray**</span></span>](id3dxbaseeffect--setmatrixarray.md)
</dt> </dl>

 

 
