---
description: Definiert die unterstützten Blend-Vorgänge. Siehe Hinweise zu Definitionen von Begriffen.
ms.assetid: ae750d84-ed7d-4a76-bf64-eae8828c66c7
title: D3DBLENDOP-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLENDOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3ad23d3fb2a93734047f55a46c14335069c95ea9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353346"
---
# <a name="d3dblendop-enumeration"></a><span data-ttu-id="f69f1-104">D3DBLENDOP-Enumeration</span><span class="sxs-lookup"><span data-stu-id="f69f1-104">D3DBLENDOP enumeration</span></span>

<span data-ttu-id="f69f1-105">Definiert die unterstützten Blend-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="f69f1-105">Defines the supported blend operations.</span></span> <span data-ttu-id="f69f1-106">Siehe Hinweise zu Definitionen von Begriffen.</span><span class="sxs-lookup"><span data-stu-id="f69f1-106">See Remarks for definitions of terms.</span></span>

## <a name="syntax"></a><span data-ttu-id="f69f1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f69f1-107">Syntax</span></span>


```C++
typedef enum D3DBLENDOP { 
  D3DBLENDOP_ADD          = 1,
  D3DBLENDOP_SUBTRACT     = 2,
  D3DBLENDOP_REVSUBTRACT  = 3,
  D3DBLENDOP_MIN          = 4,
  D3DBLENDOP_MAX          = 5,
  D3DBLENDOP_FORCE_DWORD  = 0x7fffffff
} D3DBLENDOP, *LPD3DBLENDOP;
```



## <a name="constants"></a><span data-ttu-id="f69f1-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="f69f1-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f69f1-109"><span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP \_ Hinzufügen**</span><span class="sxs-lookup"><span data-stu-id="f69f1-109"><span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP\_ADD**</span></span>
</dt> <dd>

<span data-ttu-id="f69f1-110">Das Ergebnis ist das Ziel, das der Quelle hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f69f1-110">The result is the destination added to the source.</span></span> <span data-ttu-id="f69f1-111">Result = Quelle + Ziel</span><span class="sxs-lookup"><span data-stu-id="f69f1-111">Result = Source + Destination</span></span>

</dd> <dt>

<span data-ttu-id="f69f1-112"><span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**D3DBLENDOP \_ subtrahieren**</span><span class="sxs-lookup"><span data-stu-id="f69f1-112"><span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**D3DBLENDOP\_SUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="f69f1-113">Das Ergebnis ist das Ziel, das von an die Quelle subtrahiert wird.</span><span class="sxs-lookup"><span data-stu-id="f69f1-113">The result is the destination subtracted from to the source.</span></span> <span data-ttu-id="f69f1-114">Result = Quelle-Ziel</span><span class="sxs-lookup"><span data-stu-id="f69f1-114">Result = Source - Destination</span></span>

</dd> <dt>

<span data-ttu-id="f69f1-115"><span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**D3DBLENDOP \_ revsubtract**</span><span class="sxs-lookup"><span data-stu-id="f69f1-115"><span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**D3DBLENDOP\_REVSUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="f69f1-116">Das Ergebnis ist die Quelle, die vom Ziel subtrahiert wird.</span><span class="sxs-lookup"><span data-stu-id="f69f1-116">The result is the source subtracted from the destination.</span></span> <span data-ttu-id="f69f1-117">Result = Ziel-Quelle</span><span class="sxs-lookup"><span data-stu-id="f69f1-117">Result = Destination - Source</span></span>

</dd> <dt>

<span data-ttu-id="f69f1-118"><span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP \_ Min.**</span><span class="sxs-lookup"><span data-stu-id="f69f1-118"><span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP\_MIN**</span></span>
</dt> <dd>

<span data-ttu-id="f69f1-119">Das Ergebnis ist das Minimalwert der Quelle und des Ziels.</span><span class="sxs-lookup"><span data-stu-id="f69f1-119">The result is the minimum of the source and destination.</span></span> <span data-ttu-id="f69f1-120">Ergebnis = min (Quelle, Ziel)</span><span class="sxs-lookup"><span data-stu-id="f69f1-120">Result = MIN(Source, Destination)</span></span>

