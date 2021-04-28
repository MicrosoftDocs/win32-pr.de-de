---
description: 'ID3DXConstantTable::GetConstant-Methode: Ruft eine Konstante ab, indem ihr Index gesucht wird.'
ms.assetid: 7db25171-9bda-4db8-b6a8-8a4d60a842f7
title: ID3DXConstantTable::GetConstant-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 664a1b1a214b49eb731a3a0766a255e5f5acadd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115268"
---
# <a name="id3dxconstanttablegetconstant-method"></a><span data-ttu-id="e527f-103">ID3DXConstantTable::GetConstant-Methode</span><span class="sxs-lookup"><span data-stu-id="e527f-103">ID3DXConstantTable::GetConstant method</span></span>

<span data-ttu-id="e527f-104">Ruft eine Konstante ab, indem ihr Index gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="e527f-104">Gets a constant by looking up its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e527f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e527f-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="e527f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e527f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e527f-107">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e527f-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e527f-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e527f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e527f-109">Eindeutiger Bezeichner für die übergeordnete Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="e527f-109">Unique identifier to the parent data structure.</span></span> <span data-ttu-id="e527f-110">Wenn die Konstante ein Parameter der obersten Ebene ist (es gibt keine übergeordnete Datenstruktur), verwenden Sie **NULL.**</span><span class="sxs-lookup"><span data-stu-id="e527f-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e527f-111">*Index* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e527f-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e527f-112">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e527f-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e527f-113">Nullbasierter Index der Konstante.</span><span class="sxs-lookup"><span data-stu-id="e527f-113">Zero-based index of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e527f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e527f-114">Return value</span></span>

<span data-ttu-id="e527f-115">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e527f-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e527f-116">Gibt einen eindeutigen Bezeichner an die Konstante zurück.</span><span class="sxs-lookup"><span data-stu-id="e527f-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="e527f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e527f-117">Remarks</span></span>

<span data-ttu-id="e527f-118">Um eine Konstante aus einem Array von Konstanten zu erhalten, verwenden Sie [**ID3DXConstantTable::GetConstantElement**](id3dxconstanttable--getconstantelement.md).</span><span class="sxs-lookup"><span data-stu-id="e527f-118">To get a constant from an array of constants, use [**ID3DXConstantTable::GetConstantElement**](id3dxconstanttable--getconstantelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e527f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e527f-119">Requirements</span></span>



| <span data-ttu-id="e527f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e527f-120">Requirement</span></span> | <span data-ttu-id="e527f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e527f-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e527f-122">Header</span><span class="sxs-lookup"><span data-stu-id="e527f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e527f-123"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="e527f-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e527f-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e527f-124">Library</span></span><br/> | <dl> <span data-ttu-id="e527f-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e527f-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e527f-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e527f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e527f-127">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="e527f-127">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
