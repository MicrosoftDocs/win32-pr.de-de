---
description: Definiert das Vertex-Datenlayout. Jeder Scheitelpunkt kann einen oder mehrere Datentypen enthalten, und jeder Datentyp wird von einem Vertex-Element beschrieben.
ms.assetid: 6f3c40a0-b28e-48d6-acad-ef80a919c5d7
title: D3DVERTEXELEMENT9-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXELEMENT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e6c5e9508185124673ca7464b31d741cdf8035c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354387"
---
# <a name="d3dvertexelement9-structure"></a><span data-ttu-id="4e787-104">D3DVERTEXELEMENT9-Struktur</span><span class="sxs-lookup"><span data-stu-id="4e787-104">D3DVERTEXELEMENT9 structure</span></span>

<span data-ttu-id="4e787-105">Definiert das Vertex-Datenlayout.</span><span class="sxs-lookup"><span data-stu-id="4e787-105">Defines the vertex data layout.</span></span> <span data-ttu-id="4e787-106">Jeder Scheitelpunkt kann einen oder mehrere Datentypen enthalten, und jeder Datentyp wird von einem Vertex-Element beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4e787-106">Each vertex can contain one or more data types, and each data type is described by a vertex element.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e787-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e787-107">Syntax</span></span>


```C++
typedef struct D3DVERTEXELEMENT9 {
  WORD Stream;
  WORD Offset;
  BYTE Type;
  BYTE Method;
  BYTE Usage;
  BYTE UsageIndex;
} D3DVERTEXELEMENT9, *LPD3DVERTEXELEMENT9;
```



## <a name="members"></a><span data-ttu-id="4e787-108">Member</span><span class="sxs-lookup"><span data-stu-id="4e787-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4e787-109">**Datenstrom**</span><span class="sxs-lookup"><span data-stu-id="4e787-109">**Stream**</span></span>
</dt> <dd>

<span data-ttu-id="4e787-110">Typ: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e787-110">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4e787-111">Die streamnummer.</span><span class="sxs-lookup"><span data-stu-id="4e787-111">Stream number.</span></span>

</dd> <dt>

<span data-ttu-id="4e787-112">**Offset**</span><span class="sxs-lookup"><span data-stu-id="4e787-112">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="4e787-113">Typ: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e787-113">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4e787-114">Offset vom Anfang der Scheitelpunkt Daten zu den Daten, die dem jeweiligen Datentyp zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4e787-114">Offset from the beginning of the vertex data to the data associated with the particular data type.</span></span>

</dd> <dt>

<span data-ttu-id="4e787-115">**Type**</span><span class="sxs-lookup"><span data-stu-id="4e787-115">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="4e787-116">Type: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e787-116">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4e787-117">Der als [**D3DDECLTYPE**](./d3ddecltype.md)angegebene Datentyp.</span><span class="sxs-lookup"><span data-stu-id="4e787-117">The data type, specified as a [**D3DDECLTYPE**](./d3ddecltype.md).</span></span> <span data-ttu-id="4e787-118">Einer von mehreren vordefinierten Typen, die die Datengröße definieren.</span><span class="sxs-lookup"><span data-stu-id="4e787-118">One of several predefined types that define the data size.</span></span> <span data-ttu-id="4e787-119">Einige Methoden haben einen impliziten Typ.</span><span class="sxs-lookup"><span data-stu-id="4e787-119">Some methods have an implied type.</span></span>

</dd> <dt>

<span data-ttu-id="4e787-120">**Methode**</span><span class="sxs-lookup"><span data-stu-id="4e787-120">**Method**</span></span>
</dt> <dd>

