---
description: Der Objekttyp.
ms.assetid: ab405984-2ebc-4514-9400-bdb13676eda5
title: D3DXPARAMETER_CLASS-Enumeration (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_CLASS
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: c42bfc9335c38de04ab484193a1e178a122f2210
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870083"
---
# <a name="d3dxparameter_class-enumeration"></a><span data-ttu-id="fcc5a-103">D3DXPARAMETER- \_ Klasse-Enumeration</span><span class="sxs-lookup"><span data-stu-id="fcc5a-103">D3DXPARAMETER\_CLASS enumeration</span></span>

<span data-ttu-id="fcc5a-104">Der Objekttyp.</span><span class="sxs-lookup"><span data-stu-id="fcc5a-104">The type of object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcc5a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcc5a-105">Syntax</span></span>


```C++
typedef enum D3DXPARAMETER_CLASS { 
  D3DXPC_SCALAR,
  D3DXPC_VECTOR,
  D3DXPC_MATRIX_ROWS,
  D3DXPC_MATRIX_COLUMNS,
  D3DXPC_OBJECT,
  D3DXPC_STRUCT,
  D3DXPC_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_CLASS, *LPD3DXPARAMETER_CLASS;
```



## <a name="constants"></a><span data-ttu-id="fcc5a-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="fcc5a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fcc5a-107"><span id="D3DXPC_SCALAR"></span><span id="d3dxpc_scalar"></span>**D3DXPC- \_ Skalar**</span><span class="sxs-lookup"><span data-stu-id="fcc5a-107"><span id="D3DXPC_SCALAR"></span><span id="d3dxpc_scalar"></span>**D3DXPC\_SCALAR**</span></span>
</dt> <dd>

<span data-ttu-id="fcc5a-108">Constant ist ein Skalar.</span><span class="sxs-lookup"><span data-stu-id="fcc5a-108">Constant is a scalar.</span></span>

</dd> <dt>

<span data-ttu-id="fcc5a-109"><span id="D3DXPC_VECTOR"></span><span id="d3dxpc_vector"></span>**D3DXPC- \_ Vektor**</span><span class="sxs-lookup"><span data-stu-id="fcc5a-109"><span id="D3DXPC_VECTOR"></span><span id="d3dxpc_vector"></span>**D3DXPC\_VECTOR**</span></span>
</dt> <dd>

<span data-ttu-id="fcc5a-110">Die Konstante ist ein Vektor.</span><span class="sxs-lookup"><span data-stu-id="fcc5a-110">Constant is a vector.</span></span>

</dd> <dt>

<span data-ttu-id="fcc5a-111"><span id="D3DXPC_MATRIX_ROWS"></span><span id="d3dxpc_matrix_rows"></span>**D3DXPC- \_ Matrix \_ Zeilen**</span><span class="sxs-lookup"><span data-stu-id="fcc5a-111"><span id="D3DXPC_MATRIX_ROWS"></span><span id="d3dxpc_matrix_rows"></span>**D3DXPC\_MATRIX\_ROWS**</span></span>
</dt> <dd>

<span data-ttu-id="fcc5a-112">Die Konstante ist eine Zeilen hauptmatrix.</span><span class="sxs-lookup"><span data-stu-id="fcc5a-112">Constant is a row major matrix.</span></span>

</dd> <dt>

<span data-ttu-id="fcc5a-113"><span id="D3DXPC_MATRIX_COLUMNS"></span><span id="d3dxpc_matrix_columns"></span>**D3DXPC- \_ Matrix \_ Spalten**</span><span class="sxs-lookup"><span data-stu-id="fcc5a-113"><span id="D3DXPC_MATRIX_COLUMNS"></span><span id="d3dxpc_matrix_columns"></span>**D3DXPC\_MATRIX\_COLUMNS**</span></span>
</dt> <dd>

<span data-ttu-id="fcc5a-114">Die Konstante ist eine Spalten hauptmatrix.</span><span class="sxs-lookup"><span data-stu-id="fcc5a-114">Constant is a column major matrix.</span></span>

</dd> <dt>

<span data-ttu-id="fcc5a-115"><span id="D3DXPC_OBJECT"></span><span id="d3dxpc_object"></span>**D3DXPC- \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="fcc5a-115"><span id="D3DXPC_OBJECT"></span><span id="d3dxpc_object"></span>**D3DXPC\_OBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="fcc5a-116">Constant ist entweder eine Textur, ein Shader oder eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="fcc5a-116">Constant is either a texture, shader, or a string.</span></span>

</dd> <dt>

<span data-ttu-id="fcc5a-117"><span id="D3DXPC_STRUCT"></span><span id="d3dxpc_struct"></span>**D3DXPC- \_ Struktur**</span><span class="sxs-lookup"><span data-stu-id="fcc5a-117"><span id="D3DXPC_STRUCT"></span><span id="d3dxpc_struct"></span>**D3DXPC\_STRUCT**</span></span>
</dt> <dd>

<span data-ttu-id="fcc5a-118">Die Konstante ist eine-Struktur.</span><span class="sxs-lookup"><span data-stu-id="fcc5a-118">Constant is a structure.</span></span>

</dd> <dt>

<span data-ttu-id="fcc5a-119"><span id="D3DXPC_FORCE_DWORD"></span><span id="d3dxpc_force_dword"></span>**D3DXPC \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fcc5a-119"><span id="D3DXPC_FORCE_DWORD"></span><span id="d3dxpc_force_dword"></span>**D3DXPC\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="fcc5a-120">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="fcc5a-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="fcc5a-121">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="fcc5a-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="fcc5a-122">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fcc5a-122">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fcc5a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fcc5a-123">Requirements</span></span>



| <span data-ttu-id="fcc5a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fcc5a-124">Requirement</span></span> | <span data-ttu-id="fcc5a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="fcc5a-125">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc5a-126">Header</span><span class="sxs-lookup"><span data-stu-id="fcc5a-126">Header</span></span><br/> | <dl> <span data-ttu-id="fcc5a-127"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcc5a-127"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcc5a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fcc5a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcc5a-129">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="fcc5a-129">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="fcc5a-130">**D3DXSHADER \_ TypInfo**</span><span class="sxs-lookup"><span data-stu-id="fcc5a-130">**D3DXSHADER\_TYPEINFO**</span></span>](d3dxshader-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="fcc5a-131">**D3DXCONSTANT- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="fcc5a-131">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 




