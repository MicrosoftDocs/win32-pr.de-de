---
title: TTM_SETDELAYTIME Meldung (kommstrg. h)
description: Legt die Anfangs-, Popup-und neueinblenden Dauer für ein QuickInfo-Steuerelement fest.
ms.assetid: 0a73def0-550c-4d01-9cb1-1eb1f4356fa3
keywords:
- Windows-Steuerelemente für TTM_SETDELAYTIME Meldung
topic_type:
- apiref
api_name:
- TTM_SETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b633dc75baa0a8f385cf8cdb9bf7e9fa254809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956483"
---
# <a name="ttm_setdelaytime-message"></a><span data-ttu-id="c1ce1-104">TTM- \_ setdelta-Zeit Nachricht</span><span class="sxs-lookup"><span data-stu-id="c1ce1-104">TTM\_SETDELAYTIME message</span></span>

<span data-ttu-id="c1ce1-105">Legt die Anfangs-, Popup-und neueinblenden Dauer für ein QuickInfo-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="c1ce1-105">Sets the initial, pop-up, and reshow durations for a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c1ce1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1ce1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1ce1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1ce1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1ce1-108">Flag, das den festzulegenden Uhrzeitwert angibt.</span><span class="sxs-lookup"><span data-stu-id="c1ce1-108">Flag that specifies which time value to set.</span></span> <span data-ttu-id="c1ce1-109">Dieser Parameter kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="c1ce1-109">This parameter can be one of the following values</span></span>



| <span data-ttu-id="c1ce1-110">Wert</span><span class="sxs-lookup"><span data-stu-id="c1ce1-110">Value</span></span>                                                                                                                                                            | <span data-ttu-id="c1ce1-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c1ce1-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <span data-ttu-id="c1ce1-112"><dt>**ttdt- \_ autopop**</dt></span><span class="sxs-lookup"><span data-stu-id="c1ce1-112"><dt>**TTDT\_AUTOPOP**</dt></span></span> </dl>       | <span data-ttu-id="c1ce1-113">Legen Sie den Zeitraum fest, in dem ein QuickInfo-Fenster sichtbar bleibt, wenn der Zeiger innerhalb des umgebenden Rechtecks eines Tools stationär ist.</span><span class="sxs-lookup"><span data-stu-id="c1ce1-113">Set the amount of time a tooltip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span> <span data-ttu-id="c1ce1-114">Um die autopop-Verzögerungszeit auf den Standardwert zurückzusetzen, legen Sie *LPARAM* auf-1 fest.</span><span class="sxs-lookup"><span data-stu-id="c1ce1-114">To return the autopop delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                         |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <span data-ttu-id="c1ce1-115"><dt>**ttdt- \_ Initial**</dt></span><span class="sxs-lookup"><span data-stu-id="c1ce1-115"><dt>**TTDT\_INITIAL**</dt></span></span> </dl>       | <span data-ttu-id="c1ce1-116">Legen Sie den Zeitraum fest, in dem ein Zeiger innerhalb des umgebenden Rechtecks eines Tools stationär bleiben muss, bevor das QuickInfo-Fenster angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c1ce1-116">Set the amount of time a pointer must remain stationary within a tool's bounding rectangle before the tooltip window appears.</span></span> <span data-ttu-id="c1ce1-117">Legen Sie *LPARAM* auf-1 fest, um die anfängliche Verzögerungszeit auf den Standardwert zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="c1ce1-117">To return the initial delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                    |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <span data-ttu-id="c1ce1-118"><dt>**ttdt \_ erneut anzeigen**</dt></span><span class="sxs-lookup"><span data-stu-id="c1ce1-118"><dt>**TTDT\_RESHOW**</dt></span></span> </dl>          | <span data-ttu-id="c1ce1-119">Legen Sie die Zeitspanne fest, die benötigt wird, bis nachfolgende QuickInfo-Fenster angezeigt werden, wenn der Zeiger von einem Tool zu einem anderen wechselt.</span><span class="sxs-lookup"><span data-stu-id="c1ce1-119">Set the amount of time it takes for subsequent tooltip windows to appear as the pointer moves from one tool to another.</span></span> <span data-ttu-id="c1ce1-120">Legen Sie *LPARAM* auf-1 fest, um die Zeit zum erneuten Anzeigen der Verzögerung auf den Standardwert zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="c1ce1-120">To return the reshow delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                           |
| <span id="TTDT_AUTOMATIC"></span><span id="ttdt_automatic"></span><dl> <span data-ttu-id="c1ce1-121"><dt>**ttdt \_ automatisch**</dt></span><span class="sxs-lookup"><span data-stu-id="c1ce1-121"><dt>**TTDT\_AUTOMATIC**</dt></span></span> </dl> | <span data-ttu-id="c1ce1-122">Legen Sie alle drei Verzögerungszeiten auf Standard Proportionen fest.</span><span class="sxs-lookup"><span data-stu-id="c1ce1-122">Set all three delay times to default proportions.</span></span> <span data-ttu-id="c1ce1-123">Die autopop-Zeit ist zehnmal so oft wie die Anfangszeit, und die reshow-Zeit ist ein fünftes Mal.</span><span class="sxs-lookup"><span data-stu-id="c1ce1-123">The autopop time will be ten times the initial time and the reshow time will be one fifth the initial time.</span></span> <span data-ttu-id="c1ce1-124">Wenn dieses Flag festgelegt ist, verwenden Sie einen positiven Wert von *LPARAM* , um die anfängliche Zeit in Millisekunden anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c1ce1-124">If this flag is set, use a positive value of *lParam* to specify the initial time, in milliseconds.</span></span> <span data-ttu-id="c1ce1-125">Legen Sie *LPARAM* auf einen negativen Wert fest, um alle drei Verzögerungszeiten auf ihre Standardwerte zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="c1ce1-125">Set *lParam* to a negative value to return all three delay times to their default values.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c1ce1-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1ce1-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1ce1-127">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die Verzögerungszeit in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="c1ce1-127">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the delay time, in milliseconds.</span></span> <span data-ttu-id="c1ce1-128">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="c1ce1-128">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1ce1-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1ce1-129">Return value</span></span>

