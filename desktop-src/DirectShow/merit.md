---
description: Werte Werte definieren die Reihenfolge, in der der Filter Graph-Manager versucht, während der Diagramm Bildung Filter hinzuzufügen.
ms.assetid: 9e026675-e0a9-4c82-9b57-ab0e7d9592ea
title: Verdienst (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947a13d78f58c12c236ec31f0eeee1dc6d44f1d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361268"
---
# <a name="merit"></a><span data-ttu-id="e1e15-103">Verdienst</span><span class="sxs-lookup"><span data-stu-id="e1e15-103">Merit</span></span>

<span data-ttu-id="e1e15-104">Werte Werte definieren die Reihenfolge, in der der Filter Graph-Manager versucht, während der Diagramm Bildung Filter hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e1e15-104">Merit values define the order in which the Filter Graph Manager tries to add filters during graph building.</span></span>

<dl> <span data-ttu-id="e1e15-105"><span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**Verdienst \_ Bevorzugter** (0x800000) Wert <span id="MERIT_NORMAL"></span> <span id="merit_normal"></span> **\_ Normal** (0x600000) verdient <span id="MERIT_UNLIKELY"></span> <span id="merit_unlikely"></span> nicht **\_ wahrscheinliche** (0x400000) Wert <span id="MERIT_DO_NOT_USE"></span> <span id="merit_do_not_use"></span> **\_ \_ nicht \_ verwenden** (0x200.000) Verdienst- <span id="MERIT_SW_COMPRESSOR"></span> <span id="merit_sw_compressor"></span> **\_ SW- \_ Kompressor** (0x100000) <span id="MERIT_HW_COMPRESSOR"></span> <span id="merit_hw_compressor"></span> **Merit \_ HW- \_ Kompressor** (0x100050)</span><span class="sxs-lookup"><span data-stu-id="e1e15-105"><span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**MERIT\_PREFERRED** (0x800000) <span id="MERIT_NORMAL"></span><span id="merit_normal"></span>**MERIT\_NORMAL** (0x600000) <span id="MERIT_UNLIKELY"></span><span id="merit_unlikely"></span>**MERIT\_UNLIKELY** (0x400000) <span id="MERIT_DO_NOT_USE"></span><span id="merit_do_not_use"></span>**MERIT\_DO\_NOT\_USE** (0x200000) <span id="MERIT_SW_COMPRESSOR"></span><span id="merit_sw_compressor"></span>**MERIT\_SW\_COMPRESSOR** (0x100000) <span id="MERIT_HW_COMPRESSOR"></span><span id="merit_hw_compressor"></span>**MERIT\_HW\_COMPRESSOR** (0x100050)</span></span>
</dl>

## <a name="remarks"></a><span data-ttu-id="e1e15-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1e15-106">Remarks</span></span>

<span data-ttu-id="e1e15-107">Jeder Filter ist mit einem Verdienst Wert registriert.</span><span class="sxs-lookup"><span data-stu-id="e1e15-107">Each filter is registered with a merit value.</span></span> <span data-ttu-id="e1e15-108">Wenn der Filter Graph-Manager ein Diagramm erstellt, listet er alle Filter auf, die mit dem richtigen Medientyp registriert sind.</span><span class="sxs-lookup"><span data-stu-id="e1e15-108">When the filter graph manager builds a graph, it enumerates all the filters registered with the correct media type.</span></span> <span data-ttu-id="e1e15-109">Anschließend werden die Werte in der Reihenfolge ihrer Vorzüge, von der höchsten zum niedrigsten, ausprobiert.</span><span class="sxs-lookup"><span data-stu-id="e1e15-109">Then it tries them in order of merit, from highest to lowest.</span></span> <span data-ttu-id="e1e15-110">(Es werden zusätzliche Kriterien verwendet, um zwischen Filtern mit gleichem Verdienst auszuwählen.) Es werden niemals Filter mit einem Wert vom Wert "Value" **verwendet, \_ der \_ nicht \_ verwendet** wird.</span><span class="sxs-lookup"><span data-stu-id="e1e15-110">(It uses additional criteria to choose between filters with equal merit.) It never tries filters with a merit value less than or equal to **MERIT\_DO\_NOT\_USE**.</span></span>

<span data-ttu-id="e1e15-111">Ein Filter, der nie für die normale Wiedergabe berücksichtigt werden sollte, sollte den Vorteil haben, dass **\_ Sie \_ nicht \_** oder weniger verwenden.</span><span class="sxs-lookup"><span data-stu-id="e1e15-111">A filter that should never be considered for ordinary playback should have a merit of **MERIT\_DO\_NOT\_USE** or less.</span></span> <span data-ttu-id="e1e15-112">Filter können mit zwischen Werten registriert werden, die nicht von dieser Enumeration definiert werden, wie z. b. "Wert **\_ Normal** + 1".</span><span class="sxs-lookup"><span data-stu-id="e1e15-112">Filters can be registered with intermediate values not defined by this enumeration, such as **MERIT\_NORMAL** + 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1e15-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1e15-113">Requirements</span></span>



| <span data-ttu-id="e1e15-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1e15-114">Requirement</span></span> | <span data-ttu-id="e1e15-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e1e15-115">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e1e15-116">Header</span><span class="sxs-lookup"><span data-stu-id="e1e15-116">Header</span></span><br/> | <dl> <span data-ttu-id="e1e15-117"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1e15-117"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1e15-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1e15-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1e15-119">Konstanten und GUIDs</span><span class="sxs-lookup"><span data-stu-id="e1e15-119">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="e1e15-120">Richtlinien zum Registrieren von Filtern</span><span class="sxs-lookup"><span data-stu-id="e1e15-120">Guidelines for Registering Filters</span></span>](guidelines-for-registering-filters.md)
</dt> <dt>

[<span data-ttu-id="e1e15-121">Intelligent Connect</span><span class="sxs-lookup"><span data-stu-id="e1e15-121">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 




