---
description: Ruft eine umgesetzte Matrix ab.
ms.assetid: 255c1e20-0a60-49eb-abaa-66a67322ce73
title: 'ID3DXBaseEffect:: getmatrixtransform-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f52a7b528a7853278f5e1b902c3907e8d48fa40f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355887"
---
# <a name="id3dxbaseeffectgetmatrixtranspose-method"></a><span data-ttu-id="e95ce-103">ID3DXBaseEffect:: getmatrixtransform-Methode</span><span class="sxs-lookup"><span data-stu-id="e95ce-103">ID3DXBaseEffect::GetMatrixTranspose method</span></span>

<span data-ttu-id="e95ce-104">Ruft eine umgesetzte Matrix ab.</span><span class="sxs-lookup"><span data-stu-id="e95ce-104">Gets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e95ce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e95ce-105">Syntax</span></span>


```C++
HRESULT GetMatrixTranspose(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="e95ce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e95ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e95ce-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e95ce-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e95ce-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e95ce-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e95ce-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e95ce-109">Unique identifier.</span></span> <span data-ttu-id="e95ce-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="e95ce-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="e95ce-111">*pmatrix* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e95ce-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e95ce-112">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e95ce-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e95ce-113">Gibt eine umgesetzte Matrix zurück.</span><span class="sxs-lookup"><span data-stu-id="e95ce-113">Returns a transposed matrix.</span></span> <span data-ttu-id="e95ce-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="e95ce-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e95ce-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e95ce-115">Return value</span></span>

<span data-ttu-id="e95ce-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e95ce-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e95ce-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e95ce-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e95ce-118">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="e95ce-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e95ce-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e95ce-119">Remarks</span></span>

<span data-ttu-id="e95ce-120">Eine umgesetzte Matrix enthält Spalten Hauptdaten. Das heißt, jeder Vektor ist in einer Spalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="e95ce-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="e95ce-121">Wenn die Ziel Matrix größer als die Quell Matrix ist, werden nur die linken oberen Elemente der Ziel Matrix gefüllt, und die restlichen Ziel Matrixkomponenten werden auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e95ce-121">If the destination matrix is larger than the source matrix, only the upper-left elements of the destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="e95ce-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e95ce-122">Requirements</span></span>



| <span data-ttu-id="e95ce-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e95ce-123">Requirement</span></span> | <span data-ttu-id="e95ce-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e95ce-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e95ce-125">Header</span><span class="sxs-lookup"><span data-stu-id="e95ce-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e95ce-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e95ce-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e95ce-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e95ce-127">Library</span></span><br/> | <dl> <span data-ttu-id="e95ce-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e95ce-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e95ce-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e95ce-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e95ce-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="e95ce-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="e95ce-131">**Setmatrixtransform**</span><span class="sxs-lookup"><span data-stu-id="e95ce-131">**SetMatrixTranspose**</span></span>](id3dxbaseeffect--setmatrixtranspose.md)
</dt> </dl>

 

 




