---
description: 'ID3DXConstantTable::GetConstantByName-Methode: Ruft eine Konstante ab, indem ihr Name gesucht wird.'
ms.assetid: 785a2d4f-6391-4419-a0b8-d8244a03ceae
title: ID3DXConstantTable::GetConstantByName-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 88461a45bf484a72c085f1776eb923a8534b8be3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115248"
---
# <a name="id3dxconstanttablegetconstantbyname-method"></a><span data-ttu-id="ff5db-103">ID3DXConstantTable::GetConstantByName-Methode</span><span class="sxs-lookup"><span data-stu-id="ff5db-103">ID3DXConstantTable::GetConstantByName method</span></span>

<span data-ttu-id="ff5db-104">Ruft eine Konstante ab, indem ihr Name gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="ff5db-104">Gets a constant by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff5db-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff5db-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="ff5db-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff5db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff5db-107">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ff5db-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff5db-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ff5db-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ff5db-109">Eindeutiger Bezeichner für die übergeordnete Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="ff5db-109">Unique identifier to the parent data structure.</span></span> <span data-ttu-id="ff5db-110">Wenn die Konstante ein Parameter der obersten Ebene ist (es gibt keine übergeordnete Datenstruktur), verwenden Sie **NULL.**</span><span class="sxs-lookup"><span data-stu-id="ff5db-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ff5db-111">*pName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ff5db-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff5db-112">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff5db-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff5db-113">Name der Konstante.</span><span class="sxs-lookup"><span data-stu-id="ff5db-113">Name of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff5db-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff5db-114">Return value</span></span>

<span data-ttu-id="ff5db-115">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ff5db-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ff5db-116">Gibt einen eindeutigen Bezeichner an die Konstante zurück.</span><span class="sxs-lookup"><span data-stu-id="ff5db-116">Returns a unique identifier to the constant.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff5db-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff5db-117">Requirements</span></span>



| <span data-ttu-id="ff5db-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff5db-118">Requirement</span></span> | <span data-ttu-id="ff5db-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ff5db-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff5db-120">Header</span><span class="sxs-lookup"><span data-stu-id="ff5db-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ff5db-121"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="ff5db-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ff5db-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ff5db-122">Library</span></span><br/> | <dl> <span data-ttu-id="ff5db-123"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff5db-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ff5db-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ff5db-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff5db-125">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="ff5db-125">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
