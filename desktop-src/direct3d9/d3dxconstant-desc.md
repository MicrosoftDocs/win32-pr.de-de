---
description: Eine Beschreibung einer Konstante in einer Konstanten Tabelle.
ms.assetid: d1970536-7195-4270-a1b9-b082ebe4f17f
title: D3DXCONSTANT_DESC-Struktur (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: d737fa1d95a119668602aeb056e15bc4248200aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370464"
---
# <a name="d3dxconstant_desc-structure"></a><span data-ttu-id="88b61-103">D3DXCONSTANT- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="88b61-103">D3DXCONSTANT\_DESC structure</span></span>

<span data-ttu-id="88b61-104">Eine Beschreibung einer Konstante in einer Konstanten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="88b61-104">A description of a constant in a constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="88b61-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="88b61-105">Syntax</span></span>


```C++
typedef struct D3DXCONSTANT_DESC {
  LPCSTR              Name;
  D3DXREGISTER_SET    RegisterSet;
  UINT                RegisterIndex;
  UINT                RegisterCount;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                StructMembers;
  UINT                Bytes;
  LPCVOID             DefaultValue;
} D3DXCONSTANT_DESC, *LPD3DXCONSTANT_DESC;
```



## <a name="members"></a><span data-ttu-id="88b61-106">Member</span><span class="sxs-lookup"><span data-stu-id="88b61-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="88b61-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="88b61-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="88b61-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="88b61-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="88b61-109">Der Name der Konstanten.</span><span class="sxs-lookup"><span data-stu-id="88b61-109">Name of the constant.</span></span>

</dd> <dt>

<span data-ttu-id="88b61-110">**Register Set**</span><span class="sxs-lookup"><span data-stu-id="88b61-110">**RegisterSet**</span></span>
</dt> <dd>

<span data-ttu-id="88b61-111">Typ: **[ **D3DXREGISTER \_ set**](./d3dxregister-set.md)**</span><span class="sxs-lookup"><span data-stu-id="88b61-111">Type: **[**D3DXREGISTER\_SET**](./d3dxregister-set.md)**</span></span>

</dd> <dd>

<span data-ttu-id="88b61-112">Konstanter Datentyp.</span><span class="sxs-lookup"><span data-stu-id="88b61-112">Constant data type.</span></span> <span data-ttu-id="88b61-113">Siehe [**D3DXREGISTER \_ set**](./d3dxregister-set.md).</span><span class="sxs-lookup"><span data-stu-id="88b61-113">See [**D3DXREGISTER\_SET**](./d3dxregister-set.md).</span></span>

</dd> <dt>

<span data-ttu-id="88b61-114">**Register Index**</span><span class="sxs-lookup"><span data-stu-id="88b61-114">**RegisterIndex**</span></span>
</dt> <dd>

<span data-ttu-id="88b61-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="88b61-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="88b61-116">NULL basierter Index der Konstante in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="88b61-116">Zero-based index of the constant in the table.</span></span>

</dd> <dt>

<span data-ttu-id="88b61-117">**Register count**</span><span class="sxs-lookup"><span data-stu-id="88b61-117">**RegisterCount**</span></span>
</dt> <dd>

<span data-ttu-id="88b61-118">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="88b61-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="88b61-119">Anzahl der Register, die Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="88b61-119">Number of registers that contain data.</span></span>

</dd> <dt>

<span data-ttu-id="88b61-120">**Klasse**</span><span class="sxs-lookup"><span data-stu-id="88b61-120">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="88b61-121">Type: **[ **D3DXPARAMETER- \_ Klasse**](./d3dxparameter-class.md)**</span><span class="sxs-lookup"><span data-stu-id="88b61-121">Type: **[**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md)**</span></span>

</dd> <dd>

<span data-ttu-id="88b61-122">Parameter Klasse.</span><span class="sxs-lookup"><span data-stu-id="88b61-122">Parameter class.</span></span> <span data-ttu-id="88b61-123">Siehe [**D3DXPARAMETER- \_ Klasse**](./d3dxparameter-class.md).</span><span class="sxs-lookup"><span data-stu-id="88b61-123">See [**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="88b61-124">**Type**</span><span class="sxs-lookup"><span data-stu-id="88b61-124">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="88b61-125">Type: **[ **D3DXPARAMETER- \_ Typ**](./d3dxparameter-type.md)**</span><span class="sxs-lookup"><span data-stu-id="88b61-125">Type: **[**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="88b61-126">Der Parametertyp.</span><span class="sxs-lookup"><span data-stu-id="88b61-126">Parameter type.</span></span> <span data-ttu-id="88b61-127">Siehe [**D3DXPARAMETER \_ Type**](./d3dxparameter-type.md).</span><span class="sxs-lookup"><span data-stu-id="88b61-127">See [**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="88b61-128">**Zeilen**</span><span class="sxs-lookup"><span data-stu-id="88b61-128">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="88b61-129">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="88b61-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="88b61-130">Anzahl von Zeilen.</span><span class="sxs-lookup"><span data-stu-id="88b61-130">Number of rows.</span></span>

</dd> <dt>

<span data-ttu-id="88b61-131">**Spalten**</span><span class="sxs-lookup"><span data-stu-id="88b61-131">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="88b61-132">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="88b61-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="88b61-133">Anzahl der Spalten.</span><span class="sxs-lookup"><span data-stu-id="88b61-133">Number of columns.</span></span>

</dd> <dt>

<span data-ttu-id="88b61-134">**Elemente**</span><span class="sxs-lookup"><span data-stu-id="88b61-134">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="88b61-135">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="88b61-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="88b61-136">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="88b61-136">Number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="88b61-137">**Structmembers**</span><span class="sxs-lookup"><span data-stu-id="88b61-137">**StructMembers**</span></span>
</dt> <dd>

<span data-ttu-id="88b61-138">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="88b61-138">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="88b61-139">Anzahl der unter Parameter für Strukturmember.</span><span class="sxs-lookup"><span data-stu-id="88b61-139">Number of structure member sub-parameters.</span></span>

</dd> <dt>

<span data-ttu-id="88b61-140">**Byte**</span><span class="sxs-lookup"><span data-stu-id="88b61-140">**Bytes**</span></span>
</dt> <dd>

<span data-ttu-id="88b61-141">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="88b61-141">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="88b61-142">Datengröße in Byte Anzahl.</span><span class="sxs-lookup"><span data-stu-id="88b61-142">Data size in number of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="88b61-143">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="88b61-143">**DefaultValue**</span></span>
</dt> <dd>

<span data-ttu-id="88b61-144">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="88b61-144">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="88b61-145">Zeiger auf den Standardwert.</span><span class="sxs-lookup"><span data-stu-id="88b61-145">Pointer to the default value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88b61-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88b61-146">Requirements</span></span>



| <span data-ttu-id="88b61-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88b61-147">Requirement</span></span> | <span data-ttu-id="88b61-148">Wert</span><span class="sxs-lookup"><span data-stu-id="88b61-148">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b61-149">Header</span><span class="sxs-lookup"><span data-stu-id="88b61-149">Header</span></span><br/> | <dl> <span data-ttu-id="88b61-150"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="88b61-150"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88b61-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88b61-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88b61-152">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="88b61-152">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="88b61-153">**D3DXCONSTANTTABLE- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="88b61-153">**D3DXCONSTANTTABLE\_DESC**</span></span>](d3dxconstanttable-desc.md)
</dt> </dl>

 

 
