---
description: 'ID3DXConstantTable::SetMatrixArray-Methode: Legt ein Array von nicht übersetzten Matrizen fest.'
ms.assetid: f36b8e8a-c22f-41e6-acb1-6298291b002f
title: ID3DXConstantTable::SetMatrixArray-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 02e115cf4526ab065d2613636427059826f450f5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115098"
---
# <a name="id3dxconstanttablesetmatrixarray-method"></a><span data-ttu-id="2ac11-103">ID3DXConstantTable::SetMatrixArray-Methode</span><span class="sxs-lookup"><span data-stu-id="2ac11-103">ID3DXConstantTable::SetMatrixArray method</span></span>

<span data-ttu-id="2ac11-104">Legt ein Array von nicht übersetzten Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="2ac11-104">Sets an array of nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ac11-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ac11-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="2ac11-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ac11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ac11-107">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2ac11-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ac11-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="2ac11-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="2ac11-109">Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der Konstantentabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2ac11-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="2ac11-110">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2ac11-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ac11-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2ac11-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2ac11-112">Eindeutiger Bezeichner für das Array konstanter Matrizen.</span><span class="sxs-lookup"><span data-stu-id="2ac11-112">Unique identifier to the array of constant matrices.</span></span> <span data-ttu-id="2ac11-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2ac11-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ac11-114">*pMatrix* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2ac11-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ac11-115">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2ac11-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2ac11-116">Array von nicht übersetzten Matrizen.</span><span class="sxs-lookup"><span data-stu-id="2ac11-116">Array of nontransposed matrices.</span></span> <span data-ttu-id="2ac11-117">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="2ac11-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ac11-118">*Anzahl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2ac11-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ac11-119">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ac11-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ac11-120">Anzahl der Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="2ac11-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ac11-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ac11-121">Return value</span></span>

<span data-ttu-id="2ac11-122">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2ac11-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2ac11-123">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2ac11-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2ac11-124">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="2ac11-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ac11-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ac11-125">Requirements</span></span>



| <span data-ttu-id="2ac11-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ac11-126">Requirement</span></span> | <span data-ttu-id="2ac11-127">Wert</span><span class="sxs-lookup"><span data-stu-id="2ac11-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ac11-128">Header</span><span class="sxs-lookup"><span data-stu-id="2ac11-128">Header</span></span><br/>  | <dl> <span data-ttu-id="2ac11-129"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="2ac11-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2ac11-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2ac11-130">Library</span></span><br/> | <dl> <span data-ttu-id="2ac11-131"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ac11-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2ac11-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2ac11-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ac11-133">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="2ac11-133">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
