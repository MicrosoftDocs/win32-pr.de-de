---
title: DTN_CLOSEUP Benachrichtigungs Code (kommctrl. h)
description: Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) gesendet, wenn der Benutzer den Dropdown-Monatskalender schließt.
ms.assetid: 94ace714-55cc-4c59-8b87-8d0348b15f34
keywords:
- Windows-Steuerelemente für DTN_CLOSEUP Benachrichtigungs
topic_type:
- apiref
api_name:
- DTN_CLOSEUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cfcfb23215aeffe15bec576075fd4d930790e47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742832"
---
# <a name="dtn_closeup-notification-code"></a><span data-ttu-id="edace-104">DTN- \_ closeup-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="edace-104">DTN\_CLOSEUP notification code</span></span>

<span data-ttu-id="edace-105">Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) gesendet, wenn der Benutzer den Dropdown-Monatskalender schließt.</span><span class="sxs-lookup"><span data-stu-id="edace-105">Sent by a date and time picker (DTP) control when the user closes the drop-down month calendar.</span></span> <span data-ttu-id="edace-106">Der Monatskalender wird geschlossen, wenn der Benutzer ein Datum aus dem Monatskalender auswählt oder auf den Dropdown Pfeil klickt, während der Kalender geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="edace-106">The month calendar is closed when the user chooses a date from the month calendar or clicks the drop-down arrow while the calendar is open.</span></span> <span data-ttu-id="edace-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="edace-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_CLOSEUP

    lpNmhdr = (LPMNHDR)lParam;
```



## <a name="parameters"></a><span data-ttu-id="edace-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="edace-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edace-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="edace-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="edace-110">Ein Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die Informationen zur Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="edace-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edace-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="edace-111">Return value</span></span>

<span data-ttu-id="edace-112">Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="edace-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="edace-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="edace-113">Remarks</span></span>

<span data-ttu-id="edace-114">DTP-Steuerelemente behalten kein statisches Steuerelement für untergeordnete Monatskalender bei.</span><span class="sxs-lookup"><span data-stu-id="edace-114">DTP controls do not maintain a static child month calendar control.</span></span> <span data-ttu-id="edace-115">Das DTP-Steuerelement zerstört das Kalender Steuerelement des untergeordneten Monats vor dem Senden dieses Benachrichtigungs Codes.</span><span class="sxs-lookup"><span data-stu-id="edace-115">The DTP control destroys the child month calendar control prior to sending this notification code.</span></span> <span data-ttu-id="edace-116">Daher darf Ihre Anwendung nicht auf ein statisches Fenster Handle für den untergeordneten Monatskalender des Steuer Elements zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="edace-116">So your application must not rely on a static window handle to the control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="edace-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="edace-117">Requirements</span></span>



| <span data-ttu-id="edace-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="edace-118">Requirement</span></span> | <span data-ttu-id="edace-119">Wert</span><span class="sxs-lookup"><span data-stu-id="edace-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="edace-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="edace-120">Minimum supported client</span></span><br/> | <span data-ttu-id="edace-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="edace-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="edace-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="edace-122">Minimum supported server</span></span><br/> | <span data-ttu-id="edace-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="edace-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="edace-124">Header</span><span class="sxs-lookup"><span data-stu-id="edace-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="edace-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="edace-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edace-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edace-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="edace-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="edace-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="edace-128">DTN- \_ Dropdown</span><span class="sxs-lookup"><span data-stu-id="edace-128">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="edace-129">**DTM \_ getmonthcal**</span><span class="sxs-lookup"><span data-stu-id="edace-129">**DTM\_GETMONTHCAL**</span></span>](dtm-getmonthcal.md)
</dt> </dl>

 

 





