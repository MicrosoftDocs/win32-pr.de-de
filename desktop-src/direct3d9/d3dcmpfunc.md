---
description: Definiert die unterstützten Vergleichsfunktionen.
ms.assetid: 999af3eb-a208-4312-acee-373192ea69e4
title: D3DCMPFUNC-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCMPFUNC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e49f0e058e795e00349020619f1e6d6310dfd94f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870091"
---
# <a name="d3dcmpfunc-enumeration"></a><span data-ttu-id="ead7d-103">D3DCMPFUNC-Enumeration</span><span class="sxs-lookup"><span data-stu-id="ead7d-103">D3DCMPFUNC enumeration</span></span>

<span data-ttu-id="ead7d-104">Definiert die unterstützten Vergleichsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="ead7d-104">Defines the supported compare functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="ead7d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ead7d-105">Syntax</span></span>


```C++
typedef enum D3DCMPFUNC { 
  D3DCMP_NEVER         = 1,
  D3DCMP_LESS          = 2,
  D3DCMP_EQUAL         = 3,
  D3DCMP_LESSEQUAL     = 4,
  D3DCMP_GREATER       = 5,
  D3DCMP_NOTEQUAL      = 6,
  D3DCMP_GREATEREQUAL  = 7,
  D3DCMP_ALWAYS        = 8,
  D3DCMP_FORCE_DWORD   = 0x7fffffff
} D3DCMPFUNC, *LPD3DCMPFUNC;
```



## <a name="constants"></a><span data-ttu-id="ead7d-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="ead7d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ead7d-107"><span id="D3DCMP_NEVER"></span><span id="d3dcmp_never"></span>**D3DCMP \_ nie**</span><span class="sxs-lookup"><span data-stu-id="ead7d-107"><span id="D3DCMP_NEVER"></span><span id="d3dcmp_never"></span>**D3DCMP\_NEVER**</span></span>
</dt> <dd>

<span data-ttu-id="ead7d-108">Fehler beim Test immer.</span><span class="sxs-lookup"><span data-stu-id="ead7d-108">Always fail the test.</span></span>

</dd> <dt>

<span data-ttu-id="ead7d-109"><span id="D3DCMP_LESS"></span><span id="d3dcmp_less"></span>**D3DCMP \_ less**</span><span class="sxs-lookup"><span data-stu-id="ead7d-109"><span id="D3DCMP_LESS"></span><span id="d3dcmp_less"></span>**D3DCMP\_LESS**</span></span>
</dt> <dd>

<span data-ttu-id="ead7d-110">Akzeptieren Sie das neue Pixel, wenn der Wert kleiner ist als der Wert des aktuellen Pixels.</span><span class="sxs-lookup"><span data-stu-id="ead7d-110">Accept the new pixel if its value is less than the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="ead7d-111"><span id="D3DCMP_EQUAL"></span><span id="d3dcmp_equal"></span>**D3DCMP \_ gleich**</span><span class="sxs-lookup"><span data-stu-id="ead7d-111"><span id="D3DCMP_EQUAL"></span><span id="d3dcmp_equal"></span>**D3DCMP\_EQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="ead7d-112">Akzeptieren Sie das neue Pixel, wenn sein Wert dem Wert des aktuellen Pixels gleicht.</span><span class="sxs-lookup"><span data-stu-id="ead7d-112">Accept the new pixel if its value equals the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="ead7d-113"><span id="D3DCMP_LESSEQUAL"></span><span id="d3dcmp_lessequal"></span>**D3DCMP \_ lessequal**</span><span class="sxs-lookup"><span data-stu-id="ead7d-113"><span id="D3DCMP_LESSEQUAL"></span><span id="d3dcmp_lessequal"></span>**D3DCMP\_LESSEQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="ead7d-114">Akzeptieren Sie das neue Pixel, wenn der Wert kleiner oder gleich dem Wert des aktuellen Pixels ist.</span><span class="sxs-lookup"><span data-stu-id="ead7d-114">Accept the new pixel if its value is less than or equal to the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="ead7d-115"><span id="D3DCMP_GREATER"></span><span id="d3dcmp_greater"></span>**D3DCMP \_ größer**</span><span class="sxs-lookup"><span data-stu-id="ead7d-115"><span id="D3DCMP_GREATER"></span><span id="d3dcmp_greater"></span>**D3DCMP\_GREATER**</span></span>
</dt> <dd>

