---
description: Legt ein Array nicht umsetzbarer Matrizen fest.
ms.assetid: f36b8e8a-c22f-41e6-acb1-6298291b002f
title: 'ID3DXConstantTable:: setmatrixarray-Methode (D3DX9Shader. h)'
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
ms.openlocfilehash: 48dd85975ac58dd26d4194584ce5fbebe26da2a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351954"
---
# <a name="id3dxconstanttablesetmatrixarray-method"></a><span data-ttu-id="22422-103">ID3DXConstantTable:: setmatrixarray-Methode</span><span class="sxs-lookup"><span data-stu-id="22422-103">ID3DXConstantTable::SetMatrixArray method</span></span>

<span data-ttu-id="22422-104">Legt ein Array nicht umsetzbarer Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="22422-104">Sets an array of nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="22422-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22422-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="22422-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22422-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22422-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22422-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22422-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="22422-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="22422-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Konstanten Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="22422-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="22422-110">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22422-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22422-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="22422-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="22422-112">Eindeutiger Bezeichner für das Array konstanter Matrizen.</span><span class="sxs-lookup"><span data-stu-id="22422-112">Unique identifier to the array of constant matrices.</span></span> <span data-ttu-id="22422-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="22422-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="22422-114">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22422-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22422-115">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="22422-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="22422-116">Array nicht umsetzbarer Matrizen.</span><span class="sxs-lookup"><span data-stu-id="22422-116">Array of nontransposed matrices.</span></span> <span data-ttu-id="22422-117">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="22422-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="22422-118">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22422-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22422-119">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="22422-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="22422-120">Anzahl von Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="22422-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22422-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22422-121">Return value</span></span>

<span data-ttu-id="22422-122">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="22422-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="22422-123">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="22422-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="22422-124">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="22422-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="22422-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22422-125">Requirements</span></span>



| <span data-ttu-id="22422-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22422-126">Requirement</span></span> | <span data-ttu-id="22422-127">Wert</span><span class="sxs-lookup"><span data-stu-id="22422-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="22422-128">Header</span><span class="sxs-lookup"><span data-stu-id="22422-128">Header</span></span><br/>  | <dl> <span data-ttu-id="22422-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="22422-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="22422-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="22422-130">Library</span></span><br/> | <dl> <span data-ttu-id="22422-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22422-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="22422-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22422-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22422-133">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="22422-133">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
