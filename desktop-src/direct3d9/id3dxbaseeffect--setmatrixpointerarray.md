---
description: 'ID3DXBaseEffect::SetMatrixPointerArray-Methode: Legt ein Array von Zeigern auf nicht übersetzte Matrizen fest.'
ms.assetid: f2e62470-6882-49d8-ae12-6c5b79dd5c99
title: ID3DXBaseEffect::SetMatrixPointerArray-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixPointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cfe30e0132cfa237ddbccc24758b35e102a62b0c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093768"
---
# <a name="id3dxbaseeffectsetmatrixpointerarray-method"></a><span data-ttu-id="73863-103">ID3DXBaseEffect::SetMatrixPointerArray-Methode</span><span class="sxs-lookup"><span data-stu-id="73863-103">ID3DXBaseEffect::SetMatrixPointerArray method</span></span>

<span data-ttu-id="73863-104">Legt ein Array von Zeigern auf nicht übersetzte Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="73863-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="73863-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="73863-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="73863-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="73863-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73863-107">*hParameter* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="73863-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73863-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="73863-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="73863-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="73863-109">Unique identifier.</span></span> <span data-ttu-id="73863-110">Siehe [Handles (Direct3D 9).](handles.md)</span><span class="sxs-lookup"><span data-stu-id="73863-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="73863-111">*ppMatrix* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="73863-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73863-112">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="73863-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="73863-113">Array von Zeigern auf nicht übersetzte Matrizen.</span><span class="sxs-lookup"><span data-stu-id="73863-113">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="73863-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="73863-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="73863-115">*Anzahl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="73863-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73863-116">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73863-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73863-117">Anzahl der Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="73863-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73863-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73863-118">Return value</span></span>

<span data-ttu-id="73863-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="73863-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="73863-120">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="73863-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="73863-121">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="73863-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="73863-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73863-122">Remarks</span></span>

<span data-ttu-id="73863-123">Eine nicht übersetzte Matrix enthält Zeilen-Hauptdaten. Das heißt, jeder Vektor ist in einer Zeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="73863-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="73863-124">Wenn die Zielmatrizen kleiner als die Quellmatrizen sind, werden die zusätzlichen Komponenten der Quellmatrizen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="73863-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="73863-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73863-125">Requirements</span></span>



| <span data-ttu-id="73863-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73863-126">Requirement</span></span> | <span data-ttu-id="73863-127">Wert</span><span class="sxs-lookup"><span data-stu-id="73863-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="73863-128">Header</span><span class="sxs-lookup"><span data-stu-id="73863-128">Header</span></span><br/>  | <dl> <span data-ttu-id="73863-129"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="73863-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="73863-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="73863-130">Library</span></span><br/> | <dl> <span data-ttu-id="73863-131"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="73863-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="73863-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="73863-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73863-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="73863-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="73863-134">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="73863-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
