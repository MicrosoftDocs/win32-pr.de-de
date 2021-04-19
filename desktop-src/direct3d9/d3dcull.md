---
description: Definiert die unterstützten culck-Modi.
ms.assetid: b669307c-0d40-4ecb-8a2e-8bd1d9c65647
title: D3DCULL-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCULL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e88aa1baf86b2b03177cc686bf83299311065283
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361851"
---
# <a name="d3dcull-enumeration"></a><span data-ttu-id="a128e-103">D3DCULL-Enumeration</span><span class="sxs-lookup"><span data-stu-id="a128e-103">D3DCULL enumeration</span></span>

<span data-ttu-id="a128e-104">Definiert die unterstützten culck-Modi.</span><span class="sxs-lookup"><span data-stu-id="a128e-104">Defines the supported culling modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a128e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a128e-105">Syntax</span></span>


```C++
typedef enum D3DCULL { 
  D3DCULL_NONE         = 1,
  D3DCULL_CW           = 2,
  D3DCULL_CCW          = 3,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DCULL, *LPD3DCULL;
```



## <a name="constants"></a><span data-ttu-id="a128e-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="a128e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a128e-107"><span id="D3DCULL_NONE"></span><span id="d3dcull_none"></span>**D3DCULL \_ None**</span><span class="sxs-lookup"><span data-stu-id="a128e-107"><span id="D3DCULL_NONE"></span><span id="d3dcull_none"></span>**D3DCULL\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="a128e-108">Keine Gesichter zurück.</span><span class="sxs-lookup"><span data-stu-id="a128e-108">Do not cull back faces.</span></span>

</dd> <dt>

<span data-ttu-id="a128e-109"><span id="D3DCULL_CW"></span><span id="d3dcull_cw"></span>**D3DCULL \_ CW**</span><span class="sxs-lookup"><span data-stu-id="a128e-109"><span id="D3DCULL_CW"></span><span id="d3dcull_cw"></span>**D3DCULL\_CW**</span></span>
</dt> <dd>

<span data-ttu-id="a128e-110">Die Flächen werden mit den Scheitel Punkten im Uhrzeigersinn zurückgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a128e-110">Cull back faces with clockwise vertices.</span></span>

</dd> <dt>

<span data-ttu-id="a128e-111"><span id="D3DCULL_CCW"></span><span id="d3dcull_ccw"></span>**D3DCULL \_ CCW**</span><span class="sxs-lookup"><span data-stu-id="a128e-111"><span id="D3DCULL_CCW"></span><span id="d3dcull_ccw"></span>**D3DCULL\_CCW**</span></span>
</dt> <dd>

<span data-ttu-id="a128e-112">Kell-Gesichter mit gegen Uhrzeigersinn.</span><span class="sxs-lookup"><span data-stu-id="a128e-112">Cull back faces with counterclockwise vertices.</span></span>

</dd> <dt>

<span data-ttu-id="a128e-113"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a128e-113"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a128e-114">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="a128e-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="a128e-115">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="a128e-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="a128e-116">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a128e-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a128e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a128e-117">Remarks</span></span>

<span data-ttu-id="a128e-118">Die Werte in diesem enumerierten Typ werden vom D3DRS \_ CullMode-renderzustand verwendet.</span><span class="sxs-lookup"><span data-stu-id="a128e-118">The values in this enumerated type are used by the D3DRS\_CULLMODE render state.</span></span> <span data-ttu-id="a128e-119">Die culk-Modi legen fest, wie die Gesichter beim Rendern einer Geometrie gekullt werden.</span><span class="sxs-lookup"><span data-stu-id="a128e-119">The culling modes define how back faces are culled when rendering a geometry.</span></span>

## <a name="requirements"></a><span data-ttu-id="a128e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a128e-120">Requirements</span></span>



| <span data-ttu-id="a128e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a128e-121">Requirement</span></span> | <span data-ttu-id="a128e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a128e-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a128e-123">Header</span><span class="sxs-lookup"><span data-stu-id="a128e-123">Header</span></span><br/> | <dl> <span data-ttu-id="a128e-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a128e-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a128e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a128e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a128e-126">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="a128e-126">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="a128e-127">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="a128e-127">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="a128e-128">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="a128e-128">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
