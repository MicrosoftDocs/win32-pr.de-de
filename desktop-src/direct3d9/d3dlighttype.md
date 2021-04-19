---
description: Definiert den hellen Typ.
ms.assetid: 90ad82d3-ffa8-42bb-9d9c-cf28a416c32d
title: D3DLIGHTTYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHTTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 83c94db3126443f757f01a69d7d773417f70683a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357246"
---
# <a name="d3dlighttype-enumeration"></a><span data-ttu-id="9e649-103">D3DLIGHTTYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="9e649-103">D3DLIGHTTYPE enumeration</span></span>

<span data-ttu-id="9e649-104">Definiert den hellen Typ.</span><span class="sxs-lookup"><span data-stu-id="9e649-104">Defines the light type.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e649-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e649-105">Syntax</span></span>


```C++
typedef enum D3DLIGHTTYPE { 
  D3DLIGHT_POINT        = 1,
  D3DLIGHT_SPOT         = 2,
  D3DLIGHT_DIRECTIONAL  = 3,
  D3DLIGHT_FORCE_DWORD  = 0x7fffffff
} D3DLIGHTTYPE, *LPD3DLIGHTTYPE;
```



## <a name="constants"></a><span data-ttu-id="9e649-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="9e649-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9e649-107"><span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**D3DLIGHT \_ Punkt**</span><span class="sxs-lookup"><span data-stu-id="9e649-107"><span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**D3DLIGHT\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="9e649-108">Light ist eine Punktquelle.</span><span class="sxs-lookup"><span data-stu-id="9e649-108">Light is a point source.</span></span> <span data-ttu-id="9e649-109">Das Licht hat eine Position im Raum und strahlt das Licht in alle Richtungen aus.</span><span class="sxs-lookup"><span data-stu-id="9e649-109">The light has a position in space and radiates light in all directions.</span></span>

</dd> <dt>

<span data-ttu-id="9e649-110"><span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**D3DLIGHT \_ Spot**</span><span class="sxs-lookup"><span data-stu-id="9e649-110"><span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**D3DLIGHT\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="9e649-111">Light ist eine Spotlight-Quelle.</span><span class="sxs-lookup"><span data-stu-id="9e649-111">Light is a spotlight source.</span></span> <span data-ttu-id="9e649-112">Dieses Licht ist wie ein Punktlicht, mit dem Unterschied, dass die Beleuchtung auf einen Kegel beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="9e649-112">This light is like a point light, except that the illumination is limited to a cone.</span></span> <span data-ttu-id="9e649-113">Dieser Light-Typ hat eine Richtung und einige andere Parameter, die die Form des von ihm erzeugten Diagrammes bestimmen.</span><span class="sxs-lookup"><span data-stu-id="9e649-113">This light type has a direction and several other parameters that determine the shape of the cone it produces.</span></span> <span data-ttu-id="9e649-114">Weitere Informationen zu diesen Parametern finden Sie in der [**D3DLIGHT9**](d3dlight9.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9e649-114">For information about these parameters, see the [**D3DLIGHT9**](d3dlight9.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9e649-115"><span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**D3DLIGHT \_ direktional**</span><span class="sxs-lookup"><span data-stu-id="9e649-115"><span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**D3DLIGHT\_DIRECTIONAL**</span></span>
</dt> <dd>

<span data-ttu-id="9e649-116">Light ist eine direktionale Lichtquelle.</span><span class="sxs-lookup"><span data-stu-id="9e649-116">Light is a directional light source.</span></span> <span data-ttu-id="9e649-117">Dies entspricht der Verwendung einer Point Light-Quelle in unbegrenzter Entfernung.</span><span class="sxs-lookup"><span data-stu-id="9e649-117">This is equivalent to using a point light source at an infinite distance.</span></span>

</dd> <dt>

<span data-ttu-id="9e649-118"><span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="9e649-118"><span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="9e649-119">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="9e649-119">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="9e649-120">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="9e649-120">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="9e649-121">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e649-121">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e649-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e649-122">Remarks</span></span>

<span data-ttu-id="9e649-123">Direktionale Lichter sind etwas schneller als Punktlicht Quellen, aber die Punkt Lichter sehen etwas besser aus.</span><span class="sxs-lookup"><span data-stu-id="9e649-123">Directional lights are slightly faster than point light sources, but point lights look a little better.</span></span> <span data-ttu-id="9e649-124">Die Scheinwerfer bieten interessante visuelle Effekte, sind aber Rechenzeit aufwändig.</span><span class="sxs-lookup"><span data-stu-id="9e649-124">Spotlights offer interesting visual effects but are computationally time-consuming.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e649-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e649-125">Requirements</span></span>



| <span data-ttu-id="9e649-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e649-126">Requirement</span></span> | <span data-ttu-id="9e649-127">Wert</span><span class="sxs-lookup"><span data-stu-id="9e649-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e649-128">Header</span><span class="sxs-lookup"><span data-stu-id="9e649-128">Header</span></span><br/> | <dl> <span data-ttu-id="9e649-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e649-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e649-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e649-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e649-131">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="9e649-131">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="9e649-132">**D3DLIGHT9**</span><span class="sxs-lookup"><span data-stu-id="9e649-132">**D3DLIGHT9**</span></span>](d3dlight9.md)
</dt> </dl>

 

 




