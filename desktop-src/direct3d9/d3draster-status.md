---
description: Beschreibt den Raster Status.
ms.assetid: f7b5b714-8fc8-47b8-adec-1089b8d07081
title: D3DRASTER_STATUS-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRASTER_STATUS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e77ab0e6ee164eadae862ed03df5652c21ba7040
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361215"
---
# <a name="d3draster_status-structure"></a><span data-ttu-id="07c8e-103">D3DRASTER- \_ Status Struktur</span><span class="sxs-lookup"><span data-stu-id="07c8e-103">D3DRASTER\_STATUS structure</span></span>

<span data-ttu-id="07c8e-104">Beschreibt den Raster Status.</span><span class="sxs-lookup"><span data-stu-id="07c8e-104">Describes the raster status.</span></span>

## <a name="syntax"></a><span data-ttu-id="07c8e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="07c8e-105">Syntax</span></span>


```C++
typedef struct D3DRASTER_STATUS {
  BOOL InVBlank;
  UINT ScanLine;
} D3DRASTER_STATUS, *LPD3DRASTER_STATUS;
```



## <a name="members"></a><span data-ttu-id="07c8e-106">Member</span><span class="sxs-lookup"><span data-stu-id="07c8e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="07c8e-107">**Nicht angegeben**</span><span class="sxs-lookup"><span data-stu-id="07c8e-107">**InVBlank**</span></span>
</dt> <dd>

<span data-ttu-id="07c8e-108">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07c8e-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07c8e-109">**True** , wenn sich das Raster im vertikalen leeren Zeitraum befindet.</span><span class="sxs-lookup"><span data-stu-id="07c8e-109">**TRUE** if the raster is in the vertical blank period.</span></span> <span data-ttu-id="07c8e-110">**False** , wenn sich das Raster nicht im vertikalen leeren Zeitraum befindet.</span><span class="sxs-lookup"><span data-stu-id="07c8e-110">**FALSE** if the raster is not in the vertical blank period.</span></span>

</dd> <dt>

<span data-ttu-id="07c8e-111">**Scanline**</span><span class="sxs-lookup"><span data-stu-id="07c8e-111">**ScanLine**</span></span>
</dt> <dd>

<span data-ttu-id="07c8e-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07c8e-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07c8e-113">Wenn "invblank" den Wert " **false**" hat, ist dieser Wert eine ganze Zahl, die ungefähr der aktuellen Scan Linie entspricht, die vom Raster gezeichnet wird</span><span class="sxs-lookup"><span data-stu-id="07c8e-113">If InVBlank is **FALSE**, then this value is an integer roughly corresponding to the current scan line painted by the raster.</span></span> <span data-ttu-id="07c8e-114">Überprüfungs Zeilen werden auf die gleiche Weise wie Direct3D Surface-Koordinaten nummeriert: 0 ist der obere Teil der primären Oberfläche und erweitert auf den Wert (Höhe von Oberfläche-1) am unteren Rand der Anzeige.</span><span class="sxs-lookup"><span data-stu-id="07c8e-114">Scan lines are numbered in the same way as Direct3D surface coordinates: 0 is the top of the primary surface, extending to the value (height of the surface - 1) at the bottom of the display.</span></span>

<span data-ttu-id="07c8e-115">Wenn "invblank" auf " **true**" festgelegt ist, wird dieser Wert auf NULL festgelegt und kann ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="07c8e-115">If InVBlank is **TRUE**, then this value is set to zero and can be ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07c8e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07c8e-116">Requirements</span></span>



| <span data-ttu-id="07c8e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07c8e-117">Requirement</span></span> | <span data-ttu-id="07c8e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="07c8e-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07c8e-119">Header</span><span class="sxs-lookup"><span data-stu-id="07c8e-119">Header</span></span><br/> | <dl> <span data-ttu-id="07c8e-120"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="07c8e-120"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07c8e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07c8e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07c8e-122">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="07c8e-122">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="07c8e-123">**GetRasterStatus**</span><span class="sxs-lookup"><span data-stu-id="07c8e-123">**GetRasterStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)
</dt> </dl>

 

 
