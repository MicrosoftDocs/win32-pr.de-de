---
description: Beschreibt einen Parameter, der für ein Effect-Objekt verwendet wird.
ms.assetid: 60d19b52-67ef-4903-bbde-922a8fac1ad8
title: D3DXPARAMETER_DESC-Struktur (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 2256e24daa6dc8b6e5da1528e9a5e5aefce8ec99
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219437"
---
# <a name="d3dxparameter_desc-structure"></a><span data-ttu-id="54bcf-103">D3DXPARAMETER- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="54bcf-103">D3DXPARAMETER\_DESC structure</span></span>

<span data-ttu-id="54bcf-104">Beschreibt einen Parameter, der für ein Effect-Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="54bcf-104">Describes a parameter used for an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="54bcf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="54bcf-105">Syntax</span></span>


```C++
typedef struct D3DXPARAMETER_DESC {
  LPCSTR              Name;
  LPCSTR              Semantic;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                Annotations;
  UINT                StructMembers;
  DWORD               Flags;
  UINT                Bytes;
} D3DXPARAMETER_DESC, *LPD3DXPARAMETER_DESC;
```



## <a name="members"></a><span data-ttu-id="54bcf-106">Member</span><span class="sxs-lookup"><span data-stu-id="54bcf-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="54bcf-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="54bcf-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="54bcf-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54bcf-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="54bcf-109">Der Name des Parameters.</span><span class="sxs-lookup"><span data-stu-id="54bcf-109">Name of the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="54bcf-110">**Tischer**</span><span class="sxs-lookup"><span data-stu-id="54bcf-110">**Semantic**</span></span>
</dt> <dd>

<span data-ttu-id="54bcf-111">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54bcf-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="54bcf-112">Semantik Bedeutung, auch als Verwendung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="54bcf-112">Semantic meaning, also called the usage.</span></span>

</dd> <dt>

<span data-ttu-id="54bcf-113">**Klasse**</span><span class="sxs-lookup"><span data-stu-id="54bcf-113">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="54bcf-114">Type: **[ **D3DXPARAMETER- \_ Klasse**](./d3dxparameter-class.md)**</span><span class="sxs-lookup"><span data-stu-id="54bcf-114">Type: **[**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md)**</span></span>

</dd> <dd>

<span data-ttu-id="54bcf-115">Parameter Klasse.</span><span class="sxs-lookup"><span data-stu-id="54bcf-115">Parameter class.</span></span> <span data-ttu-id="54bcf-116">Legen Sie diesen Wert auf einen der Werte in der [**D3DXPARAMETER- \_ Klasse**](./d3dxparameter-class.md)fest.</span><span class="sxs-lookup"><span data-stu-id="54bcf-116">Set this to one of the values in [**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="54bcf-117">**Type**</span><span class="sxs-lookup"><span data-stu-id="54bcf-117">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="54bcf-118">Type: **[ **D3DXPARAMETER- \_ Typ**](./d3dxparameter-type.md)**</span><span class="sxs-lookup"><span data-stu-id="54bcf-118">Type: **[**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="54bcf-119">Der Parametertyp.</span><span class="sxs-lookup"><span data-stu-id="54bcf-119">Parameter type.</span></span> <span data-ttu-id="54bcf-120">Legen Sie diesen Wert auf einen der Werte in [**D3DXPARAMETER \_ Type**](./d3dxparameter-type.md)fest.</span><span class="sxs-lookup"><span data-stu-id="54bcf-120">Set this to one of the values in [**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="54bcf-121">**Zeilen**</span><span class="sxs-lookup"><span data-stu-id="54bcf-121">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="54bcf-122">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54bcf-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="54bcf-123">Anzahl der Zeilen im Array.</span><span class="sxs-lookup"><span data-stu-id="54bcf-123">Number of rows in the array.</span></span>

</dd> <dt>

<span data-ttu-id="54bcf-124">**Spalten**</span><span class="sxs-lookup"><span data-stu-id="54bcf-124">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="54bcf-125">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54bcf-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="54bcf-126">Anzahl der Spalten im Array.</span><span class="sxs-lookup"><span data-stu-id="54bcf-126">Number of columns in the array.</span></span>

</dd> <dt>

<span data-ttu-id="54bcf-127">**Elemente**</span><span class="sxs-lookup"><span data-stu-id="54bcf-127">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="54bcf-128">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54bcf-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="54bcf-129">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="54bcf-129">Number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="54bcf-130">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="54bcf-130">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="54bcf-131">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54bcf-131">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="54bcf-132">Anzahl der Anmerkungen.</span><span class="sxs-lookup"><span data-stu-id="54bcf-132">Number of annotations.</span></span>

</dd> <dt>

<span data-ttu-id="54bcf-133">**Structmembers**</span><span class="sxs-lookup"><span data-stu-id="54bcf-133">**StructMembers**</span></span>
</dt> <dd>

<span data-ttu-id="54bcf-134">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54bcf-134">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="54bcf-135">Anzahl von Strukturmembern.</span><span class="sxs-lookup"><span data-stu-id="54bcf-135">Number of structure members.</span></span>

</dd> <dt>

<span data-ttu-id="54bcf-136">**Flags**</span><span class="sxs-lookup"><span data-stu-id="54bcf-136">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="54bcf-137">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54bcf-137">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="54bcf-138">Parameter Attribute.</span><span class="sxs-lookup"><span data-stu-id="54bcf-138">Parameter attributes.</span></span> <span data-ttu-id="54bcf-139">Siehe [Wirkungs Konstanten](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="54bcf-139">See [Effect Constants](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="54bcf-140">**Byte**</span><span class="sxs-lookup"><span data-stu-id="54bcf-140">**Bytes**</span></span>
</dt> <dd>

<span data-ttu-id="54bcf-141">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54bcf-141">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="54bcf-142">Die Größe des Parameters in Byte.</span><span class="sxs-lookup"><span data-stu-id="54bcf-142">The size of the parameter, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="54bcf-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54bcf-143">Requirements</span></span>



| <span data-ttu-id="54bcf-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54bcf-144">Requirement</span></span> | <span data-ttu-id="54bcf-145">Wert</span><span class="sxs-lookup"><span data-stu-id="54bcf-145">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="54bcf-146">Header</span><span class="sxs-lookup"><span data-stu-id="54bcf-146">Header</span></span><br/> | <dl> <span data-ttu-id="54bcf-147"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="54bcf-147"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54bcf-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54bcf-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54bcf-149">Effekt Strukturen</span><span class="sxs-lookup"><span data-stu-id="54bcf-149">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