<span data-ttu-id="ead7d-116">Akzeptieren Sie das neue Pixel, wenn der Wert größer ist als der Wert des aktuellen Pixels.</span><span class="sxs-lookup"><span data-stu-id="ead7d-116">Accept the new pixel if its value is greater than the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="ead7d-117"><span id="D3DCMP_NOTEQUAL"></span><span id="d3dcmp_notequal"></span>**D3DCMP \_ NotEqual**</span><span class="sxs-lookup"><span data-stu-id="ead7d-117"><span id="D3DCMP_NOTEQUAL"></span><span id="d3dcmp_notequal"></span>**D3DCMP\_NOTEQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="ead7d-118">Akzeptieren Sie das neue Pixel, wenn der Wert nicht dem Wert des aktuellen Pixels entspricht.</span><span class="sxs-lookup"><span data-stu-id="ead7d-118">Accept the new pixel if its value does not equal the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="ead7d-119"><span id="D3DCMP_GREATEREQUAL"></span><span id="d3dcmp_greaterequal"></span>**D3DCMP \_ greaterequal**</span><span class="sxs-lookup"><span data-stu-id="ead7d-119"><span id="D3DCMP_GREATEREQUAL"></span><span id="d3dcmp_greaterequal"></span>**D3DCMP\_GREATEREQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="ead7d-120">Akzeptieren Sie das neue Pixel, wenn der Wert größer oder gleich dem Wert des aktuellen Pixels ist.</span><span class="sxs-lookup"><span data-stu-id="ead7d-120">Accept the new pixel if its value is greater than or equal to the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="ead7d-121"><span id="D3DCMP_ALWAYS"></span><span id="d3dcmp_always"></span>**D3DCMP \_ immer**</span><span class="sxs-lookup"><span data-stu-id="ead7d-121"><span id="D3DCMP_ALWAYS"></span><span id="d3dcmp_always"></span>**D3DCMP\_ALWAYS**</span></span>
</dt> <dd>

<span data-ttu-id="ead7d-122">Bestanden Sie den Test immer.</span><span class="sxs-lookup"><span data-stu-id="ead7d-122">Always pass the test.</span></span>

</dd> <dt>

<span data-ttu-id="ead7d-123"><span id="D3DCMP_FORCE_DWORD"></span><span id="d3dcmp_force_dword"></span>**D3DCMP \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ead7d-123"><span id="D3DCMP_FORCE_DWORD"></span><span id="d3dcmp_force_dword"></span>**D3DCMP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="ead7d-124">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="ead7d-124">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="ead7d-125">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="ead7d-125">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="ead7d-126">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ead7d-126">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ead7d-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ead7d-127">Remarks</span></span>

<span data-ttu-id="ead7d-128">Die Werte in diesem enumerierten Typ definieren die unterstützten Vergleichsfunktionen für die \_ Rendering-Zustände D3DRS zfunc, D3DRS \_ alphafunc und D3DRS \_ stencilfunc.</span><span class="sxs-lookup"><span data-stu-id="ead7d-128">The values in this enumerated type define the supported compare functions for the D3DRS\_ZFUNC, D3DRS\_ALPHAFUNC, and D3DRS\_STENCILFUNC render states.</span></span>

## <a name="requirements"></a><span data-ttu-id="ead7d-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ead7d-129">Requirements</span></span>



| <span data-ttu-id="ead7d-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ead7d-130">Requirement</span></span> | <span data-ttu-id="ead7d-131">Wert</span><span class="sxs-lookup"><span data-stu-id="ead7d-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ead7d-132">Header</span><span class="sxs-lookup"><span data-stu-id="ead7d-132">Header</span></span><br/> | <dl> <span data-ttu-id="ead7d-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ead7d-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ead7d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ead7d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ead7d-135">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="ead7d-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="ead7d-136">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="ead7d-136">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
