---
description: 'ID3DXConstantTable::SetMatrixTranspose-Methode: Legt eine transponierte Matrix fest.'
ms.assetid: 1c4d64ce-64bd-47d4-9912-879f4834c0e8
title: ID3DXConstantTable::SetMatrixTranspose-Methode (D3DX9Shader.h)
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
ms.openlocfilehash: 06cc989a14da6f2fe84d30f7f5d7d9fc35acd3bc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115058"
---
# <a name="id3dxconstanttablesetmatrixtranspose-method"></a><span data-ttu-id="5035b-103">ID3DXConstantTable::SetMatrixTranspose-Methode</span><span class="sxs-lookup"><span data-stu-id="5035b-103">ID3DXConstantTable::SetMatrixTranspose method</span></span>

<span data-ttu-id="5035b-104">Legt eine transponierte Matrix fest.</span><span class="sxs-lookup"><span data-stu-id="5035b-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="5035b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5035b-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="5035b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5035b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5035b-107">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5035b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5035b-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="5035b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="5035b-109">Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der konstanten Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5035b-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="5035b-110">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5035b-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5035b-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5035b-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5035b-112">Eindeutiger Bezeichner für die Matrix von Konstanten.</span><span class="sxs-lookup"><span data-stu-id="5035b-112">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="5035b-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5035b-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="5035b-114">*pMatrix* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5035b-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5035b-115">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5035b-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5035b-116">Zeiger auf eine transponierte Matrix.</span><span class="sxs-lookup"><span data-stu-id="5035b-116">Pointer to a transposed matrix.</span></span> <span data-ttu-id="5035b-117">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="5035b-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5035b-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5035b-118">Return value</span></span>

<span data-ttu-id="5035b-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5035b-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5035b-120">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5035b-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5035b-121">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="5035b-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5035b-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5035b-122">Requirements</span></span>



| <span data-ttu-id="5035b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5035b-123">Requirement</span></span> | <span data-ttu-id="5035b-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5035b-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5035b-125">Header</span><span class="sxs-lookup"><span data-stu-id="5035b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5035b-126"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="5035b-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5035b-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5035b-127">Library</span></span><br/> | <dl> <span data-ttu-id="5035b-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5035b-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5035b-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5035b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5035b-130">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="5035b-130">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
