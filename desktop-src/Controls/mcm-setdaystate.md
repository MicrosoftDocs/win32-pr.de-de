---
title: MCM_SETDAYSTATE Meldung (kommstrg. h)
description: Legt die Tages Zustände für alle Monate fest, die gegenwärtig innerhalb eines Monatskalender-Steuer Elements sichtbar sind. Sie können diese Nachricht explizit oder mit dem monthcal \_ SetDayState-Makro senden.
ms.assetid: 518cb2a9-ea82-40b4-88ca-f901b6f9f8c4
keywords:
- Windows-Steuerelemente für MCM_SETDAYSTATE Meldung
topic_type:
- apiref
api_name:
- MCM_SETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6174cc7d8d97d424d599671740530dd8014cc998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478957"
---
# <a name="mcm_setdaystate-message"></a><span data-ttu-id="fbc8f-105">MCM \_ SetDayState-Meldung</span><span class="sxs-lookup"><span data-stu-id="fbc8f-105">MCM\_SETDAYSTATE message</span></span>

<span data-ttu-id="fbc8f-106">Legt die Tages Zustände für alle Monate fest, die gegenwärtig innerhalb eines Monatskalender-Steuer Elements sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="fbc8f-106">Sets the day states for all months that are currently visible within a month calendar control.</span></span> <span data-ttu-id="fbc8f-107">Sie können diese Nachricht explizit oder mit dem [**monthcal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="fbc8f-107">You can send this message explicitly or by using the [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fbc8f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbc8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbc8f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fbc8f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fbc8f-110">Ein Wert, der angibt, wie viele Elemente im Array sind, auf das *LPARAM* zeigt.</span><span class="sxs-lookup"><span data-stu-id="fbc8f-110">Value indicating how many elements are in the array that *lParam* points to.</span></span>

</dd> <dt>

<span data-ttu-id="fbc8f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fbc8f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fbc8f-112">Ein Zeiger auf ein Array von [**MONTHDAYSTATE**](monthdaystate.md) -Werten, die definieren, wie das Monatskalender-Steuerelement jeden Tag in der Anzeige zeichnen wird.</span><span class="sxs-lookup"><span data-stu-id="fbc8f-112">Pointer to an array of [**MONTHDAYSTATE**](monthdaystate.md) values that define how the month calendar control will draw each day in its display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbc8f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fbc8f-113">Return value</span></span>

<span data-ttu-id="fbc8f-114">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="fbc8f-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbc8f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbc8f-115">Remarks</span></span>

<span data-ttu-id="fbc8f-116">Eine Anwendung kann die Tages Zustandsinformationen explizit festlegen, indem diese Nachricht gesendet wird. der Zustand wird jedoch nicht beibehalten, wenn ein anderer Teil des Kalenders in der Ansicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fbc8f-116">An application can explicitly set day state information by sending this message, but the state will not persist when a different part of the calendar is scrolled into view.</span></span> <span data-ttu-id="fbc8f-117">Die Tages Zustandsinformationen werden in der Regel als Reaktion auf den [MCN \_ getdaystate](mcn-getdaystate.md) -Benachrichtigungs Code festgelegt, der immer dann gesendet wird, wenn das Steuerelement aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="fbc8f-117">Day state information is usually set in response to the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code, which is sent whenever the control needs to be refreshed.</span></span>

<span data-ttu-id="fbc8f-118">Das Array bei *LPARAM* muss so viele Elemente enthalten wie der Wert, der vom folgenden Makro zurückgegeben wird:</span><span class="sxs-lookup"><span data-stu-id="fbc8f-118">The array at *lParam* must contain as many elements as the value returned by the following macro:</span></span>

`MonthCal_GetMonthRange(hwndMC, GMR_DAYSTATE, NULL);`

<span data-ttu-id="fbc8f-119">Beachten Sie, dass das Array bei *LPARAM* die [**MONTHDAYSTATE**](monthdaystate.md) -Werte enthalten muss, die mit allen Monaten übereinstimmen, die sich derzeit in der Anzeige des Steuer Elements in chronologischer Reihenfolge befinden.</span><span class="sxs-lookup"><span data-stu-id="fbc8f-119">Keep in mind that the array at *lParam* must contain [**MONTHDAYSTATE**](monthdaystate.md) values that correspond with all months currently in the control's display, in chronological order.</span></span> <span data-ttu-id="fbc8f-120">Dies schließt die zwei Monate ein, die möglicherweise vor dem ersten Monat und nach dem letzten Monat teilweise angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fbc8f-120">This includes the two months that may be partially displayed before the first month and after the last month.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbc8f-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbc8f-121">Requirements</span></span>



| <span data-ttu-id="fbc8f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbc8f-122">Requirement</span></span> | <span data-ttu-id="fbc8f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="fbc8f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fbc8f-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fbc8f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fbc8f-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbc8f-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fbc8f-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fbc8f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fbc8f-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbc8f-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fbc8f-128">Header</span><span class="sxs-lookup"><span data-stu-id="fbc8f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbc8f-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbc8f-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbc8f-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbc8f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbc8f-131">Verwenden von Monatskalender-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="fbc8f-131">Using Month Calendar Controls</span></span>](using-month-calendar-controls.md)
</dt> </dl>

 

 





