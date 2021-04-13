---
description: Definiert Konstanten, die den Nebel Modus beschreiben.
ms.assetid: cd83c914-bc1d-4f66-b5a6-7984b7ec52cd
title: D3DFOGMODE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFOGMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8436a52edbb9460c6945c1526513629939ec444b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355237"
---
# <a name="d3dfogmode-enumeration"></a><span data-ttu-id="b1cff-103">D3DFOGMODE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="b1cff-103">D3DFOGMODE enumeration</span></span>

<span data-ttu-id="b1cff-104">Definiert Konstanten, die den Nebel Modus beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b1cff-104">Defines constants that describe the fog mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1cff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1cff-105">Syntax</span></span>


```C++
typedef enum D3DFOGMODE { 
  D3DFOG_NONE         = 0,
  D3DFOG_EXP          = 1,
  D3DFOG_EXP2         = 2,
  D3DFOG_LINEAR       = 3,
  D3DFOG_FORCE_DWORD  = 0x7fffffff
} D3DFOGMODE, *LPD3DFOGMODE;
```



## <a name="constants"></a><span data-ttu-id="b1cff-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="b1cff-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b1cff-107"><span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG \_ None**</span><span class="sxs-lookup"><span data-stu-id="b1cff-107"><span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="b1cff-108">Kein Nebeleffekt.</span><span class="sxs-lookup"><span data-stu-id="b1cff-108">No fog effect.</span></span>

</dd> <dt>

<span data-ttu-id="b1cff-109"><span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG- \_ Exp**</span><span class="sxs-lookup"><span data-stu-id="b1cff-109"><span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG\_EXP**</span></span>
</dt> <dd>

<span data-ttu-id="b1cff-110">Der Nebeleffekt wird entsprechend der folgenden Formel exponentiell verstärkt.</span><span class="sxs-lookup"><span data-stu-id="b1cff-110">Fog effect intensifies exponentially, according to the following formula.</span></span>

![Formel der Nebeleffekt Intensität](images/fogexp.png)

</dd> <dt>

<span data-ttu-id="b1cff-112"><span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG \_ exp2**</span><span class="sxs-lookup"><span data-stu-id="b1cff-112"><span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG\_EXP2**</span></span>
</dt> <dd>

<span data-ttu-id="b1cff-113">Der Nebeleffekt wird exponentiell mit dem Quadrat der Entfernung entsprechend der folgenden Formel verstärkt.</span><span class="sxs-lookup"><span data-stu-id="b1cff-113">Fog effect intensifies exponentially with the square of the distance, according to the following formula.</span></span>

![Formel der Nebel Wirkungs Intensität basierend auf dem Quadrat der Entfernung](images/fogexp2.png)

</dd> <dt>

<span data-ttu-id="b1cff-115"><span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**D3DFOG \_ linear**</span><span class="sxs-lookup"><span data-stu-id="b1cff-115"><span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**D3DFOG\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="b1cff-116">Der Nebeleffekt wird linear zwischen dem Start-und dem Endpunkt entsprechend der folgenden Formel verstärkt.</span><span class="sxs-lookup"><span data-stu-id="b1cff-116">Fog effect intensifies linearly between the start and end points, according to the following formula.</span></span>

![Formel der Nebel Wirkungs Intensität basierend auf Start-und Endpunkten](images/fogliner.png)

<span data-ttu-id="b1cff-118">Dies ist der einzige derzeit unterstützte Nebelmodus.</span><span class="sxs-lookup"><span data-stu-id="b1cff-118">This is the only fog mode currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="b1cff-119"><span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1cff-119"><span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="b1cff-120">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="b1cff-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="b1cff-121">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="b1cff-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="b1cff-122">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1cff-122">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1cff-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1cff-123">Remarks</span></span>

<span data-ttu-id="b1cff-124">Die Werte in diesem enumerierten Typ werden von den \_ renderzuständen D3DRS fogtablemode und D3DRS \_ fogvertexmode verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1cff-124">The values in this enumerated type are used by the D3DRS\_FOGTABLEMODE and D3DRS\_FOGVERTEXMODE render states.</span></span>

<span data-ttu-id="b1cff-125">Nebel kann als Maß der Sichtbarkeit betrachtet werden: je niedriger der von einer Nebel Gleichung erzeugte Nebelwert ist, desto weniger sichtbar ist ein Objekt.</span><span class="sxs-lookup"><span data-stu-id="b1cff-125">Fog can be considered a measure of visibility: the lower the fog value produced by a fog equation, the less visible an object is.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1cff-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1cff-126">Requirements</span></span>



| <span data-ttu-id="b1cff-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1cff-127">Requirement</span></span> | <span data-ttu-id="b1cff-128">Wert</span><span class="sxs-lookup"><span data-stu-id="b1cff-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1cff-129">Header</span><span class="sxs-lookup"><span data-stu-id="b1cff-129">Header</span></span><br/> | <dl> <span data-ttu-id="b1cff-130"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1cff-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1cff-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1cff-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1cff-132">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="b1cff-132">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="b1cff-133">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="b1cff-133">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
