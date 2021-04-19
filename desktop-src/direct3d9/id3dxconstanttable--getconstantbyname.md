---
description: Ruft eine Konstante ab, indem Ihr Name gesucht wird.
ms.assetid: 785a2d4f-6391-4419-a0b8-d8244a03ceae
title: 'ID3DXConstantTable:: getconstantbyname-Methode (D3DX9Shader. h)'
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
ms.openlocfilehash: 3df4fc2cf44e035daf208d5dd14602e89b528ed1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363979"
---
# <a name="id3dxconstanttablegetconstantbyname-method"></a><span data-ttu-id="3ef9a-103">ID3DXConstantTable:: getconstantbyname-Methode</span><span class="sxs-lookup"><span data-stu-id="3ef9a-103">ID3DXConstantTable::GetConstantByName method</span></span>

<span data-ttu-id="3ef9a-104">Ruft eine Konstante ab, indem Ihr Name gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="3ef9a-104">Gets a constant by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ef9a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ef9a-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="3ef9a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ef9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ef9a-107">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ef9a-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ef9a-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="3ef9a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="3ef9a-109">Eindeutiger Bezeichner für die übergeordnete Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="3ef9a-109">Unique identifier to the parent data structure.</span></span> <span data-ttu-id="3ef9a-110">Wenn die Konstante ein Parameter der obersten Ebene ist (es gibt keine übergeordnete Datenstruktur), verwenden Sie **null**.</span><span class="sxs-lookup"><span data-stu-id="3ef9a-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3ef9a-111">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ef9a-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ef9a-112">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ef9a-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ef9a-113">Der Name der Konstanten.</span><span class="sxs-lookup"><span data-stu-id="3ef9a-113">Name of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ef9a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3ef9a-114">Return value</span></span>

<span data-ttu-id="3ef9a-115">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="3ef9a-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="3ef9a-116">Gibt einen eindeutigen Bezeichner für die Konstante zurück.</span><span class="sxs-lookup"><span data-stu-id="3ef9a-116">Returns a unique identifier to the constant.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ef9a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ef9a-117">Requirements</span></span>



| <span data-ttu-id="3ef9a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ef9a-118">Requirement</span></span> | <span data-ttu-id="3ef9a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3ef9a-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ef9a-120">Header</span><span class="sxs-lookup"><span data-stu-id="3ef9a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="3ef9a-121"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ef9a-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="3ef9a-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3ef9a-122">Library</span></span><br/> | <dl> <span data-ttu-id="3ef9a-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ef9a-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3ef9a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ef9a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ef9a-125">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="3ef9a-125">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
