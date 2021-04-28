---
description: 'ID3DXConstantTable::SetMatrixTransposePointerArray-Methode: Legt ein Array von Zeigern auf transponierte Matrizen fest.'
ms.assetid: f2db10cb-a146-412d-8de8-f093253470fd
title: ID3DXConstantTable::SetMatrixTransposePointerArray-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fefb5a0b62174499a4631f2fe8020c25a3a8efa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115038"
---
# <a name="id3dxconstanttablesetmatrixtransposepointerarray-method"></a><span data-ttu-id="e206b-103">ID3DXConstantTable::SetMatrixTransposePointerArray-Methode</span><span class="sxs-lookup"><span data-stu-id="e206b-103">ID3DXConstantTable::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="e206b-104">Legt ein Array von Zeigern auf transponierte Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="e206b-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="e206b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e206b-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="e206b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e206b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e206b-107">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e206b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e206b-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e206b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e206b-109">Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der konstanten Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e206b-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="e206b-110">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e206b-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e206b-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e206b-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e206b-112">Eindeutiger Bezeichner für das Array von Matrixkonstanten.</span><span class="sxs-lookup"><span data-stu-id="e206b-112">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="e206b-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e206b-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e206b-114">*ppMatrix* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e206b-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e206b-115">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="e206b-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="e206b-116">Array von Zeigern auf transponierte Matrizen.</span><span class="sxs-lookup"><span data-stu-id="e206b-116">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="e206b-117">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="e206b-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="e206b-118">*Anzahl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e206b-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e206b-119">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e206b-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e206b-120">Anzahl der Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="e206b-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e206b-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e206b-121">Return value</span></span>

<span data-ttu-id="e206b-122">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e206b-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e206b-123">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e206b-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e206b-124">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="e206b-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e206b-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e206b-125">Remarks</span></span>

<span data-ttu-id="e206b-126">Eine transponierte Matrix enthält Spalten-Hauptdaten. Das heißt, jeder Vektor ist in einer Spalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="e206b-126">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="e206b-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e206b-127">Requirements</span></span>



| <span data-ttu-id="e206b-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e206b-128">Requirement</span></span> | <span data-ttu-id="e206b-129">Wert</span><span class="sxs-lookup"><span data-stu-id="e206b-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e206b-130">Header</span><span class="sxs-lookup"><span data-stu-id="e206b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="e206b-131"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="e206b-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e206b-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e206b-132">Library</span></span><br/> | <dl> <span data-ttu-id="e206b-133"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e206b-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e206b-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e206b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e206b-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="e206b-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
