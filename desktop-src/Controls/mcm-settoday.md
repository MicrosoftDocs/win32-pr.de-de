---
title: MCM_SETTODAY Meldung (kommstrg. h)
description: Legt den \ 0034; heute \ 0034; fest. Auswahl für ein Monatskalender-Steuerelement. Sie können diese Nachricht explizit oder mit dem monthcal- \_ settoday-Makro senden.
ms.assetid: fcd4d33d-e661-4e02-8d19-666d80e1a070
keywords:
- Windows-Steuerelemente für MCM_SETTODAY Meldung
topic_type:
- apiref
api_name:
- MCM_SETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b725e5f61e3c08170a323b063616434acb857e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743816"
---
# <a name="mcm_settoday-message"></a><span data-ttu-id="3217d-105">MCM \_ settoday-Meldung</span><span class="sxs-lookup"><span data-stu-id="3217d-105">MCM\_SETTODAY message</span></span>

<span data-ttu-id="3217d-106">Legt die Auswahl "heute" für ein Monatskalender-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="3217d-106">Sets the "today" selection for a month calendar control.</span></span> <span data-ttu-id="3217d-107">Sie können diese Nachricht explizit oder mit dem [**monthcal- \_ settoday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="3217d-107">You can send this message explicitly or by using the [**MonthCal\_SetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3217d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3217d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3217d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3217d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3217d-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="3217d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3217d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3217d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3217d-112">Ein Zeiger auf eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die das Datum enthält, das als "heutige" Auswahl für das Steuerelement festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3217d-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date to be set as the "today" selection for the control.</span></span> <span data-ttu-id="3217d-113">Wenn dieser Parameter auf **null** festgelegt ist, wird das Steuerelement zur Standardeinstellung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3217d-113">If this parameter is set to **NULL**, the control returns to the default setting.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3217d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3217d-114">Return value</span></span>

<span data-ttu-id="3217d-115">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3217d-115">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="3217d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3217d-116">Remarks</span></span>

<span data-ttu-id="3217d-117">Wenn die Auswahl "heute" auf ein anderes Datum als die Standardeinstellung festgelegt ist, gelten die folgenden Bedingungen:</span><span class="sxs-lookup"><span data-stu-id="3217d-117">If the "today" selection is set to any date other than the default, the following conditions apply:</span></span>

-   <span data-ttu-id="3217d-118">Das Steuerelement aktualisiert die "heute"-Auswahl nicht automatisch, wenn die Zeit für den aktuellen Tag Mitternacht überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="3217d-118">The control will not automatically update the "today" selection when the time passes midnight for the current day.</span></span>
-   <span data-ttu-id="3217d-119">Das-Steuerelement aktualisiert seine Anzeige nicht automatisch basierend auf Gebiets Schema Änderungen.</span><span class="sxs-lookup"><span data-stu-id="3217d-119">The control will not automatically update its display based on locale changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="3217d-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3217d-120">Requirements</span></span>



| <span data-ttu-id="3217d-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3217d-121">Requirement</span></span> | <span data-ttu-id="3217d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="3217d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3217d-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3217d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3217d-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3217d-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3217d-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3217d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3217d-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3217d-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3217d-127">Header</span><span class="sxs-lookup"><span data-stu-id="3217d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3217d-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3217d-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3217d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3217d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3217d-130">Uhrzeiten im Monatskalender-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3217d-130">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

