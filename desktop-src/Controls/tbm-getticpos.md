---
title: TBM_GETTICPOS Meldung (kommstrg. h)
description: Ruft die aktuelle physische Position eines Teil Strichs in einer TrackBar ab.
ms.assetid: a4b0ec32-ef4e-4607-ade1-5e2be02bebe4
keywords:
- Windows-Steuerelemente für TBM_GETTICPOS Meldung
topic_type:
- apiref
api_name:
- TBM_GETTICPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb1346f63e9bb10b919c678373e0e8df0724861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338544"
---
# <a name="tbm_getticpos-message"></a><span data-ttu-id="fbb92-104">TBM- \_ GetTicPos-Nachricht</span><span class="sxs-lookup"><span data-stu-id="fbb92-104">TBM\_GETTICPOS message</span></span>

<span data-ttu-id="fbb92-105">Ruft die aktuelle physische Position eines Teil Strichs in einer TrackBar ab.</span><span class="sxs-lookup"><span data-stu-id="fbb92-105">Retrieves the current physical position of a tick mark in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="fbb92-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbb92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbb92-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fbb92-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fbb92-108">NULL basierter Index, der einen Teil Strich identifiziert.</span><span class="sxs-lookup"><span data-stu-id="fbb92-108">Zero-based index identifying a tick mark.</span></span> <span data-ttu-id="fbb92-109">Die Positionen des ersten und letzten Teil Strichs sind nicht direkt über diese Meldung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fbb92-109">The positions of the first and last tick marks are not directly available via this message.</span></span>

</dd> <dt>

<span data-ttu-id="fbb92-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fbb92-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fbb92-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="fbb92-111">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbb92-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fbb92-112">Return value</span></span>

<span data-ttu-id="fbb92-113">Gibt die Entfernung in Client Koordinaten vom linken oder oberen Rand des Client Bereichs der TrackBar zum angegebenen Teil Strich zurück.</span><span class="sxs-lookup"><span data-stu-id="fbb92-113">Returns the distance, in client coordinates, from the left or top of the trackbar's client area to the specified tick mark.</span></span> <span data-ttu-id="fbb92-114">Der Rückgabewert ist die x-Koordinate des Teil Strichs für eine horizontale Trackleiste oder die y-Koordinate für eine vertikale TrackBar.</span><span class="sxs-lookup"><span data-stu-id="fbb92-114">The return value is the x-coordinate of the tick mark for a horizontal trackbar or the y-coordinate for a vertical trackbar.</span></span> <span data-ttu-id="fbb92-115">Wenn *wParam* kein gültiger Index ist, ist der Rückgabewert-1.</span><span class="sxs-lookup"><span data-stu-id="fbb92-115">If *wParam* is not a valid index, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbb92-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbb92-116">Remarks</span></span>

<span data-ttu-id="fbb92-117">Da der erste und der letzte Teil Strich über diese Nachricht nicht verfügbar sind, werden gültige Indizes von der Tick-Position auf der TrackBar versetzt.</span><span class="sxs-lookup"><span data-stu-id="fbb92-117">Because the first and last tick marks are not available through this message, valid indexes are offset from their tick position on the trackbar.</span></span> <span data-ttu-id="fbb92-118">Wenn der Unterschied zwischen [**TBM \_ getrangemin**](tbm-getrangemin.md) und [**TBM \_ getrangemax**](tbm-getrangemax.md) kleiner als zwei ist, gibt es keinen gültigen Index, und diese Meldung schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="fbb92-118">If the difference between [**TBM\_GETRANGEMIN**](tbm-getrangemin.md) and [**TBM\_GETRANGEMAX**](tbm-getrangemax.md) is less than two, then there is no valid index and this message will fail.</span></span>

<span data-ttu-id="fbb92-119">Im folgenden Beispiel wird die Beziehung zwischen den Ticks auf einer TrackBar, den in dieser Meldung verfügbaren Ticks und ihren Null basierten Indizes veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="fbb92-119">The following illustrates the relation between the ticks on a trackbar, the ticks available through this message, and their zero-based indexes.</span></span>

``` syntax
0 1 2 3 4 5 6 7 8 9    // Tick positions seen on the trackbar.
  1 2 3 4 5 6 7 8      // Tick positions whose position can be identified.
  0 1 2 3 4 5 6 7      // Index numbers for the identifiable positions.
```

## <a name="requirements"></a><span data-ttu-id="fbb92-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbb92-120">Requirements</span></span>



| <span data-ttu-id="fbb92-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbb92-121">Requirement</span></span> | <span data-ttu-id="fbb92-122">Wert</span><span class="sxs-lookup"><span data-stu-id="fbb92-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fbb92-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fbb92-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fbb92-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbb92-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fbb92-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fbb92-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fbb92-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbb92-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fbb92-127">Header</span><span class="sxs-lookup"><span data-stu-id="fbb92-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbb92-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbb92-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





