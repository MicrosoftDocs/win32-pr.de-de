---
description: Legt ein Array von Zeigern auf nicht umgesetzte Matrizen fest.
ms.assetid: f2e62470-6882-49d8-ae12-6c5b79dd5c99
title: 'ID3DXBaseEffect:: setmatrixpointerarray-Methode (D3DX9Shader. h)'
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
ms.openlocfilehash: 0f199c3db335dfc6b9966987678c07b4b3a22402
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961546"
---
# <a name="id3dxbaseeffectsetmatrixpointerarray-method"></a><span data-ttu-id="aff49-103">ID3DXBaseEffect:: setmatrixpointerarray-Methode</span><span class="sxs-lookup"><span data-stu-id="aff49-103">ID3DXBaseEffect::SetMatrixPointerArray method</span></span>

<span data-ttu-id="aff49-104">Legt ein Array von Zeigern auf nicht umgesetzte Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="aff49-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="aff49-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aff49-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="aff49-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aff49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aff49-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aff49-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aff49-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="aff49-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="aff49-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="aff49-109">Unique identifier.</span></span> <span data-ttu-id="aff49-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="aff49-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff49-111">*ppmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aff49-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aff49-112">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="aff49-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="aff49-113">Array von Zeigern auf nicht umgesetzte Matrizen.</span><span class="sxs-lookup"><span data-stu-id="aff49-113">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="aff49-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="aff49-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff49-115">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aff49-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aff49-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aff49-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aff49-117">Anzahl von Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="aff49-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aff49-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aff49-118">Return value</span></span>

<span data-ttu-id="aff49-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aff49-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aff49-120">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="aff49-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="aff49-121">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="aff49-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="aff49-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aff49-122">Remarks</span></span>

<span data-ttu-id="aff49-123">Eine nicht umgesetzte Matrix enthält Zeilen Hauptdaten; Das heißt, jeder Vektor ist in einer Zeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="aff49-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="aff49-124">Wenn die Ziel Matrizen kleiner als die Quell Matrizen sind, werden die zusätzlichen Komponenten der Quell Matrizen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="aff49-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="aff49-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aff49-125">Requirements</span></span>



| <span data-ttu-id="aff49-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aff49-126">Requirement</span></span> | <span data-ttu-id="aff49-127">Wert</span><span class="sxs-lookup"><span data-stu-id="aff49-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aff49-128">Header</span><span class="sxs-lookup"><span data-stu-id="aff49-128">Header</span></span><br/>  | <dl> <span data-ttu-id="aff49-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="aff49-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="aff49-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aff49-130">Library</span></span><br/> | <dl> <span data-ttu-id="aff49-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aff49-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="aff49-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aff49-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aff49-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="aff49-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="aff49-134">**Getmatrixarray**</span><span class="sxs-lookup"><span data-stu-id="aff49-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