</dd> <dt>

<span data-ttu-id="f69f1-121"><span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP \_ Max**</span><span class="sxs-lookup"><span data-stu-id="f69f1-121"><span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="f69f1-122">Das Ergebnis ist der Höchstwert der Quelle und des Ziels.</span><span class="sxs-lookup"><span data-stu-id="f69f1-122">The result is the maximum of the source and destination.</span></span> <span data-ttu-id="f69f1-123">Result = Max (Quelle, Ziel)</span><span class="sxs-lookup"><span data-stu-id="f69f1-123">Result = MAX(Source, Destination)</span></span>

</dd> <dt>

<span data-ttu-id="f69f1-124"><span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f69f1-124"><span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="f69f1-125">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="f69f1-125">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="f69f1-126">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="f69f1-126">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="f69f1-127">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f69f1-127">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f69f1-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f69f1-128">Remarks</span></span>

<span data-ttu-id="f69f1-129">Quelle, Ziel und Ergebnis werden wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="f69f1-129">Source, Destination, and Result are defined as:</span></span>



| <span data-ttu-id="f69f1-130">Begriff</span><span class="sxs-lookup"><span data-stu-id="f69f1-130">Term</span></span>        | <span data-ttu-id="f69f1-131">type</span><span class="sxs-lookup"><span data-stu-id="f69f1-131">Type</span></span>   | <span data-ttu-id="f69f1-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f69f1-132">Description</span></span>                                                            |
|-------------|--------|------------------------------------------------------------------------|
| <span data-ttu-id="f69f1-133">`Source`</span><span class="sxs-lookup"><span data-stu-id="f69f1-133">Source</span></span>      | <span data-ttu-id="f69f1-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f69f1-134">Input</span></span>  | <span data-ttu-id="f69f1-135">Farbe des Quell Pixels vor dem Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f69f1-135">Color of the source pixel before the operation.</span></span>                        |
| <span data-ttu-id="f69f1-136">Destination</span><span class="sxs-lookup"><span data-stu-id="f69f1-136">Destination</span></span> | <span data-ttu-id="f69f1-137">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f69f1-137">Input</span></span>  | <span data-ttu-id="f69f1-138">Farbe des Pixels im Ziel Puffer vor dem Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f69f1-138">Color of the pixel in the destination buffer before the operation.</span></span>     |
| <span data-ttu-id="f69f1-139">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="f69f1-139">Result</span></span>      | <span data-ttu-id="f69f1-140">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="f69f1-140">Output</span></span> | <span data-ttu-id="f69f1-141">Der zurückgegebene Wert, der die aus dem Vorgang resultierende gemischte Farbe ist.</span><span class="sxs-lookup"><span data-stu-id="f69f1-141">Returned value that is the blended color resulting from the operation.</span></span> |



 

<span data-ttu-id="f69f1-142">Dieser enumerierte Typ definiert die Werte, die von den folgenden Rendering-Zuständen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="f69f1-142">This enumerated type defines values used by the following render states:</span></span>

-   <span data-ttu-id="f69f1-143">D3DRS \_ blendop</span><span class="sxs-lookup"><span data-stu-id="f69f1-143">D3DRS\_BLENDOP</span></span>
-   <span data-ttu-id="f69f1-144">D3DRS \_ blendopalpha</span><span class="sxs-lookup"><span data-stu-id="f69f1-144">D3DRS\_BLENDOPALPHA</span></span>

## <a name="requirements"></a><span data-ttu-id="f69f1-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f69f1-145">Requirements</span></span>



| <span data-ttu-id="f69f1-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f69f1-146">Requirement</span></span> | <span data-ttu-id="f69f1-147">Wert</span><span class="sxs-lookup"><span data-stu-id="f69f1-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f69f1-148">Header</span><span class="sxs-lookup"><span data-stu-id="f69f1-148">Header</span></span><br/> | <dl> <span data-ttu-id="f69f1-149"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f69f1-149"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f69f1-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f69f1-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f69f1-151">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="f69f1-151">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="f69f1-152">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="f69f1-152">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="f69f1-153">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="f69f1-153">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
