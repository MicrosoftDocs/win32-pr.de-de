---
title: DTN_DROPDOWN Benachrichtigungs Code (kommctrl. h)
description: Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) gesendet, wenn der Benutzer den Dropdown-Monatskalender aktiviert. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 6f20fa87-2223-4876-b77d-2c684685bf10
keywords:
- Windows-Steuerelemente für DTN_DROPDOWN Benachrichtigungs
topic_type:
- apiref
api_name:
- DTN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101a25a8e2da09b9f4065a54fcff9896690adbb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859076"
---
# <a name="dtn_dropdown-notification-code"></a><span data-ttu-id="9e5b5-105">DTN- \_ Dropdown-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="9e5b5-105">DTN\_DROPDOWN notification code</span></span>

<span data-ttu-id="9e5b5-106">Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) gesendet, wenn der Benutzer den Dropdown-Monatskalender aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9e5b5-106">Sent by a date and time picker (DTP) control when the user activates the drop-down month calendar.</span></span> <span data-ttu-id="9e5b5-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="9e5b5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_DROPDOWN

    lpNmhdr = (LPNMHDR)lParam;
```



## <a name="parameters"></a><span data-ttu-id="9e5b5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e5b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e5b5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e5b5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e5b5-110">Ein Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die Informationen zur Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="9e5b5-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e5b5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e5b5-111">Return value</span></span>

<span data-ttu-id="9e5b5-112">Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e5b5-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e5b5-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e5b5-113">Remarks</span></span>

<span data-ttu-id="9e5b5-114">Eine Aufgabe, die der Benachrichtigungs Handler ausführen muss, besteht darin, das Dropdown-Monatskalender-Steuerelement anzupassen.</span><span class="sxs-lookup"><span data-stu-id="9e5b5-114">One task that your notification handler may need to perform is to customize the dropdown month-calendar control.</span></span> <span data-ttu-id="9e5b5-115">Wenn Sie beispielsweise "Gehe zu heute" nicht möchten, müssen Sie den [**MCS- \_ notoday**](month-calendar-control-styles.md)  -Stil des Steuer Elements festlegen.</span><span class="sxs-lookup"><span data-stu-id="9e5b5-115">For instance, if you do not want "Go To Today," you need to set the control's [**MCS\_NOTODAY**](month-calendar-control-styles.md)  style.</span></span> <span data-ttu-id="9e5b5-116">Um ein Handle für das Month-Calendar-Steuerelement abzurufen, senden Sie dem DTP-Steuerelement eine [**DTM \_ getmonthcal**](dtm-getmonthcal.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9e5b5-116">To retrieve a handle to the month-calendar control, send the DTP control a [**DTM\_GETMONTHCAL**](dtm-getmonthcal.md) message.</span></span> <span data-ttu-id="9e5b5-117">Anschließend können Sie dieses Handle und [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) verwenden, um den gewünschten Monat Kalender Stil festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9e5b5-117">You can then use this handle and [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) to set the desired month-calendar style.</span></span>

<span data-ttu-id="9e5b5-118">DTP-Steuerelemente behalten kein statisches Steuerelement für untergeordnete Monatskalender bei.</span><span class="sxs-lookup"><span data-stu-id="9e5b5-118">DTP controls do not maintain a static child month calendar control.</span></span> <span data-ttu-id="9e5b5-119">Das DTP-Steuerelement erstellt vor dem Senden dieses Benachrichtigungs Codes ein neues Monatskalender-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="9e5b5-119">The DTP control creates a new month calendar control before sending this notification code.</span></span> <span data-ttu-id="9e5b5-120">Darüber hinaus zerstört das DTP-Steuerelement das untergeordnete Steuerelement, wenn es nicht aktiv ist (sichtbar).</span><span class="sxs-lookup"><span data-stu-id="9e5b5-120">Additionally, the DTP control destroys the child control when it is not active (visible).</span></span> <span data-ttu-id="9e5b5-121">Daher darf Ihre Anwendung nicht auf ein statisches Fenster Handle für den untergeordneten Monatskalender des Steuer Elements zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="9e5b5-121">So your application must not rely on a static window handle to the control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e5b5-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e5b5-122">Requirements</span></span>



| <span data-ttu-id="9e5b5-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e5b5-123">Requirement</span></span> | <span data-ttu-id="9e5b5-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9e5b5-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e5b5-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e5b5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9e5b5-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e5b5-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e5b5-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e5b5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9e5b5-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e5b5-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e5b5-129">Header</span><span class="sxs-lookup"><span data-stu-id="9e5b5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e5b5-130"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e5b5-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e5b5-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e5b5-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="9e5b5-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9e5b5-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9e5b5-133">DTN- \_ Schließung</span><span class="sxs-lookup"><span data-stu-id="9e5b5-133">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> <dt>

[<span data-ttu-id="9e5b5-134">**DTM \_ getmonthcal**</span><span class="sxs-lookup"><span data-stu-id="9e5b5-134">**DTM\_GETMONTHCAL**</span></span>](dtm-getmonthcal.md)
</dt> </dl>

 

