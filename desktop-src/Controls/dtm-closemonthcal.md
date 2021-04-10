---
title: DTM_CLOSEMONTHCAL Meldung (kommstrg. h)
description: Schließt ein DTP-Steuerelement (Datums-und Zeitauswahl). Senden Sie diese Nachricht explizit oder mithilfe des "DateTime \_ closemonthcal"-Makros.
ms.assetid: f60af77f-ec34-4f3d-9427-cda7ac6083bf
keywords:
- Windows-Steuerelemente für DTM_CLOSEMONTHCAL Meldung
topic_type:
- apiref
api_name:
- DTM_CLOSEMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd79f33576490196bf29fd51316f8ce3daf4ad4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040186"
---
# <a name="dtm_closemonthcal-message"></a><span data-ttu-id="72153-105">DTM \_ closemonthcal-Nachricht</span><span class="sxs-lookup"><span data-stu-id="72153-105">DTM\_CLOSEMONTHCAL message</span></span>

<span data-ttu-id="72153-106">Schließt ein DTP-Steuerelement (Datums-und Zeitauswahl).</span><span class="sxs-lookup"><span data-stu-id="72153-106">Closes a date and time picker (DTP) control.</span></span> <span data-ttu-id="72153-107">Senden Sie diese Nachricht explizit oder mithilfe des " [**DateTime \_ closemonthcal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) "-Makros.</span><span class="sxs-lookup"><span data-stu-id="72153-107">Send this message explicitly or by using the [**DateTime\_CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="72153-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="72153-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72153-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="72153-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72153-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="72153-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="72153-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="72153-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="72153-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="72153-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72153-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72153-113">Return value</span></span>

<span data-ttu-id="72153-114">Gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="72153-114">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="72153-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72153-115">Remarks</span></span>

<span data-ttu-id="72153-116">Zerstört das-Steuerelement und sendet eine [Dtn- \_ closeup](dtn-closeup.md) -Benachrichtigung, dass das-Steuerelement geschlossen wird, anstatt das-Steuerelement zu öffnen (in der [Dtn- \_ Dropdown](dtn-dropdown.md) Benachrichtigung), an das übergeordnete Steuerelement des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="72153-116">Destroys the control and sends a [DTN\_CLOSEUP](dtn-closeup.md) notification that the control is closing as opposed to the control is opening (dropping-down as in the [DTN\_DROPDOWN](dtn-dropdown.md) notification) to the control's parent.</span></span>

## <a name="requirements"></a><span data-ttu-id="72153-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72153-117">Requirements</span></span>



| <span data-ttu-id="72153-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72153-118">Requirement</span></span> | <span data-ttu-id="72153-119">Wert</span><span class="sxs-lookup"><span data-stu-id="72153-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72153-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72153-120">Minimum supported client</span></span><br/> | <span data-ttu-id="72153-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72153-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="72153-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72153-122">Minimum supported server</span></span><br/> | <span data-ttu-id="72153-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72153-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="72153-124">Header</span><span class="sxs-lookup"><span data-stu-id="72153-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="72153-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="72153-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72153-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72153-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="72153-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="72153-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="72153-128">DTN- \_ Dropdown</span><span class="sxs-lookup"><span data-stu-id="72153-128">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="72153-129">DTN- \_ Schließung</span><span class="sxs-lookup"><span data-stu-id="72153-129">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> </dl>

 

 