<span data-ttu-id="4e787-121">Type: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e787-121">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4e787-122">Die-Methode gibt die Verarbeitung von Mosaik Operatoren an, die bestimmt, wie der Mosaik Prozess die Scheitelpunkt Daten interpretiert (oder verarbeitet).</span><span class="sxs-lookup"><span data-stu-id="4e787-122">The method specifies the tessellator processing, which determines how the tessellator interprets (or operates on) the vertex data.</span></span> <span data-ttu-id="4e787-123">Weitere Informationen finden Sie unter [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span><span class="sxs-lookup"><span data-stu-id="4e787-123">For more information, see [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e787-124">**Verwendung**</span><span class="sxs-lookup"><span data-stu-id="4e787-124">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="4e787-125">Type: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e787-125">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4e787-126">Definiert, wofür die Daten verwendet werden. Das heißt, die Interoperabilität zwischen Scheitelpunkt Daten Layouts und Vertex-Shadern.</span><span class="sxs-lookup"><span data-stu-id="4e787-126">Defines what the data will be used for; that is, the interoperability between vertex data layouts and vertex shaders.</span></span> <span data-ttu-id="4e787-127">Jede Verwendung dient zum Binden einer Scheitelpunkt Deklaration an einen Scheitelpunkt-Shader.</span><span class="sxs-lookup"><span data-stu-id="4e787-127">Each usage acts to bind a vertex declaration to a vertex shader.</span></span> <span data-ttu-id="4e787-128">In einigen Fällen haben Sie eine spezielle Interpretation.</span><span class="sxs-lookup"><span data-stu-id="4e787-128">In some cases, they have a special interpretation.</span></span> <span data-ttu-id="4e787-129">Beispielsweise wird ein Element, das die Position "D3DDECLUSAGE normal" oder "D3DDECLUSAGE" angibt, \_ \_ vom N-Patch-Mosaik Prozess verwendet, um das Mosaik zu richten.</span><span class="sxs-lookup"><span data-stu-id="4e787-129">For example, an element that specifies D3DDECLUSAGE\_NORMAL or D3DDECLUSAGE\_POSITION is used by the N-patch tessellator to set up tessellation.</span></span> <span data-ttu-id="4e787-130">Eine Liste der verfügbaren Semantik finden Sie unter [**D3DDECLUSAGE**](./d3ddeclusage.md) .</span><span class="sxs-lookup"><span data-stu-id="4e787-130">See [**D3DDECLUSAGE**](./d3ddeclusage.md) for a list of the available semantics.</span></span> <span data-ttu-id="4e787-131">D3DDECLUSAGE \_ texcoord kann für benutzerdefinierte Felder verwendet werden (für die keine vorhandene Verwendung definiert ist).</span><span class="sxs-lookup"><span data-stu-id="4e787-131">D3DDECLUSAGE\_TEXCOORD can be used for user-defined fields (which don't have an existing usage defined).</span></span>

</dd> <dt>

<span data-ttu-id="4e787-132">**Start Index**</span><span class="sxs-lookup"><span data-stu-id="4e787-132">**UsageIndex**</span></span>
</dt> <dd>

<span data-ttu-id="4e787-133">Type: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e787-133">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4e787-134">Ändert die Verwendungs Daten, um dem Benutzer das Angeben mehrerer Verwendungs Typen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="4e787-134">Modifies the usage data to allow the user to specify multiple usage types.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e787-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e787-135">Remarks</span></span>

<span data-ttu-id="4e787-136">Vertex-Daten werden mit einem Array von **D3DVERTEXELEMENT9** -Strukturen definiert.</span><span class="sxs-lookup"><span data-stu-id="4e787-136">Vertex data is defined using an array of **D3DVERTEXELEMENT9** structures.</span></span> <span data-ttu-id="4e787-137">Verwenden Sie [**D3DDECL \_ End**](d3ddecl-end.md) , um das letzte Element in der Deklaration zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="4e787-137">Use [**D3DDECL\_END**](d3ddecl-end.md) to declare the last element in the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e787-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e787-138">Requirements</span></span>



| <span data-ttu-id="4e787-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e787-139">Requirement</span></span> | <span data-ttu-id="4e787-140">Wert</span><span class="sxs-lookup"><span data-stu-id="4e787-140">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e787-141">Header</span><span class="sxs-lookup"><span data-stu-id="4e787-141">Header</span></span><br/> | <dl> <span data-ttu-id="4e787-142"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e787-142"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e787-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e787-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e787-144">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="4e787-144">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="4e787-145">Vertex-Deklaration (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4e787-145">Vertex Declaration (Direct3D 9)</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