<span data-ttu-id="c1ce1-130">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c1ce1-130">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1ce1-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1ce1-131">Remarks</span></span>

<span data-ttu-id="c1ce1-132">Die Standard Verzögerungszeiten basieren auf der Doppelklick Zeit.</span><span class="sxs-lookup"><span data-stu-id="c1ce1-132">The default delay times are based on the double-click time.</span></span> <span data-ttu-id="c1ce1-133">Bei der standardmäßigen Doppelklick Zeit von 500 ms beträgt die anfängliche, autopop-und reshow-Verzögerungszeit 500 ms, 5000 ms bzw. 100 ms.</span><span class="sxs-lookup"><span data-stu-id="c1ce1-133">For the default double-click time of 500 ms, the initial, autopop, and reshow delay times are 500ms, 5000ms, and 100ms respectively.</span></span> <span data-ttu-id="c1ce1-134">Im folgenden Code Fragment wird die [**getdoubleclicktime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) -Funktion verwendet, um die drei Verzögerungszeiten für ein beliebiges System festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c1ce1-134">The following code fragment uses the [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) function to determine the three delay times for any system.</span></span>


```
initial = GetDoubleClickTime();

autopop = GetDoubleClickTime() * 10;

reshow = GetDoubleClickTime() / 5;
```



## <a name="requirements"></a><span data-ttu-id="c1ce1-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1ce1-135">Requirements</span></span>



| <span data-ttu-id="c1ce1-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1ce1-136">Requirement</span></span> | <span data-ttu-id="c1ce1-137">Wert</span><span class="sxs-lookup"><span data-stu-id="c1ce1-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1ce1-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1ce1-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c1ce1-139">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1ce1-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c1ce1-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1ce1-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c1ce1-141">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1ce1-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c1ce1-142">Header</span><span class="sxs-lookup"><span data-stu-id="c1ce1-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1ce1-143"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1ce1-143"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1ce1-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1ce1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1ce1-145">**TTM \_ getdelta-Zeit**</span><span class="sxs-lookup"><span data-stu-id="c1ce1-145">**TTM\_GETDELAYTIME**</span></span>](ttm-getdelaytime.md)
</dt> </dl>

 

