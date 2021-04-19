---
description: Definiert den Grad der Variablen in der Gleichung, die eine Kurve beschreibt.
ms.assetid: 52a9c57e-a48d-4d8a-a208-97a3d09e7abf
title: D3DDEGREETYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEGREETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 773ef3a8dd8fc5f4657119c2021c5723e54a3bd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364354"
---
# <a name="d3ddegreetype-enumeration"></a><span data-ttu-id="69125-103">D3DDEGREETYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="69125-103">D3DDEGREETYPE enumeration</span></span>

<span data-ttu-id="69125-104">Definiert den Grad der Variablen in der Gleichung, die eine Kurve beschreibt.</span><span class="sxs-lookup"><span data-stu-id="69125-104">Defines the degree of the variables in the equation that describes a curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="69125-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="69125-105">Syntax</span></span>


```C++
typedef enum D3DDEGREETYPE { 
  D3DDEGREE_LINEAR     = 1,
  D3DDEGREE_QUADRATIC  = 2,
  D3DDEGREE_CUBIC      = 3,
  D3DDEGREE_QUINTIC    = 5,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DDEGREETYPE, *LPD3DDEGREETYPE;
```



## <a name="constants"></a><span data-ttu-id="69125-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="69125-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="69125-107"><span id="D3DDEGREE_LINEAR"></span><span id="d3ddegree_linear"></span>**D3DDEGREE \_ linear**</span><span class="sxs-lookup"><span data-stu-id="69125-107"><span id="D3DDEGREE_LINEAR"></span><span id="d3ddegree_linear"></span>**D3DDEGREE\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="69125-108">Die Kurve wird durch Variablen der ersten Reihenfolge beschrieben.</span><span class="sxs-lookup"><span data-stu-id="69125-108">Curve is described by variables of first order.</span></span>

</dd> <dt>

<span data-ttu-id="69125-109"><span id="D3DDEGREE_QUADRATIC"></span><span id="d3ddegree_quadratic"></span>**D3DDEGREE \_ quadratisch**</span><span class="sxs-lookup"><span data-stu-id="69125-109"><span id="D3DDEGREE_QUADRATIC"></span><span id="d3ddegree_quadratic"></span>**D3DDEGREE\_QUADRATIC**</span></span>
</dt> <dd>

<span data-ttu-id="69125-110">Die Kurve wird durch Variablen der zweiten Reihenfolge beschrieben.</span><span class="sxs-lookup"><span data-stu-id="69125-110">Curve is described by variables of second order.</span></span>

</dd> <dt>

<span data-ttu-id="69125-111"><span id="D3DDEGREE_CUBIC"></span><span id="d3ddegree_cubic"></span>**D3DDEGREE \_ kubisch**</span><span class="sxs-lookup"><span data-stu-id="69125-111"><span id="D3DDEGREE_CUBIC"></span><span id="d3ddegree_cubic"></span>**D3DDEGREE\_CUBIC**</span></span>
</dt> <dd>

<span data-ttu-id="69125-112">Die Kurve wird durch die Variablen der dritten Reihenfolge beschrieben.</span><span class="sxs-lookup"><span data-stu-id="69125-112">Curve is described by variables of third order.</span></span>

</dd> <dt>

<span data-ttu-id="69125-113"><span id="D3DDEGREE_QUINTIC"></span><span id="d3ddegree_quintic"></span>**D3DDEGREE \_ Quintic**</span><span class="sxs-lookup"><span data-stu-id="69125-113"><span id="D3DDEGREE_QUINTIC"></span><span id="d3ddegree_quintic"></span>**D3DDEGREE\_QUINTIC**</span></span>
</dt> <dd>

<span data-ttu-id="69125-114">Die Kurve wird durch Variablen der vierten Reihenfolge beschrieben.</span><span class="sxs-lookup"><span data-stu-id="69125-114">Curve is described by variables of fourth order.</span></span>

</dd> <dt>

<span data-ttu-id="69125-115"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="69125-115"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="69125-116">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="69125-116">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="69125-117">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="69125-117">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="69125-118">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="69125-118">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69125-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69125-119">Remarks</span></span>

<span data-ttu-id="69125-120">Die Werte in dieser Enumeration werden verwendet, um die Kurven zu beschreiben, die von Rechteck-und Dreiecks Patches verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="69125-120">The values in this enumeration are used to describe the curves used by rectangle and triangle patches.</span></span> <span data-ttu-id="69125-121">Weitere Informationen finden Sie unter D3DRS \_ CullMode.</span><span class="sxs-lookup"><span data-stu-id="69125-121">For more information, see D3DRS\_CULLMODE.</span></span>

## <a name="requirements"></a><span data-ttu-id="69125-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69125-122">Requirements</span></span>



| <span data-ttu-id="69125-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69125-123">Requirement</span></span> | <span data-ttu-id="69125-124">Wert</span><span class="sxs-lookup"><span data-stu-id="69125-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69125-125">Header</span><span class="sxs-lookup"><span data-stu-id="69125-125">Header</span></span><br/> | <dl> <span data-ttu-id="69125-126"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="69125-126"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69125-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69125-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69125-128">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="69125-128">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="69125-129">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="69125-129">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="69125-130">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="69125-130">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
