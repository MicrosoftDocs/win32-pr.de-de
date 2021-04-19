---
description: Legt ein Array von Zeigern auf umgesetzte Matrizen fest.
ms.assetid: 11a21077-eeee-4d52-ac16-41444e3eca4f
title: 'ID3DXBaseEffect:: setmatrixtransposepointerarray-Methode (D3DX9Shader. h)'
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
ms.openlocfilehash: 1152deccdcadebe9f421fac6d7d5ce53c8d3e5f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355220"
---
# <a name="id3dxbaseeffectsetmatrixtransposepointerarray-method"></a><span data-ttu-id="9e6da-103">ID3DXBaseEffect:: setmatrixtransposepointerarray-Methode</span><span class="sxs-lookup"><span data-stu-id="9e6da-103">ID3DXBaseEffect::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="9e6da-104">Legt ein Array von Zeigern auf umgesetzte Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="9e6da-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e6da-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e6da-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="9e6da-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e6da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e6da-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e6da-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e6da-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="9e6da-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="9e6da-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="9e6da-109">Unique identifier.</span></span> <span data-ttu-id="9e6da-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="9e6da-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e6da-111">*ppmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e6da-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e6da-112">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="9e6da-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="9e6da-113">Array von Zeigern auf umgesetzte Matrizen.</span><span class="sxs-lookup"><span data-stu-id="9e6da-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="9e6da-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="9e6da-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e6da-115">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e6da-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e6da-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9e6da-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9e6da-117">Anzahl von Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="9e6da-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e6da-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e6da-118">Return value</span></span>

<span data-ttu-id="9e6da-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9e6da-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9e6da-120">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9e6da-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9e6da-121">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="9e6da-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e6da-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e6da-122">Remarks</span></span>

<span data-ttu-id="9e6da-123">Eine umgesetzte Matrix enthält Spalten Hauptdaten. Das heißt, jeder Vektor ist in einer Spalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="9e6da-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="9e6da-124">Wenn die Ziel Matrizen kleiner als die Quell Matrizen sind, werden die zusätzlichen Komponenten der Quell Matrizen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9e6da-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e6da-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e6da-125">Requirements</span></span>



| <span data-ttu-id="9e6da-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e6da-126">Requirement</span></span> | <span data-ttu-id="9e6da-127">Wert</span><span class="sxs-lookup"><span data-stu-id="9e6da-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e6da-128">Header</span><span class="sxs-lookup"><span data-stu-id="9e6da-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9e6da-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e6da-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9e6da-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9e6da-130">Library</span></span><br/> | <dl> <span data-ttu-id="9e6da-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e6da-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9e6da-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e6da-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e6da-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="9e6da-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="9e6da-134">**Getmatrixtransposearray**</span><span class="sxs-lookup"><span data-stu-id="9e6da-134">**GetMatrixTransposeArray**</span></span>](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
