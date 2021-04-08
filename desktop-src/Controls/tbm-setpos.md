---
title: TBM_SETPOS Meldung (kommstrg. h)
description: Legt die aktuelle logische Position des Schiebereglers in einer TrackBar fest.
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- Windows-Steuerelemente für TBM_SETPOS Meldung
topic_type:
- apiref
api_name:
- TBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e8da6e8e231a26b216ca8f9314d59474384857
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957215"
---
# <a name="tbm_setpos-message"></a><span data-ttu-id="89661-104">TBM- \_ SetPos-Nachricht</span><span class="sxs-lookup"><span data-stu-id="89661-104">TBM\_SETPOS message</span></span>

<span data-ttu-id="89661-105">Legt die aktuelle logische Position des Schiebereglers in einer TrackBar fest.</span><span class="sxs-lookup"><span data-stu-id="89661-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="89661-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="89661-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89661-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="89661-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89661-108">Flag neu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="89661-108">Redraw flag.</span></span> <span data-ttu-id="89661-109">Wenn dieser Parameter **true** ist, zeichnet die Nachricht das Steuerelement mit dem Schieberegler an der Position, die von *LPARAM* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="89661-109">If this parameter is **TRUE**, the message redraws the control with the slider at the position given by *lParam*.</span></span> <span data-ttu-id="89661-110">Wenn dieser Parameter **false** ist, wird der Schieberegler von der Nachricht nicht an der neuen Position neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="89661-110">If this parameter is **FALSE**, the message does not redraw the slider at the new position.</span></span> <span data-ttu-id="89661-111">Beachten Sie, dass die Nachricht unabhängig vom *wParam* -Parameter den Wert der Schieberegler-Position festlegt (wie von der [**TBM- \_ GetPos**](tbm-getpos.md) -Nachricht zurückgegeben).</span><span class="sxs-lookup"><span data-stu-id="89661-111">Note that the message sets the value of the slider position (as returned by the [**TBM\_GETPOS**](tbm-getpos.md) message) regardless of the *wParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="89661-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89661-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89661-113">Neue logische Position des Schiebereglers.</span><span class="sxs-lookup"><span data-stu-id="89661-113">New logical position of the slider.</span></span> <span data-ttu-id="89661-114">Gültige logische Positionen sind die ganzzahligen Werte in der TrackBar-Bereich der minimalen bis maximalen Schieberegler-Positionen.</span><span class="sxs-lookup"><span data-stu-id="89661-114">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="89661-115">Wenn dieser Wert außerhalb des maximalen und minimalen Bereichs des Steuer Elements liegt, wird die Position auf den maximalen oder minimalen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="89661-115">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89661-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89661-116">Return value</span></span>

<span data-ttu-id="89661-117">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="89661-117">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="89661-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89661-118">Requirements</span></span>



| <span data-ttu-id="89661-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89661-119">Requirement</span></span> | <span data-ttu-id="89661-120">Wert</span><span class="sxs-lookup"><span data-stu-id="89661-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89661-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="89661-121">Minimum supported client</span></span><br/> | <span data-ttu-id="89661-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89661-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89661-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="89661-123">Minimum supported server</span></span><br/> | <span data-ttu-id="89661-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89661-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="89661-125">Header</span><span class="sxs-lookup"><span data-stu-id="89661-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="89661-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="89661-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





