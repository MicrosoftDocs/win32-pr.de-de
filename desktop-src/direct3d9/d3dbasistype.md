---
description: Definiert den Basis-Typ einer hochwertigen patchoberfläche.
ms.assetid: 18c31c77-7ba3-449c-af4a-717b8c1dced1
title: D3DBASISTYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBASISTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7e166f56aa2625c868d3e2e2223efbb577e05bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132305"
---
# <a name="d3dbasistype-enumeration"></a><span data-ttu-id="8a662-103">D3DBASISTYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="8a662-103">D3DBASISTYPE enumeration</span></span>

<span data-ttu-id="8a662-104">Definiert den Basis-Typ einer hochwertigen patchoberfläche.</span><span class="sxs-lookup"><span data-stu-id="8a662-104">Defines the basis type of a high-order patch surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a662-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a662-105">Syntax</span></span>


```C++
typedef enum D3DBASISTYPE { 
  D3DBASIS_BEZIER       = 0,
  D3DBASIS_BSPLINE      = 1,
  D3DBASIS_CATMULL_ROM  = 2,
  D3DBASIS_FORCE_DWORD  = 0x7fffffff
} D3DBASISTYPE, *LPD3DBASISTYPE;
```



## <a name="constants"></a><span data-ttu-id="8a662-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="8a662-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8a662-107"><span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**D3DBASIS \_ Bezier**</span><span class="sxs-lookup"><span data-stu-id="8a662-107"><span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**D3DBASIS\_BEZIER**</span></span>
</dt> <dd>

<span data-ttu-id="8a662-108">Eingabe Vertices werden als eine Reihe von Bézier-Patches behandelt.</span><span class="sxs-lookup"><span data-stu-id="8a662-108">Input vertices are treated as a series of Bézier patches.</span></span> <span data-ttu-id="8a662-109">Die Anzahl der angegebenen Scheitel Punkte muss von 4 unterschieden werden.</span><span class="sxs-lookup"><span data-stu-id="8a662-109">The number of vertices specified must be divisible by 4.</span></span> <span data-ttu-id="8a662-110">Teile des Netzes, die über dieses Kriterium hinausgehen, werden nicht gerendert.</span><span class="sxs-lookup"><span data-stu-id="8a662-110">Portions of the mesh beyond this criterion will not be rendered.</span></span> <span data-ttu-id="8a662-111">Die vollständige Kontinuität wird zwischen den Subpatches im Inneren der Oberfläche, die von den einzelnen anrufen gerendert wird, angenommen.</span><span class="sxs-lookup"><span data-stu-id="8a662-111">Full continuity is assumed between sub-patches in the interior of the surface rendered by each call.</span></span> <span data-ttu-id="8a662-112">Es ist garantiert, dass nur die Scheitel Punkte an den Ecken der einzelnen Subpatches auf der sich ergebenden Oberfläche liegen.</span><span class="sxs-lookup"><span data-stu-id="8a662-112">Only the vertices at the corners of each sub-patch are guaranteed to lie on the resulting surface.</span></span>

</dd> <dt>

<span data-ttu-id="8a662-113"><span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**D3DBASIS \_ Bspline**</span><span class="sxs-lookup"><span data-stu-id="8a662-113"><span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**D3DBASIS\_BSPLINE**</span></span>
</dt> <dd>

<span data-ttu-id="8a662-114">Eingabe Vertices werden als Steuerungs Punkte einer B-Spline-Oberfläche behandelt.</span><span class="sxs-lookup"><span data-stu-id="8a662-114">Input vertices are treated as control points of a B-spline surface.</span></span> <span data-ttu-id="8a662-115">Die Anzahl der gerenderten Blenden ist zwei weniger als die Anzahl der Öffnungen in dieser Richtung.</span><span class="sxs-lookup"><span data-stu-id="8a662-115">The number of apertures rendered is two fewer than the number of apertures in that direction.</span></span> <span data-ttu-id="8a662-116">Im Allgemeinen enthält die generierte Oberfläche nicht die angegebenen Steuerelement Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="8a662-116">In general, the generated surface does not contain the control vertices specified.</span></span>

</dd> <dt>

<span data-ttu-id="8a662-117"><span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS- \_ Update- \_ Rom**</span><span class="sxs-lookup"><span data-stu-id="8a662-117"><span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS\_CATMULL\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="8a662-118">Eine interinterpolation definiert die Oberfläche, damit die Oberfläche alle angegebenen Eingabe Scheitel Punkte durchläuft.</span><span class="sxs-lookup"><span data-stu-id="8a662-118">An interpolating basis defines the surface so that the surface goes through all the input vertices specified.</span></span> <span data-ttu-id="8a662-119">In DirectX 8 war dies D3DBASIS \_ Interpolate.</span><span class="sxs-lookup"><span data-stu-id="8a662-119">In DirectX 8, this was D3DBASIS\_INTERPOLATE.</span></span>

</dd> <dt>

<span data-ttu-id="8a662-120"><span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8a662-120"><span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="8a662-121">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="8a662-121">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="8a662-122">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="8a662-122">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="8a662-123">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8a662-123">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a662-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a662-124">Remarks</span></span>

<span data-ttu-id="8a662-125">Die Member von **D3DBASISTYPE** geben die zu verwendende Formulierung an, die bei der Auswertung der hochwertigen patchoberflächen primitive während des Mosaik Prozesses verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a662-125">The members of **D3DBASISTYPE** specify the formulation to be used in evaluating the high-order patch surface primitive during tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a662-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a662-126">Requirements</span></span>



| <span data-ttu-id="8a662-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a662-127">Requirement</span></span> | <span data-ttu-id="8a662-128">Wert</span><span class="sxs-lookup"><span data-stu-id="8a662-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a662-129">Header</span><span class="sxs-lookup"><span data-stu-id="8a662-129">Header</span></span><br/> | <dl> <span data-ttu-id="8a662-130"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a662-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a662-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a662-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a662-132">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="8a662-132">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="8a662-133">**D3DRECTPATCH \_ Info**</span><span class="sxs-lookup"><span data-stu-id="8a662-133">**D3DRECTPATCH\_INFO**</span></span>](d3drectpatch-info.md)
</dt> <dt>

[<span data-ttu-id="8a662-134">**D3DTRIPATCH \_ Info**</span><span class="sxs-lookup"><span data-stu-id="8a662-134">**D3DTRIPATCH\_INFO**</span></span>](d3dtripatch-info.md)
</dt> </dl>

 

 




