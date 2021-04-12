---
description: D3DXSHADER \_ constantinfo-Struktur
ms.assetid: 0c42cea7-559e-4475-b66a-e932a9cb42de
title: D3DXSHADER_CONSTANTINFO-Struktur (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: e90c0085035e78b9bc3ce1c48642157d8badc924
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219496"
---
# <a name="d3dxshader_constantinfo-structure"></a><span data-ttu-id="f0345-103">D3DXSHADER \_ constantinfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="f0345-103">D3DXSHADER\_CONSTANTINFO structure</span></span>

## <a name="syntax"></a><span data-ttu-id="f0345-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0345-104">Syntax</span></span>


```C++
typedef struct D3DXSHADER_CONSTANTINFO {
  DWORD Name;
  WORD  RegisterSet;
  WORD  RegisterIndex;
  WORD  RegisterCount;
  WORD  Reserved;
  DWORD TypeInfo;
  DWORD DefaultValue;
} D3DXSHADER_CONSTANTINFO, *LPD3DXSHADER_CONSTANTINFO;
```



## <a name="members"></a><span data-ttu-id="f0345-105">Member</span><span class="sxs-lookup"><span data-stu-id="f0345-105">Members</span></span>

<dl> <dt>

<span data-ttu-id="f0345-106">**Name**</span><span class="sxs-lookup"><span data-stu-id="f0345-106">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="f0345-107">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0345-107">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0345-108">Offset vom Anfang dieser Struktur in Bytes zur Zeichenfolge, die die Konstanten Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="f0345-108">Offset from the beginning of this structure, in bytes, to the string that contains the constant information.</span></span>

</dd> <dt>

<span data-ttu-id="f0345-109">**Register Set**</span><span class="sxs-lookup"><span data-stu-id="f0345-109">**RegisterSet**</span></span>
</dt> <dd>

<span data-ttu-id="f0345-110">Typ: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0345-110">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0345-111">Register Satz.</span><span class="sxs-lookup"><span data-stu-id="f0345-111">Register set.</span></span> <span data-ttu-id="f0345-112">Siehe [**D3DXREGISTER \_ set**](./d3dxregister-set.md).</span><span class="sxs-lookup"><span data-stu-id="f0345-112">See [**D3DXREGISTER\_SET**](./d3dxregister-set.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0345-113">**Register Index**</span><span class="sxs-lookup"><span data-stu-id="f0345-113">**RegisterIndex**</span></span>
</dt> <dd>

<span data-ttu-id="f0345-114">Typ: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0345-114">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0345-115">Der Registrierungs Index.</span><span class="sxs-lookup"><span data-stu-id="f0345-115">The register index.</span></span>

</dd> <dt>

<span data-ttu-id="f0345-116">**Register count**</span><span class="sxs-lookup"><span data-stu-id="f0345-116">**RegisterCount**</span></span>
</dt> <dd>

<span data-ttu-id="f0345-117">Typ: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0345-117">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0345-118">Anzahl der Register.</span><span class="sxs-lookup"><span data-stu-id="f0345-118">Number of registers.</span></span>

</dd> <dt>

<span data-ttu-id="f0345-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="f0345-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="f0345-120">Typ: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0345-120">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0345-121">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="f0345-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f0345-122">**TypeInfo**</span><span class="sxs-lookup"><span data-stu-id="f0345-122">**TypeInfo**</span></span>
</dt> <dd>

<span data-ttu-id="f0345-123">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0345-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0345-124">Offset vom Anfang dieser Struktur in Bytes zur Zeichenfolge, die die [**D3DXSHADER \_ TypeInfo**](d3dxshader-typeinfo.md) -Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="f0345-124">Offset from the beginning of this structure, in bytes, to the string that contains the [**D3DXSHADER\_TYPEINFO**](d3dxshader-typeinfo.md) information.</span></span>

</dd> <dt>

<span data-ttu-id="f0345-125">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="f0345-125">**DefaultValue**</span></span>
</dt> <dd>

<span data-ttu-id="f0345-126">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0345-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0345-127">Offset vom Anfang dieser-Struktur in Bytes zur Zeichenfolge, die den Standardwert enthält.</span><span class="sxs-lookup"><span data-stu-id="f0345-127">Offset from the beginning of this structure, in bytes, to the string that contains the default value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0345-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0345-128">Requirements</span></span>



| <span data-ttu-id="f0345-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0345-129">Requirement</span></span> | <span data-ttu-id="f0345-130">Wert</span><span class="sxs-lookup"><span data-stu-id="f0345-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0345-131">Header</span><span class="sxs-lookup"><span data-stu-id="f0345-131">Header</span></span><br/> | <dl> <span data-ttu-id="f0345-132"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0345-132"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0345-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0345-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0345-134">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f0345-134">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
