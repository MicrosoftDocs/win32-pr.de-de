---
description: Legt ein Array von Zeigern auf umgesetzte Matrizen fest.
ms.assetid: f2db10cb-a146-412d-8de8-f093253470fd
title: 'ID3DXConstantTable:: setmatrixtransposepointerarray-Methode (D3DX9Shader. h)'
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
ms.openlocfilehash: 6c78c051ff2d2ab52c9a741fa117a89f66ff450d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373520"
---
# <a name="id3dxconstanttablesetmatrixtransposepointerarray-method"></a><span data-ttu-id="ac78e-103">ID3DXConstantTable:: setmatrixtransposepointerarray-Methode</span><span class="sxs-lookup"><span data-stu-id="ac78e-103">ID3DXConstantTable::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="ac78e-104">Legt ein Array von Zeigern auf umgesetzte Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="ac78e-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac78e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac78e-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="ac78e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac78e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac78e-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac78e-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac78e-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ac78e-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ac78e-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Konstanten Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ac78e-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="ac78e-110">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac78e-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac78e-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ac78e-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ac78e-112">Eindeutiger Bezeichner für das Array von Matrix Konstanten.</span><span class="sxs-lookup"><span data-stu-id="ac78e-112">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="ac78e-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ac78e-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac78e-114">*ppmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac78e-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac78e-115">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="ac78e-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="ac78e-116">Array von Zeigern auf umgesetzte Matrizen.</span><span class="sxs-lookup"><span data-stu-id="ac78e-116">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="ac78e-117">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="ac78e-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac78e-118">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac78e-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac78e-119">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac78e-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac78e-120">Anzahl von Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="ac78e-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac78e-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac78e-121">Return value</span></span>

<span data-ttu-id="ac78e-122">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ac78e-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ac78e-123">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ac78e-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ac78e-124">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="ac78e-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac78e-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac78e-125">Remarks</span></span>

<span data-ttu-id="ac78e-126">Eine umgesetzte Matrix enthält Spalten Hauptdaten. Das heißt, jeder Vektor ist in einer Spalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="ac78e-126">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac78e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac78e-127">Requirements</span></span>



| <span data-ttu-id="ac78e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac78e-128">Requirement</span></span> | <span data-ttu-id="ac78e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="ac78e-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac78e-130">Header</span><span class="sxs-lookup"><span data-stu-id="ac78e-130">Header</span></span><br/>  | <dl> <span data-ttu-id="ac78e-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac78e-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ac78e-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ac78e-132">Library</span></span><br/> | <dl> <span data-ttu-id="ac78e-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac78e-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ac78e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac78e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac78e-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="ac78e-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
