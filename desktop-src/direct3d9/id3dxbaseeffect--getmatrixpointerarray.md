---
description: Ruft ein Array von Zeigern auf nicht umgesetzte Matrizen ab.
ms.assetid: ee9f752d-a06a-43a3-b4ce-d1d585ba8c08
title: 'ID3DXBaseEffect:: getmatrixpointerarray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixPointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a841c321e641b74841a76432eab8b016f396f61a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961755"
---
# <a name="id3dxbaseeffectgetmatrixpointerarray-method"></a><span data-ttu-id="23e0a-103">ID3DXBaseEffect:: getmatrixpointerarray-Methode</span><span class="sxs-lookup"><span data-stu-id="23e0a-103">ID3DXBaseEffect::GetMatrixPointerArray method</span></span>

<span data-ttu-id="23e0a-104">Ruft ein Array von Zeigern auf nicht umgesetzte Matrizen ab.</span><span class="sxs-lookup"><span data-stu-id="23e0a-104">Gets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="23e0a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="23e0a-105">Syntax</span></span>


```C++
HRESULT GetMatrixPointerArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX **ppMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="23e0a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="23e0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23e0a-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23e0a-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23e0a-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="23e0a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="23e0a-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="23e0a-109">Unique identifier.</span></span> <span data-ttu-id="23e0a-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="23e0a-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="23e0a-111">*ppmatrix* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="23e0a-111">*ppMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23e0a-112">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="23e0a-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="23e0a-113">Array von Zeigern auf nicht umgesetzte Matrizen.</span><span class="sxs-lookup"><span data-stu-id="23e0a-113">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="23e0a-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="23e0a-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="23e0a-115">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23e0a-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23e0a-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23e0a-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="23e0a-117">Anzahl von Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="23e0a-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23e0a-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="23e0a-118">Return value</span></span>

<span data-ttu-id="23e0a-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="23e0a-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="23e0a-120">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="23e0a-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="23e0a-121">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="23e0a-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="23e0a-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23e0a-122">Remarks</span></span>

<span data-ttu-id="23e0a-123">Eine nicht umgesetzte Matrix enthält Zeilen Hauptdaten; Das heißt, jeder Vektor ist in einer Zeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="23e0a-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="23e0a-124">Wenn die Ziel Matrizen größer als die Quell Matrizen sind, werden nur die linken oberen Komponenten der einzelnen Ziel Matrix gefüllt, und die restlichen Ziel Matrixkomponenten werden auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="23e0a-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="23e0a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23e0a-125">Requirements</span></span>



| <span data-ttu-id="23e0a-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23e0a-126">Requirement</span></span> | <span data-ttu-id="23e0a-127">Wert</span><span class="sxs-lookup"><span data-stu-id="23e0a-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="23e0a-128">Header</span><span class="sxs-lookup"><span data-stu-id="23e0a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="23e0a-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="23e0a-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="23e0a-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="23e0a-130">Library</span></span><br/> | <dl> <span data-ttu-id="23e0a-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23e0a-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="23e0a-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23e0a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23e0a-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="23e0a-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="23e0a-134">**Getmatrixarray**</span><span class="sxs-lookup"><span data-stu-id="23e0a-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
