---
description: Legt ein Array von Zeigern auf nicht umgesetzte Matrizen fest.
ms.assetid: 1b985e03-b5cb-48e5-969f-115ca165acdc
title: 'ID3DXConstantTable:: setmatrixpointerarray-Methode (D3DX9Shader. h)'
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
ms.openlocfilehash: 4b29d4298d8ca52d2826cc780fb90d769c3337f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363977"
---
# <a name="id3dxconstanttablesetmatrixpointerarray-method"></a><span data-ttu-id="733fd-103">ID3DXConstantTable:: setmatrixpointerarray-Methode</span><span class="sxs-lookup"><span data-stu-id="733fd-103">ID3DXConstantTable::SetMatrixPointerArray method</span></span>

<span data-ttu-id="733fd-104">Legt ein Array von Zeigern auf nicht umgesetzte Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="733fd-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="733fd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="733fd-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="733fd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="733fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="733fd-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="733fd-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="733fd-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="733fd-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="733fd-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Konstanten Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="733fd-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="733fd-110">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="733fd-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="733fd-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="733fd-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="733fd-112">Eindeutiger Bezeichner für ein Array konstanter Matrizen.</span><span class="sxs-lookup"><span data-stu-id="733fd-112">Unique identifier to an array of constant matrices.</span></span> <span data-ttu-id="733fd-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="733fd-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="733fd-114">*ppmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="733fd-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="733fd-115">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="733fd-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="733fd-116">Array von Zeigern auf nicht umgesetzte Matrizen.</span><span class="sxs-lookup"><span data-stu-id="733fd-116">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="733fd-117">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="733fd-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="733fd-118">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="733fd-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="733fd-119">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="733fd-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="733fd-120">Anzahl von Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="733fd-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="733fd-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="733fd-121">Return value</span></span>

<span data-ttu-id="733fd-122">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="733fd-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="733fd-123">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="733fd-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="733fd-124">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="733fd-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="733fd-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="733fd-125">Remarks</span></span>

<span data-ttu-id="733fd-126">Eine nicht umgesetzte Matrix enthält Zeilen Hauptdaten; Das heißt, jeder Vektor ist in einer Zeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="733fd-126">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="733fd-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="733fd-127">Requirements</span></span>



| <span data-ttu-id="733fd-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="733fd-128">Requirement</span></span> | <span data-ttu-id="733fd-129">Wert</span><span class="sxs-lookup"><span data-stu-id="733fd-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="733fd-130">Header</span><span class="sxs-lookup"><span data-stu-id="733fd-130">Header</span></span><br/>  | <dl> <span data-ttu-id="733fd-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="733fd-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="733fd-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="733fd-132">Library</span></span><br/> | <dl> <span data-ttu-id="733fd-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="733fd-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="733fd-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="733fd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="733fd-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="733fd-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
