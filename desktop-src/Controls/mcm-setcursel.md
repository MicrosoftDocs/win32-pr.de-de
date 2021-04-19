---
title: MCM_SETCURSEL Meldung (kommstrg. h)
description: Legt das aktuell ausgewählte Datum für ein Monatskalender-Steuerelement fest. Wenn das angegebene Datum nicht in der Ansicht enthalten ist, aktualisiert das Steuerelement die Anzeige, um es anzuzeigen. Sie können diese Nachricht explizit oder mit dem monthcal \_ setcurrsel-Makro senden.
ms.assetid: 2a9f82a1-66d9-44dd-b60f-b588b4688316
keywords:
- Windows-Steuerelemente für MCM_SETCURSEL Meldung
topic_type:
- apiref
api_name:
- MCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cceff48fbc4ffdb7446277d506c369e1bd89c92b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346336"
---
# <a name="mcm_setcursel-message"></a><span data-ttu-id="6f541-106">MCM- \_ setcurrsel-Meldung</span><span class="sxs-lookup"><span data-stu-id="6f541-106">MCM\_SETCURSEL message</span></span>

<span data-ttu-id="6f541-107">Legt das aktuell ausgewählte Datum für ein Monatskalender-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="6f541-107">Sets the currently selected date for a month calendar control.</span></span> <span data-ttu-id="6f541-108">Wenn das angegebene Datum nicht in der Ansicht enthalten ist, aktualisiert das Steuerelement die Anzeige, um es anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6f541-108">If the specified date is not in view, the control updates the display to bring it into view.</span></span> <span data-ttu-id="6f541-109">Sie können diese Nachricht explizit oder mit dem [**monthcal \_ setcurrsel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="6f541-109">You can send this message explicitly or by using the [**MonthCal\_SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6f541-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f541-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f541-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f541-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6f541-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="6f541-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6f541-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f541-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f541-114">Ein Zeiger auf eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die das Datum enthält, das als aktuelle Auswahl festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6f541-114">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date to be set as the current selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f541-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f541-115">Return value</span></span>

<span data-ttu-id="6f541-116">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="6f541-116">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="6f541-117">Diese Nachricht schlägt fehl, wenn Sie auf ein Monatskalender-Steuerelement angewendet wird, das das [**MCS- \_ MultiSelect**](month-calendar-control-styles.md) -Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="6f541-117">This message will fail if applied to a month calendar control that uses the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f541-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f541-118">Requirements</span></span>



| <span data-ttu-id="6f541-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f541-119">Requirement</span></span> | <span data-ttu-id="6f541-120">Wert</span><span class="sxs-lookup"><span data-stu-id="6f541-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f541-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f541-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6f541-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f541-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6f541-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f541-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6f541-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f541-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6f541-125">Header</span><span class="sxs-lookup"><span data-stu-id="6f541-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f541-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f541-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f541-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f541-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f541-128">Uhrzeiten im Monatskalender-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="6f541-128">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

