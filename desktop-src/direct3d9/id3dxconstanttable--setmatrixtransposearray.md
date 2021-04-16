---
description: Legt ein Array von umsetzten Matrizen fest.
ms.assetid: a67afc21-f43d-4dc5-b145-f3d66dd86dbb
title: 'ID3DXConstantTable:: setmatrixtransposearray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTransposeArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 69755ed973a8c412373287f128642b78ea2ad346
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530944"
---
# <a name="id3dxconstanttablesetmatrixtransposearray-method"></a><span data-ttu-id="721ee-103">ID3DXConstantTable:: setmatrixtransposearray-Methode</span><span class="sxs-lookup"><span data-stu-id="721ee-103">ID3DXConstantTable::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="721ee-104">Legt ein Array von umsetzten Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="721ee-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="721ee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="721ee-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="721ee-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="721ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="721ee-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="721ee-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="721ee-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="721ee-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="721ee-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Konstanten Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="721ee-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="721ee-110">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="721ee-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="721ee-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="721ee-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="721ee-112">Eindeutiger Bezeichner für das Array von Matrix Konstanten.</span><span class="sxs-lookup"><span data-stu-id="721ee-112">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="721ee-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="721ee-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="721ee-114">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="721ee-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="721ee-115">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="721ee-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="721ee-116">Array der übersetzten Matrizen.</span><span class="sxs-lookup"><span data-stu-id="721ee-116">Array of transposed matrices.</span></span> <span data-ttu-id="721ee-117">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="721ee-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="721ee-118">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="721ee-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="721ee-119">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="721ee-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="721ee-120">Anzahl von Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="721ee-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="721ee-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="721ee-121">Return value</span></span>

<span data-ttu-id="721ee-122">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="721ee-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="721ee-123">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="721ee-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="721ee-124">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="721ee-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="721ee-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="721ee-125">Requirements</span></span>



| <span data-ttu-id="721ee-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="721ee-126">Requirement</span></span> | <span data-ttu-id="721ee-127">Wert</span><span class="sxs-lookup"><span data-stu-id="721ee-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="721ee-128">Header</span><span class="sxs-lookup"><span data-stu-id="721ee-128">Header</span></span><br/>  | <dl> <span data-ttu-id="721ee-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="721ee-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="721ee-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="721ee-130">Library</span></span><br/> | <dl> <span data-ttu-id="721ee-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="721ee-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="721ee-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="721ee-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="721ee-133">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="721ee-133">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
