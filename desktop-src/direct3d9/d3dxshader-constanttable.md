---
description: Hilfsstruktur zum Verwalten einer shaderkonstantentabelle. Dies kann auch mithilfe von ID3DXConstantTable erfolgen.
ms.assetid: cc6d66e4-c600-420b-b7b5-1bd10ecb22f9
title: D3DXSHADER_CONSTANTTABLE-Struktur (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTTABLE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: ef4fe6cf9af924d9ae6c358f72bf49f93d85f29d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367363"
---
# <a name="d3dxshader_constanttable-structure"></a><span data-ttu-id="db662-104">D3DXSHADER \_ constanables-Struktur</span><span class="sxs-lookup"><span data-stu-id="db662-104">D3DXSHADER\_CONSTANTTABLE structure</span></span>

<span data-ttu-id="db662-105">Hilfsstruktur zum Verwalten einer shaderkonstantentabelle.</span><span class="sxs-lookup"><span data-stu-id="db662-105">Helper structure for managing a shader constant table.</span></span> <span data-ttu-id="db662-106">Dies kann auch mithilfe von [**ID3DXConstantTable**](id3dxconstanttable.md)erfolgen.</span><span class="sxs-lookup"><span data-stu-id="db662-106">This can also be done using [**ID3DXConstantTable**](id3dxconstanttable.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="db662-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="db662-107">Syntax</span></span>


```C++
typedef struct D3DXSHADER_CONSTANTTABLE {
  DWORD Size;
  DWORD Creator;
  DWORD Version;
  DWORD Constants;
  DWORD ConstantInfo;
  DWORD Flags;
  DWORD Target;
} D3DXSHADER_CONSTANTTABLE, *LPD3DXSHADER_CONSTANTTABLE;
```



## <a name="members"></a><span data-ttu-id="db662-108">Member</span><span class="sxs-lookup"><span data-stu-id="db662-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="db662-109">**Größe**</span><span class="sxs-lookup"><span data-stu-id="db662-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="db662-110">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db662-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="db662-111">Größe der Struktur.</span><span class="sxs-lookup"><span data-stu-id="db662-111">Size of the structure.</span></span> <span data-ttu-id="db662-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="db662-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="db662-113">**Creator**</span><span class="sxs-lookup"><span data-stu-id="db662-113">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="db662-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db662-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="db662-115">Offset vom Anfang dieser-Struktur in Bytes zur Zeichenfolge, die den Namen des Erstellers enthält.</span><span class="sxs-lookup"><span data-stu-id="db662-115">Offset from the beginning of this structure, in bytes, to the string that contains the name of the creator.</span></span>

</dd> <dt>

<span data-ttu-id="db662-116">**Version**</span><span class="sxs-lookup"><span data-stu-id="db662-116">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="db662-117">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db662-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="db662-118">Shader-Version.</span><span class="sxs-lookup"><span data-stu-id="db662-118">Shader version.</span></span>

</dd> <dt>

<span data-ttu-id="db662-119">**Konstanten**</span><span class="sxs-lookup"><span data-stu-id="db662-119">**Constants**</span></span>
</dt> <dd>

<span data-ttu-id="db662-120">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db662-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="db662-121">Anzahl der Konstanten.</span><span class="sxs-lookup"><span data-stu-id="db662-121">Number of constants.</span></span>

</dd> <dt>

<span data-ttu-id="db662-122">**Constantinfo**</span><span class="sxs-lookup"><span data-stu-id="db662-122">**ConstantInfo**</span></span>
</dt> <dd>

<span data-ttu-id="db662-123">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db662-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="db662-124">Array konstanter Informationen, D3DXSHADER \_ constantinfo \[ *Konstanten* \] .</span><span class="sxs-lookup"><span data-stu-id="db662-124">Array of constant information, D3DXSHADER\_CONSTANTINFO\[*Constants*\].</span></span> <span data-ttu-id="db662-125">Weitere Informationen finden Sie unter [**D3DXSHADER \_ constantinfo**](d3dxshader-constantinfo.md).</span><span class="sxs-lookup"><span data-stu-id="db662-125">See [**D3DXSHADER\_CONSTANTINFO**](d3dxshader-constantinfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="db662-126">**Flags**</span><span class="sxs-lookup"><span data-stu-id="db662-126">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="db662-127">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db662-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="db662-128">Die [D3DXSHADER Flags](d3dxshader-flags.md) -Flags, mit denen der Shader kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="db662-128">The [D3DXSHADER Flags](d3dxshader-flags.md) flags used to compile the shader.</span></span>

</dd> <dt>

<span data-ttu-id="db662-129">**Target**</span><span class="sxs-lookup"><span data-stu-id="db662-129">**Target**</span></span>
</dt> <dd>

<span data-ttu-id="db662-130">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db662-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="db662-131">Offset in der Zeichenfolge, die das Ziel enthält.</span><span class="sxs-lookup"><span data-stu-id="db662-131">Offset into the string that contains the target.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db662-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db662-132">Remarks</span></span>

<span data-ttu-id="db662-133">Shader-konstanteninformationen sind in einer durch Tabstopps getrennten Tabelle mit Kommentaren enthalten.</span><span class="sxs-lookup"><span data-stu-id="db662-133">Shader constant information is included in a tab-delimited table of comments.</span></span> <span data-ttu-id="db662-134">Alle Offsets werden in Bytes vom Anfang der Struktur gemessen.</span><span class="sxs-lookup"><span data-stu-id="db662-134">All offsets are measured in bytes from the beginning of the structure.</span></span> <span data-ttu-id="db662-135">Einträge in der Konstanten Tabelle werden nach Ersteller in aufsteigender Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="db662-135">Entries in the constant table are sorted by Creator in ascending order.</span></span>

<span data-ttu-id="db662-136">Eine Shader-Konstante Tabelle kann mit den [**ID3DXConstantTable**](id3dxconstanttable.md) -Schnittstellen verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="db662-136">A shader constant table can be managed with the [**ID3DXConstantTable**](id3dxconstanttable.md) interfaces.</span></span> <span data-ttu-id="db662-137">Alternativ dazu können Sie die Konstante Tabelle mit **D3DXSHADER \_ CONSTAN/verwalten**.</span><span class="sxs-lookup"><span data-stu-id="db662-137">Alternatively, you can manage the constant table with **D3DXSHADER\_CONSTANTTABLE**.</span></span>

<span data-ttu-id="db662-138">Dieses Größen Element wird häufig mit folgendem initialisiert:</span><span class="sxs-lookup"><span data-stu-id="db662-138">This size member is often initialized using the following:</span></span>


```
D3DXSHADER_CONSTANTTABLE constantTable;
constantTable.Size = sizeof(D3DXSHADER_CONSTANTTABLE)
```



## <a name="requirements"></a><span data-ttu-id="db662-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db662-139">Requirements</span></span>



| <span data-ttu-id="db662-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db662-140">Requirement</span></span> | <span data-ttu-id="db662-141">Wert</span><span class="sxs-lookup"><span data-stu-id="db662-141">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="db662-142">Header</span><span class="sxs-lookup"><span data-stu-id="db662-142">Header</span></span><br/> | <dl> <span data-ttu-id="db662-143"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="db662-143"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db662-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db662-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db662-145">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="db662-145">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="db662-146">**D3DXGetShaderConstantTable**</span><span class="sxs-lookup"><span data-stu-id="db662-146">**D3DXGetShaderConstantTable**</span></span>](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
