---
description: Ruft eine Konstante von einem Array von Konstanten ab. Ein Array besteht aus Elementen.
ms.assetid: 20a61207-b0e1-455d-9b65-0fade543d1cf
title: 'ID3DXConstantTable:: getconstantelements-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5396c70c1c4286223d9f45fb8ab9b73a019becb1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363144"
---
# <a name="id3dxconstanttablegetconstantelement-method"></a><span data-ttu-id="88d5b-104">ID3DXConstantTable:: getconstantelements-Methode</span><span class="sxs-lookup"><span data-stu-id="88d5b-104">ID3DXConstantTable::GetConstantElement method</span></span>

<span data-ttu-id="88d5b-105">Ruft eine Konstante von einem Array von Konstanten ab.</span><span class="sxs-lookup"><span data-stu-id="88d5b-105">Gets a constant from an array of constants.</span></span> <span data-ttu-id="88d5b-106">Ein Array besteht aus Elementen.</span><span class="sxs-lookup"><span data-stu-id="88d5b-106">An array is made up of elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="88d5b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="88d5b-107">Syntax</span></span>


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="88d5b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="88d5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88d5b-109">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88d5b-109">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88d5b-110">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="88d5b-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="88d5b-111">Eindeutiger Bezeichner für das Array von Konstanten.</span><span class="sxs-lookup"><span data-stu-id="88d5b-111">Unique identifier to the array of constants.</span></span> <span data-ttu-id="88d5b-112">Dieser Wert darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="88d5b-112">This value may not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="88d5b-113">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88d5b-113">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88d5b-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="88d5b-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="88d5b-115">NULL basierter Index des Elements im Array.</span><span class="sxs-lookup"><span data-stu-id="88d5b-115">Zero-based index of the element in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88d5b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88d5b-116">Return value</span></span>

<span data-ttu-id="88d5b-117">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="88d5b-117">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="88d5b-118">Gibt einen eindeutigen Bezeichner für die Element Konstante zurück.</span><span class="sxs-lookup"><span data-stu-id="88d5b-118">Returns a unique identifier to the element constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="88d5b-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88d5b-119">Remarks</span></span>

<span data-ttu-id="88d5b-120">Verwenden Sie [**ID3DXConstantTable:: getconstant**](id3dxconstanttable--getconstant.md) oder [**ID3DXConstantTable:: getconstantbyname**](id3dxconstanttable--getconstantbyname.md), um eine Konstante zu erhalten, die nicht Teil eines Arrays ist.</span><span class="sxs-lookup"><span data-stu-id="88d5b-120">To get a constant that is not part of an array, use [**ID3DXConstantTable::GetConstant**](id3dxconstanttable--getconstant.md) or [**ID3DXConstantTable::GetConstantByName**](id3dxconstanttable--getconstantbyname.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88d5b-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88d5b-121">Requirements</span></span>



| <span data-ttu-id="88d5b-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88d5b-122">Requirement</span></span> | <span data-ttu-id="88d5b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="88d5b-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="88d5b-124">Header</span><span class="sxs-lookup"><span data-stu-id="88d5b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="88d5b-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="88d5b-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="88d5b-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="88d5b-126">Library</span></span><br/> | <dl> <span data-ttu-id="88d5b-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88d5b-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="88d5b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88d5b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88d5b-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="88d5b-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
