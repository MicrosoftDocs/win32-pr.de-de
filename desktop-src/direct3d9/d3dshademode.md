---
description: Definiert Konstanten, die die unterstützten Schattierungs Modi beschreiben.
ms.assetid: ba4e0c62-b496-427b-a324-2fb560d153ba
title: D3DSHADEMODE-Enumeration (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSHADEMODE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9950e0074bef7a7b0c211177b3902cd69e2e112c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354537"
---
# <a name="d3dshademode-enumeration"></a><span data-ttu-id="aff68-103">D3DSHADEMODE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="aff68-103">D3DSHADEMODE enumeration</span></span>

<span data-ttu-id="aff68-104">Definiert Konstanten, die die unterstützten Schattierungs Modi beschreiben.</span><span class="sxs-lookup"><span data-stu-id="aff68-104">Defines constants that describe the supported shading modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="aff68-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aff68-105">Syntax</span></span>


```C++
typedef enum D3DSHADEMODE { 
  D3DSHADE_FLAT         = 1,
  D3DSHADE_GOURAUD      = 2,
  D3DSHADE_PHONG        = 3,
  D3DSHADE_FORCE_DWORD  = 0x7fffffff
} D3DSHADEMODE, *LPD3DSHADEMODE;
```



## <a name="constants"></a><span data-ttu-id="aff68-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="aff68-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="aff68-107"><span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE \_ Flat**</span><span class="sxs-lookup"><span data-stu-id="aff68-107"><span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE\_FLAT**</span></span>
</dt> <dd>

<span data-ttu-id="aff68-108">Flacher Schattierungs Modus.</span><span class="sxs-lookup"><span data-stu-id="aff68-108">Flat shading mode.</span></span> <span data-ttu-id="aff68-109">Die Farbe und die Glanz Komponente des ersten Scheitel Punkts im Dreieck werden verwendet, um die Farbe und die Glanz Komponente der Vorderseite zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="aff68-109">The color and specular component of the first vertex in the triangle are used to determine the color and specular component of the face.</span></span> <span data-ttu-id="aff68-110">Diese Farben bleiben über das Dreieck konstant. Das heißt, Sie werden nicht interpoliert.</span><span class="sxs-lookup"><span data-stu-id="aff68-110">These colors remain constant across the triangle; that is, they are not interpolated.</span></span> <span data-ttu-id="aff68-111">Das Glanz Alpha ist interpoliert.</span><span class="sxs-lookup"><span data-stu-id="aff68-111">The specular alpha is interpolated.</span></span> <span data-ttu-id="aff68-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="aff68-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="aff68-113"><span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE- \_ Gouraud**</span><span class="sxs-lookup"><span data-stu-id="aff68-113"><span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE\_GOURAUD**</span></span>
</dt> <dd>

<span data-ttu-id="aff68-114">Der Gouraud-Schattierungs Modus.</span><span class="sxs-lookup"><span data-stu-id="aff68-114">Gouraud shading mode.</span></span> <span data-ttu-id="aff68-115">Die Farbe und die Glanz Komponenten der Vorderseite werden durch eine lineare interpolung zwischen allen drei Scheitel Punkten des Dreiecks bestimmt.</span><span class="sxs-lookup"><span data-stu-id="aff68-115">The color and specular components of the face are determined by a linear interpolation between all three of the triangle's vertices.</span></span>

</dd> <dt>

<span data-ttu-id="aff68-116"><span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE \_ Phong**</span><span class="sxs-lookup"><span data-stu-id="aff68-116"><span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE\_PHONG**</span></span>
</dt> <dd>

<span data-ttu-id="aff68-117">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aff68-117">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="aff68-118"><span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="aff68-118"><span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="aff68-119">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="aff68-119">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="aff68-120">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="aff68-120">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="aff68-121">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="aff68-121">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aff68-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aff68-122">Remarks</span></span>

<span data-ttu-id="aff68-123">Der erste Scheitelpunkt eines Dreiecks für den flachen Schattierungs Modus wird wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="aff68-123">The first vertex of a triangle for flat shading mode is defined in the following manner.</span></span>

-   <span data-ttu-id="aff68-124">Für eine Dreiecks Liste ist der erste Scheitelpunkt des Dreiecks i \* 3.</span><span class="sxs-lookup"><span data-stu-id="aff68-124">For a triangle list, the first vertex of the triangle i is i \* 3.</span></span>
-   <span data-ttu-id="aff68-125">Bei einem Dreiecks Streifen ist der erste Scheitelpunkt des Dreiecks "Scheitelpunkt i".</span><span class="sxs-lookup"><span data-stu-id="aff68-125">For a triangle strip, the first vertex of the triangle i is vertex i.</span></span>
-   <span data-ttu-id="aff68-126">Bei einem Dreiecks Lüfter ist der erste Scheitelpunkt des Dreiecks "Scheitelpunkt i + 1".</span><span class="sxs-lookup"><span data-stu-id="aff68-126">For a triangle fan, the first vertex of the triangle i is vertex i + 1.</span></span>

<span data-ttu-id="aff68-127">Die Member dieses Enumerationstyps definieren die Werte für den D3DRS \_ SHADEMODE-Rendering-Zustand.</span><span class="sxs-lookup"><span data-stu-id="aff68-127">The members of this enumerated type define the vales for the D3DRS\_SHADEMODE render state.</span></span>

## <a name="requirements"></a><span data-ttu-id="aff68-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aff68-128">Requirements</span></span>



| <span data-ttu-id="aff68-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aff68-129">Requirement</span></span> | <span data-ttu-id="aff68-130">Wert</span><span class="sxs-lookup"><span data-stu-id="aff68-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aff68-131">Header</span><span class="sxs-lookup"><span data-stu-id="aff68-131">Header</span></span><br/> | <dl> <span data-ttu-id="aff68-132"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="aff68-132"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aff68-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aff68-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aff68-134">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="aff68-134">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="aff68-135">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="aff68-135">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
