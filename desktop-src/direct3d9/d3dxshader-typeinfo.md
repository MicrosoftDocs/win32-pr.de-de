---
description: Eine hilfsstruktur, die Member-Typinformationen enthält.
ms.assetid: 5580122d-c700-4632-8fcf-903519f2429e
title: D3DXSHADER_TYPEINFO-Struktur (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_TYPEINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 71b9cc893cdcfdc9802aca173627cd9da4f9ca4b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354716"
---
# <a name="d3dxshader_typeinfo-structure"></a><span data-ttu-id="463a1-103">D3DXSHADER \_ TypInfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="463a1-103">D3DXSHADER\_TYPEINFO structure</span></span>

<span data-ttu-id="463a1-104">Eine hilfsstruktur, die Member-Typinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="463a1-104">A helper structure containing member type information.</span></span>

## <a name="syntax"></a><span data-ttu-id="463a1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="463a1-105">Syntax</span></span>


```C++
typedef struct D3DXSHADER_TYPEINFO {
  WORD  Class;
  WORD  Type;
  WORD  Rows;
  WORD  Columns;
  WORD  Elements;
  WORD  StructMembers;
  DWORD StructMemberInfo;
} D3DXSHADER_TYPEINFO, *LPD3DXSHADER_TYPEINFO;
```



## <a name="members"></a><span data-ttu-id="463a1-106">Member</span><span class="sxs-lookup"><span data-stu-id="463a1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="463a1-107">**Klasse**</span><span class="sxs-lookup"><span data-stu-id="463a1-107">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="463a1-108">Typ: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="463a1-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="463a1-109">Shader-Objekttyp.</span><span class="sxs-lookup"><span data-stu-id="463a1-109">Shader object type.</span></span> <span data-ttu-id="463a1-110">Siehe [**D3DXPARAMETER- \_ Klasse**](./d3dxparameter-class.md).</span><span class="sxs-lookup"><span data-stu-id="463a1-110">See [**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="463a1-111">**Type**</span><span class="sxs-lookup"><span data-stu-id="463a1-111">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="463a1-112">Typ: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="463a1-112">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="463a1-113">Datentyp.</span><span class="sxs-lookup"><span data-stu-id="463a1-113">Data type.</span></span> <span data-ttu-id="463a1-114">Siehe [**D3DXPARAMETER \_ Type**](./d3dxparameter-type.md).</span><span class="sxs-lookup"><span data-stu-id="463a1-114">See [**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="463a1-115">**Zeilen**</span><span class="sxs-lookup"><span data-stu-id="463a1-115">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="463a1-116">Typ: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="463a1-116">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="463a1-117">Anzahl von Matrix Zeilen (Matrizen).</span><span class="sxs-lookup"><span data-stu-id="463a1-117">Number of matrix rows (matrices).</span></span>

</dd> <dt>

<span data-ttu-id="463a1-118">**Spalten**</span><span class="sxs-lookup"><span data-stu-id="463a1-118">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="463a1-119">Typ: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="463a1-119">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="463a1-120">Anzahl der Spalten (Vektoren und Matrizen).</span><span class="sxs-lookup"><span data-stu-id="463a1-120">Number of columns (vectors and matrices).</span></span>

</dd> <dt>

<span data-ttu-id="463a1-121">**Elemente**</span><span class="sxs-lookup"><span data-stu-id="463a1-121">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="463a1-122">Typ: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="463a1-122">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="463a1-123">Array Dimension.</span><span class="sxs-lookup"><span data-stu-id="463a1-123">Array dimension.</span></span>

</dd> <dt>

<span data-ttu-id="463a1-124">**Structmembers**</span><span class="sxs-lookup"><span data-stu-id="463a1-124">**StructMembers**</span></span>
</dt> <dd>

<span data-ttu-id="463a1-125">Typ: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="463a1-125">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="463a1-126">Anzahl von Strukturmembern.</span><span class="sxs-lookup"><span data-stu-id="463a1-126">Number of structure members.</span></span>

</dd> <dt>

<span data-ttu-id="463a1-127">**Structmembership Info**</span><span class="sxs-lookup"><span data-stu-id="463a1-127">**StructMemberInfo**</span></span>
</dt> <dd>

<span data-ttu-id="463a1-128">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="463a1-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="463a1-129">Array von Strukturmember-Informationen, D3DXSHADER \_ structmembership Info \[ *structmembers* \] .</span><span class="sxs-lookup"><span data-stu-id="463a1-129">Array of structure member information, D3DXSHADER\_STRUCTMEMBERINFO\[*StructMembers*\].</span></span> <span data-ttu-id="463a1-130">Weitere Informationen finden Sie unter [**D3DXSHADER \_ structmembership Info**](d3dxshader-structmemberinfo.md).</span><span class="sxs-lookup"><span data-stu-id="463a1-130">See [**D3DXSHADER\_STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="463a1-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="463a1-131">Remarks</span></span>

<span data-ttu-id="463a1-132">Die Typinformationen sind Teil von [**D3DXSHADER \_ structmembership Info**](d3dxshader-structmemberinfo.md).</span><span class="sxs-lookup"><span data-stu-id="463a1-132">The type information is part of [**D3DXSHADER\_STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="463a1-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="463a1-133">Requirements</span></span>



| <span data-ttu-id="463a1-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="463a1-134">Requirement</span></span> | <span data-ttu-id="463a1-135">Wert</span><span class="sxs-lookup"><span data-stu-id="463a1-135">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="463a1-136">Header</span><span class="sxs-lookup"><span data-stu-id="463a1-136">Header</span></span><br/> | <dl> <span data-ttu-id="463a1-137"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="463a1-137"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="463a1-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="463a1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="463a1-139">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="463a1-139">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="463a1-140">**D3DXSHADER \_ constantinfo**</span><span class="sxs-lookup"><span data-stu-id="463a1-140">**D3DXSHADER\_CONSTANTINFO**</span></span>](d3dxshader-constantinfo.md)
</dt> </dl>

 

 
