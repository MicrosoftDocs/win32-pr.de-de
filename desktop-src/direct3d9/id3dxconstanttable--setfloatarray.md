---
description: 'ID3DXConstantTable::SetFloatArray-Methode: Legt ein Array von Gleitkommazahlen fest.'
ms.assetid: 7a622dd5-47ed-4166-a6df-f484b03e0b5a
title: ID3DXConstantTable::SetFloatArray-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetFloatArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 23c96cb2bfc8113fd167c8b57a21a46285b691a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115168"
---
# <a name="id3dxconstanttablesetfloatarray-method"></a><span data-ttu-id="d7f2c-103">ID3DXConstantTable::SetFloatArray-Methode</span><span class="sxs-lookup"><span data-stu-id="d7f2c-103">ID3DXConstantTable::SetFloatArray method</span></span>

<span data-ttu-id="d7f2c-104">Legt ein Array von Gleitkommazahlen fest.</span><span class="sxs-lookup"><span data-stu-id="d7f2c-104">Sets an array of floating-point numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f2c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7f2c-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const FLOAT             *pf,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="d7f2c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7f2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7f2c-107">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d7f2c-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f2c-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d7f2c-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d7f2c-109">Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der konstanten Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d7f2c-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="d7f2c-110">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d7f2c-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f2c-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d7f2c-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d7f2c-112">Eindeutiger Bezeichner für das Array von Konstanten.</span><span class="sxs-lookup"><span data-stu-id="d7f2c-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="d7f2c-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d7f2c-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7f2c-114">*pf* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d7f2c-114">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f2c-115">Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d7f2c-115">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d7f2c-116">Array von Gleitkommazahlen.</span><span class="sxs-lookup"><span data-stu-id="d7f2c-116">Array of floating-point numbers.</span></span>

</dd> <dt>

<span data-ttu-id="d7f2c-117">*Anzahl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d7f2c-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f2c-118">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7f2c-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d7f2c-119">Anzahl der Gleitkommawerte im Array.</span><span class="sxs-lookup"><span data-stu-id="d7f2c-119">Number of floating-point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7f2c-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7f2c-120">Return value</span></span>

<span data-ttu-id="d7f2c-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d7f2c-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d7f2c-122">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d7f2c-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d7f2c-123">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="d7f2c-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7f2c-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7f2c-124">Requirements</span></span>



| <span data-ttu-id="d7f2c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7f2c-125">Requirement</span></span> | <span data-ttu-id="d7f2c-126">Wert</span><span class="sxs-lookup"><span data-stu-id="d7f2c-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f2c-127">Header</span><span class="sxs-lookup"><span data-stu-id="d7f2c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d7f2c-128"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="d7f2c-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d7f2c-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d7f2c-129">Library</span></span><br/> | <dl> <span data-ttu-id="d7f2c-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7f2c-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d7f2c-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d7f2c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f2c-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="d7f2c-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
