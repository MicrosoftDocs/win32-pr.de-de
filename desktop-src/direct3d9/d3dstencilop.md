---
description: Definiert Schablonen Puffer Vorgänge.
ms.assetid: 338a3b7f-236a-484f-96b8-1e6bfb014484
title: D3DSTENCILOP-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTENCILOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 34784a57d3afd3862d380554040f3909ec905898
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371900"
---
# <a name="d3dstencilop-enumeration"></a><span data-ttu-id="ffedc-103">D3DSTENCILOP-Enumeration</span><span class="sxs-lookup"><span data-stu-id="ffedc-103">D3DSTENCILOP enumeration</span></span>

<span data-ttu-id="ffedc-104">Definiert Schablonen Puffer Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="ffedc-104">Defines stencil-buffer operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffedc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffedc-105">Syntax</span></span>


```C++
typedef enum D3DSTENCILOP { 
  D3DSTENCILOP_KEEP         = 1,
  D3DSTENCILOP_ZERO         = 2,
  D3DSTENCILOP_REPLACE      = 3,
  D3DSTENCILOP_INCRSAT      = 4,
  D3DSTENCILOP_DECRSAT      = 5,
  D3DSTENCILOP_INVERT       = 6,
  D3DSTENCILOP_INCR         = 7,
  D3DSTENCILOP_DECR         = 8,
  D3DSTENCILOP_FORCE_DWORD  = 0x7fffffff
} D3DSTENCILOP, *LPD3DSTENCILOP;
```



## <a name="constants"></a><span data-ttu-id="ffedc-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="ffedc-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ffedc-107"><span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCILOP \_ beibehalten**</span><span class="sxs-lookup"><span data-stu-id="ffedc-107"><span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCILOP\_KEEP**</span></span>
</dt> <dd>

<span data-ttu-id="ffedc-108">Aktualisieren Sie den Eintrag nicht im Schablonen Puffer.</span><span class="sxs-lookup"><span data-stu-id="ffedc-108">Do not update the entry in the stencil buffer.</span></span> <span data-ttu-id="ffedc-109">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="ffedc-109">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="ffedc-110"><span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP \_ 0**</span><span class="sxs-lookup"><span data-stu-id="ffedc-110"><span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP\_ZERO**</span></span>
</dt> <dd>

<span data-ttu-id="ffedc-111">Legen Sie den Schablone-Puffer Eintrag auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="ffedc-111">Set the stencil-buffer entry to 0.</span></span>

</dd> <dt>

<span data-ttu-id="ffedc-112"><span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCILOP \_ ersetzen**</span><span class="sxs-lookup"><span data-stu-id="ffedc-112"><span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCILOP\_REPLACE**</span></span>
</dt> <dd>

<span data-ttu-id="ffedc-113">Ersetzen Sie den Stencil-Buffer-Eintrag durch einen Verweis Wert.</span><span class="sxs-lookup"><span data-stu-id="ffedc-113">Replace the stencil-buffer entry with a reference value.</span></span>

</dd> <dt>

<span data-ttu-id="ffedc-114"><span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**D3DSTENCILOP \_ incrsat**</span><span class="sxs-lookup"><span data-stu-id="ffedc-114"><span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**D3DSTENCILOP\_INCRSAT**</span></span>
</dt> <dd>

<span data-ttu-id="ffedc-115">Erhöhen Sie den Schablone-Puffer Eintrag, und legen Sie auf den maximalen Wert an.</span><span class="sxs-lookup"><span data-stu-id="ffedc-115">Increment the stencil-buffer entry, clamping to the maximum value.</span></span>

</dd> <dt>

<span data-ttu-id="ffedc-116"><span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**D3DSTENCILOP \_ decrsat**</span><span class="sxs-lookup"><span data-stu-id="ffedc-116"><span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**D3DSTENCILOP\_DECRSAT**</span></span>
</dt> <dd>

<span data-ttu-id="ffedc-117">Dekrement der Schablone-Puffer Eintrag, der auf 0 (null) gesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="ffedc-117">Decrement the stencil-buffer entry, clamping to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ffedc-118"><span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**D3DSTENCILOP \_ umkehren**</span><span class="sxs-lookup"><span data-stu-id="ffedc-118"><span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**D3DSTENCILOP\_INVERT**</span></span>
</dt> <dd>

<span data-ttu-id="ffedc-119">Umkehren Sie die Bits im Schablone-Puffer Eintrag.</span><span class="sxs-lookup"><span data-stu-id="ffedc-119">Invert the bits in the stencil-buffer entry.</span></span>

</dd> <dt>

<span data-ttu-id="ffedc-120"><span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**D3DSTENCILOP \_ INCR**</span><span class="sxs-lookup"><span data-stu-id="ffedc-120"><span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**D3DSTENCILOP\_INCR**</span></span>
</dt> <dd>

<span data-ttu-id="ffedc-121">Erhöhen Sie den Schablonen Puffer Eintrag, wobei der Wert auf 0 (null) umwickelt wird, wenn der neue Wert den maximalen Wert überschreitet.</span><span class="sxs-lookup"><span data-stu-id="ffedc-121">Increment the stencil-buffer entry, wrapping to zero if the new value exceeds the maximum value.</span></span>

</dd> <dt>

<span data-ttu-id="ffedc-122"><span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**D3DSTENCILOP- \_ decr**</span><span class="sxs-lookup"><span data-stu-id="ffedc-122"><span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**D3DSTENCILOP\_DECR**</span></span>
</dt> <dd>

<span data-ttu-id="ffedc-123">Verringert den Schablonen Puffer Eintrag und umwickelt ihn in den maximalen Wert, wenn der neue Wert kleiner als 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="ffedc-123">Decrement the stencil-buffer entry, wrapping to the maximum value if the new value is less than zero.</span></span>

</dd> <dt>

<span data-ttu-id="ffedc-124"><span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCILOP \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ffedc-124"><span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCILOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="ffedc-125">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="ffedc-125">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="ffedc-126">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="ffedc-126">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="ffedc-127">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ffedc-127">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ffedc-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffedc-128">Remarks</span></span>

<span data-ttu-id="ffedc-129">Schablone-Puffer Einträge sind ganzzahlige Werte im Bereich von 0 bis 2 ⁿ-1, wobei n die Bittiefe des Schablonen Puffers ist.</span><span class="sxs-lookup"><span data-stu-id="ffedc-129">Stencil-buffer entries are integer values ranging from 0 through 2ⁿ - 1, where n is the bit depth of the stencil buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffedc-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffedc-130">Requirements</span></span>



| <span data-ttu-id="ffedc-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffedc-131">Requirement</span></span> | <span data-ttu-id="ffedc-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ffedc-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffedc-133">Header</span><span class="sxs-lookup"><span data-stu-id="ffedc-133">Header</span></span><br/> | <dl> <span data-ttu-id="ffedc-134"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffedc-134"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffedc-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffedc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffedc-136">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="ffedc-136">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




