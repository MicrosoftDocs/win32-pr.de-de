---
description: 'ID3DXConstantTable::SetMatrixPointerArray-Methode: Legt ein Array von Zeigern auf nicht übersetzte Matrizen fest.'
ms.assetid: 1b985e03-b5cb-48e5-969f-115ca165acdc
title: ID3DXConstantTable::SetMatrixPointerArray-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixPointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd9505f82674efc822d4921d7116c8eab17198c1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115068"
---
# <a name="id3dxconstanttablesetmatrixpointerarray-method"></a><span data-ttu-id="633c1-103">ID3DXConstantTable::SetMatrixPointerArray-Methode</span><span class="sxs-lookup"><span data-stu-id="633c1-103">ID3DXConstantTable::SetMatrixPointerArray method</span></span>

<span data-ttu-id="633c1-104">Legt ein Array von Zeigern auf nicht übersetzte Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="633c1-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="633c1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="633c1-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="633c1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="633c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="633c1-107">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="633c1-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="633c1-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="633c1-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="633c1-109">Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der Konstantentabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="633c1-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="633c1-110">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="633c1-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="633c1-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="633c1-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="633c1-112">Eindeutiger Bezeichner für ein Array von konstanten Matrizen.</span><span class="sxs-lookup"><span data-stu-id="633c1-112">Unique identifier to an array of constant matrices.</span></span> <span data-ttu-id="633c1-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="633c1-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="633c1-114">*ppMatrix* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="633c1-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="633c1-115">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="633c1-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="633c1-116">Array von Zeigern auf nicht übersetzte Matrizen.</span><span class="sxs-lookup"><span data-stu-id="633c1-116">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="633c1-117">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="633c1-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="633c1-118">*Anzahl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="633c1-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="633c1-119">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="633c1-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="633c1-120">Anzahl der Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="633c1-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="633c1-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="633c1-121">Return value</span></span>

<span data-ttu-id="633c1-122">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="633c1-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="633c1-123">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="633c1-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="633c1-124">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="633c1-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="633c1-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="633c1-125">Remarks</span></span>

<span data-ttu-id="633c1-126">Eine nicht übersetzte Matrix enthält Zeilen-Hauptdaten. Das heißt, jeder Vektor ist in einer Zeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="633c1-126">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="633c1-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="633c1-127">Requirements</span></span>



| <span data-ttu-id="633c1-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="633c1-128">Requirement</span></span> | <span data-ttu-id="633c1-129">Wert</span><span class="sxs-lookup"><span data-stu-id="633c1-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="633c1-130">Header</span><span class="sxs-lookup"><span data-stu-id="633c1-130">Header</span></span><br/>  | <dl> <span data-ttu-id="633c1-131"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="633c1-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="633c1-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="633c1-132">Library</span></span><br/> | <dl> <span data-ttu-id="633c1-133"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="633c1-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="633c1-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="633c1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="633c1-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="633c1-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
