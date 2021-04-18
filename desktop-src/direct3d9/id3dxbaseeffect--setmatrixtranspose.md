---
description: Legt eine übersetzte Matrix fest.
ms.assetid: d340b058-6ba5-43ec-b398-111064965730
title: 'ID3DXBaseEffect:: setmatrixtransform-Methode (D3DX9Shader. h)'
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
ms.openlocfilehash: f62847f7b15899389cbd5f207ce810b0ed0dd119
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354978"
---
# <a name="id3dxbaseeffectsetmatrixtranspose-method"></a><span data-ttu-id="9123d-103">ID3DXBaseEffect:: setmatrixtransform-Methode</span><span class="sxs-lookup"><span data-stu-id="9123d-103">ID3DXBaseEffect::SetMatrixTranspose method</span></span>

<span data-ttu-id="9123d-104">Legt eine übersetzte Matrix fest.</span><span class="sxs-lookup"><span data-stu-id="9123d-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="9123d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9123d-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="9123d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9123d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9123d-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9123d-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9123d-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="9123d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="9123d-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="9123d-109">Unique identifier.</span></span> <span data-ttu-id="9123d-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="9123d-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="9123d-111">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9123d-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9123d-112">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="9123d-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9123d-113">Zeiger auf eine umgesetzte Matrix.</span><span class="sxs-lookup"><span data-stu-id="9123d-113">Pointer to a transposed matrix.</span></span> <span data-ttu-id="9123d-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="9123d-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9123d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9123d-115">Return value</span></span>

<span data-ttu-id="9123d-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9123d-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9123d-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9123d-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9123d-118">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="9123d-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9123d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9123d-119">Remarks</span></span>

<span data-ttu-id="9123d-120">Eine umgesetzte Matrix enthält Spalten Hauptdaten. Das heißt, jeder Vektor ist in einer Spalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="9123d-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="9123d-121">Wenn die Ziel Matrix kleiner als die Quell Matrix ist, werden die zusätzlichen Komponenten der Quell Matrix ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9123d-121">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="9123d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9123d-122">Requirements</span></span>



| <span data-ttu-id="9123d-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9123d-123">Requirement</span></span> | <span data-ttu-id="9123d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9123d-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9123d-125">Header</span><span class="sxs-lookup"><span data-stu-id="9123d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="9123d-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="9123d-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9123d-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9123d-127">Library</span></span><br/> | <dl> <span data-ttu-id="9123d-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9123d-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9123d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9123d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9123d-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="9123d-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="9123d-131">**Getmatrixtransform**</span><span class="sxs-lookup"><span data-stu-id="9123d-131">**GetMatrixTranspose**</span></span>](id3dxbaseeffect--getmatrixtranspose.md)
</dt> </dl>

 

 




