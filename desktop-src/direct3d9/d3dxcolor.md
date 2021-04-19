---
description: Beschreibt Farbwerte.
ms.assetid: 53d3176a-f727-498e-8bea-0e30e0a1c66e
title: D3DXCOLOR-Struktur (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: c7e5c1ac12341ccf6272714511959ee9a131ba4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350693"
---
# <a name="d3dxcolor-structure-d3dx9mathh"></a><span data-ttu-id="b4072-103">D3DXCOLOR-Struktur (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="b4072-103">D3DXCOLOR structure (D3dx9math.h)</span></span>

<span data-ttu-id="b4072-104">Beschreibt Farbwerte.</span><span class="sxs-lookup"><span data-stu-id="b4072-104">Describes color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4072-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4072-105">Syntax</span></span>


```C++
typedef struct D3DXCOLOR {
  FLOAT r;
  FLOAT g;
  FLOAT b;
  FLOAT a;
} D3DXCOLOR, *LPD3DXCOLOR;
```



## <a name="members"></a><span data-ttu-id="b4072-106">Member</span><span class="sxs-lookup"><span data-stu-id="b4072-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b4072-107">**r**</span><span class="sxs-lookup"><span data-stu-id="b4072-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="b4072-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4072-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4072-109">Rote Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="b4072-109">Red component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="b4072-110">**g**</span><span class="sxs-lookup"><span data-stu-id="b4072-110">**g**</span></span>
</dt> <dd>

<span data-ttu-id="b4072-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4072-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4072-112">Grüne Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="b4072-112">Green component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="b4072-113">**b**</span><span class="sxs-lookup"><span data-stu-id="b4072-113">**b**</span></span>
</dt> <dd>

<span data-ttu-id="b4072-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4072-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4072-115">Blaue Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="b4072-115">Blue component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="b4072-116">**ein**</span><span class="sxs-lookup"><span data-stu-id="b4072-116">**a**</span></span>
</dt> <dd>

<span data-ttu-id="b4072-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4072-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4072-118">Alpha Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="b4072-118">Alpha component of the color.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4072-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4072-119">Remarks</span></span>

<span data-ttu-id="b4072-120">C++-Programmierer können das Überladen von Operatoren und die Typumwandlung mit den [**D3DXCOLOR-Erweiterungen**](d3dxcolor-extensions.md)nutzen, die überladene Konstruktoren implementieren, sowie Zuweisungs-, unäre und binäre (einschließlich Gleichheits-) Operatoren.</span><span class="sxs-lookup"><span data-stu-id="b4072-120">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXCOLOR Extensions**](d3dxcolor-extensions.md), which implement overloaded constructors, as well as assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4072-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4072-121">Requirements</span></span>



| <span data-ttu-id="b4072-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4072-122">Requirement</span></span> | <span data-ttu-id="b4072-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b4072-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4072-124">Header</span><span class="sxs-lookup"><span data-stu-id="b4072-124">Header</span></span><br/> | <dl> <span data-ttu-id="b4072-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4072-125"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4072-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4072-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4072-127">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="b4072-127">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
