---
description: Legt eine übersetzte Matrix fest.
ms.assetid: 1c4d64ce-64bd-47d4-9912-879f4834c0e8
title: 'ID3DXConstantTable:: setmatrixtransform-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTranspose
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa84f9e483be0c6c2ddae37c52ef6df2c43fda90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365101"
---
# <a name="id3dxconstanttablesetmatrixtranspose-method"></a><span data-ttu-id="f2542-103">ID3DXConstantTable:: setmatrixtransform-Methode</span><span class="sxs-lookup"><span data-stu-id="f2542-103">ID3DXConstantTable::SetMatrixTranspose method</span></span>

<span data-ttu-id="f2542-104">Legt eine übersetzte Matrix fest.</span><span class="sxs-lookup"><span data-stu-id="f2542-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2542-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2542-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="f2542-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2542-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2542-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2542-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2542-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="f2542-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="f2542-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Konstanten Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f2542-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="f2542-110">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2542-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2542-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f2542-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f2542-112">Eindeutiger Bezeichner für die Matrix der Konstanten.</span><span class="sxs-lookup"><span data-stu-id="f2542-112">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="f2542-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f2542-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2542-114">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2542-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2542-115">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f2542-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f2542-116">Zeiger auf eine umgesetzte Matrix.</span><span class="sxs-lookup"><span data-stu-id="f2542-116">Pointer to a transposed matrix.</span></span> <span data-ttu-id="f2542-117">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="f2542-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2542-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2542-118">Return value</span></span>

<span data-ttu-id="f2542-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f2542-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f2542-120">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f2542-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f2542-121">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="f2542-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2542-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2542-122">Requirements</span></span>



| <span data-ttu-id="f2542-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2542-123">Requirement</span></span> | <span data-ttu-id="f2542-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f2542-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2542-125">Header</span><span class="sxs-lookup"><span data-stu-id="f2542-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f2542-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2542-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f2542-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f2542-127">Library</span></span><br/> | <dl> <span data-ttu-id="f2542-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2542-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f2542-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2542-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2542-130">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="f2542-130">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
