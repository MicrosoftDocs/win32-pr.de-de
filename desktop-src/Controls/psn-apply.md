---
title: PSN_APPLY Benachrichtigungs Code (prsht. h)
description: Wird an jede Seite im Eigenschaften Blatt gesendet, um anzugeben, dass der Benutzer auf die Schaltfläche "OK", "Schließen" oder "übernehmen" geklickt hat und alle Änderungen wirksam werden sollen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 18da6bdb-9409-49b6-8116-580fedd99a02
keywords:
- Windows-Steuerelemente für PSN_APPLY Benachrichtigungs
topic_type:
- apiref
api_name:
- PSN_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d8206b4e423fb01be3277a9dd0ca3a49b59129
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477547"
---
# <a name="psn_apply-notification-code"></a><span data-ttu-id="d2599-105">\_Benachrichtigungs Code für PSN-Anwendung</span><span class="sxs-lookup"><span data-stu-id="d2599-105">PSN\_APPLY notification code</span></span>

<span data-ttu-id="d2599-106">Wird an jede Seite im Eigenschaften Blatt gesendet, um anzugeben, dass der Benutzer auf die Schaltfläche "OK", "Schließen" oder "übernehmen" geklickt hat und alle Änderungen wirksam werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d2599-106">Sent to every page in the property sheet to indicate that the user has clicked the OK, Close, or Apply button and wants all changes to take effect.</span></span> <span data-ttu-id="d2599-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="d2599-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_APPLY 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d2599-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2599-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2599-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2599-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2599-110">Ein Zeiger auf eine [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, die Informationen über den Benachrichtigungs Code einschließlich der ID der Seite enthält.</span><span class="sxs-lookup"><span data-stu-id="d2599-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code, including the ID of the page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2599-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2599-111">Return value</span></span>

<span data-ttu-id="d2599-112">Legen Sie psnret \_ noError fest, um anzugeben, dass die an dieser Seite vorgenommenen Änderungen gültig sind und angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="d2599-112">Set PSNRET\_NOERROR to indicate that the changes made to this page are valid and have been applied.</span></span> <span data-ttu-id="d2599-113">Wenn alle Seiten psnret \_ noError festlegen, kann das Eigenschaften Blatt zerstört werden.</span><span class="sxs-lookup"><span data-stu-id="d2599-113">If all pages set PSNRET\_NOERROR, the property sheet can be destroyed.</span></span> <span data-ttu-id="d2599-114">Um anzugeben, dass die an dieser Seite vorgenommenen Änderungen ungültig sind, und um zu verhindern, dass das Eigenschaften Blatt zerstört wird, legen Sie einen der folgenden Rückgabewerte fest:</span><span class="sxs-lookup"><span data-stu-id="d2599-114">To indicate that the changes made to this page are invalid and to prevent the property sheet from being destroyed, set one of the following return values:</span></span>

-   <span data-ttu-id="d2599-115">psnret ist \_ ungültig.</span><span class="sxs-lookup"><span data-stu-id="d2599-115">PSNRET\_INVALID.</span></span> <span data-ttu-id="d2599-116">Das Eigenschaften Blatt wird nicht zerstört, und der Fokus wird auf diese Seite zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d2599-116">The property sheet will not be destroyed, and focus will be returned to this page.</span></span>
-   <span data-ttu-id="d2599-117">psnret \_ ungültige \_ nochangepage.</span><span class="sxs-lookup"><span data-stu-id="d2599-117">PSNRET\_INVALID\_NOCHANGEPAGE.</span></span> <span data-ttu-id="d2599-118">Das Eigenschaften Blatt wird nicht zerstört, und der Fokus wird auf die Seite zurückgegeben, die den Fokus hatte, als die Schaltfläche gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="d2599-118">The property sheet will not be destroyed, and focus will be returned to the page that had focus when the button was pressed.</span></span>

<span data-ttu-id="d2599-119">Um den Rückgabewert festzulegen, muss die Dialogfeld Prozedur für die Seite die Funktion [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) mit dem DWL \_ -Wert msgresult aufrufen, und die Dialogfeld Prozedur muss **true** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d2599-119">To set the return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2599-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2599-120">Remarks</span></span>

<span data-ttu-id="d2599-121">Wenn der Benutzer auf die Schaltfläche OK, übernehmen oder schließen klickt, sendet das Eigenschaften Blatt eine [PSN- \_ killactive](psn-killactive.md) -Benachrichtigung an die aktive Seite und gibt dadurch die Möglichkeit, die Änderungen des Benutzers zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d2599-121">When the user clicks the OK, Apply, or Close button, the property sheet sends a [PSN\_KILLACTIVE](psn-killactive.md) notification to the active page, giving it an opportunity to validate the user's changes.</span></span> <span data-ttu-id="d2599-122">Wenn die Änderungen gültig sind, sendet das Eigenschaften Blatt einen "PSN Apply"- \_ Benachrichtigungs Code auf jede Seite und leitet ihn so um, dass die neuen Eigenschaften auf das entsprechende Element angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d2599-122">If the changes are valid, the property sheet sends a PSN\_APPLY notification code to each page, directing it to apply the new properties to the corresponding item.</span></span>

> [!Note]  
> <span data-ttu-id="d2599-123">Das Eigenschaften Blatt bearbeitet die Liste der Seiten, wenn der \_ Benachrichtigungs Code "PSN Apply" gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="d2599-123">The property sheet is in the process of manipulating the list of pages when the PSN\_APPLY notification code is sent.</span></span> <span data-ttu-id="d2599-124">Versuchen Sie nicht, Seiten hinzuzufügen, zu entfernen oder einzufügen, während Sie diese Benachrichtigung verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d2599-124">Do not attempt to add, remove, or insert pages while handling this notification.</span></span> <span data-ttu-id="d2599-125">Dies führt zu unvorhersehbaren Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="d2599-125">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="d2599-126">Der **LPARAM** -Member der [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, auf die von *LPARAM* verwiesen wird, ist auf **true** festgelegt, wenn der Benutzer auf die Schaltfläche OK klickt.</span><span class="sxs-lookup"><span data-stu-id="d2599-126">The **lParam** member of the [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure pointed to by *lParam* is set to **TRUE** if the user clicks the OK button.</span></span> <span data-ttu-id="d2599-127">Sie wird auch auf " **true** " festgelegt, wenn die [**PSM \_ canceldeclose**](psm-canceltoclose.md) -Nachricht gesendet wurde und der Benutzer auf die Schaltfläche "Schließen" klickt.</span><span class="sxs-lookup"><span data-stu-id="d2599-127">It is also set to **TRUE** if the [**PSM\_CANCELTOCLOSE**](psm-canceltoclose.md) message has been sent and the user clicks the Close button.</span></span> <span data-ttu-id="d2599-128">Der Wert ist auf **false** festgelegt, wenn der Benutzer auf die Schaltfläche übernehmen klickt.</span><span class="sxs-lookup"><span data-stu-id="d2599-128">It is set to **FALSE** if the user clicks the Apply button.</span></span>

<span data-ttu-id="d2599-129">Die [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur als ersten Member, **HDR**. Der **hwndfrom** -Member dieser **NMHDR** -Struktur enthält das Handle für das Eigenschaften Blatt.</span><span class="sxs-lookup"><span data-stu-id="d2599-129">The [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

<span data-ttu-id="d2599-130">Beim Verarbeiten dieses Benachrichtigungs Codes dürfen Sie die [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) -Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d2599-130">Do not call the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function when processing this notification code.</span></span>

<span data-ttu-id="d2599-131">Ein modales Eigenschaften Blatt wird zerstört, wenn der Benutzer auf die Schaltfläche OK klickt und jede Seite den Wert psnret \_ noError als Antwort auf **PSN \_ Apply** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d2599-131">A modal property sheet is destroyed if the user clicks the OK button and every page returns the PSNRET\_NOERROR value in response to **PSN\_APPLY**.</span></span> <span data-ttu-id="d2599-132">Wenn eine Seite "psnret \_ invalid" oder "psnret \_ ungültige \_ nochangepage" zurückgibt, wird der Apply-Prozess sofort abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="d2599-132">If any page returns PSNRET\_INVALID or PSNRET\_INVALID\_NOCHANGEPAGE, the Apply process is canceled immediately.</span></span> <span data-ttu-id="d2599-133">Seiten, die auf der Abbruch Seite stehen, erhalten keinen PSN- \_ Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="d2599-133">Pages after the cancelling page will not receive a PSN\_APPLY notification code.</span></span>

<span data-ttu-id="d2599-134">Um diesen Benachrichtigungs Code zu erhalten, muss eine Seite den DWL- \_ msgresult-Wert als Antwort auf den Benachrichtigungs Code " [PSN \_ killactive](psn-killactive.md) " auf " **false** " festlegen.</span><span class="sxs-lookup"><span data-stu-id="d2599-134">To receive this notification code, a page must set the DWL\_MSGRESULT value to **FALSE** in response to the [PSN\_KILLACTIVE](psn-killactive.md) notification code.</span></span>

> [!Note]  
> <span data-ttu-id="d2599-135">Dieser Benachrichtigungs Code wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d2599-135">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d2599-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2599-136">Requirements</span></span>



| <span data-ttu-id="d2599-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2599-137">Requirement</span></span> | <span data-ttu-id="d2599-138">Wert</span><span class="sxs-lookup"><span data-stu-id="d2599-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d2599-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2599-139">Minimum supported client</span></span><br/> | <span data-ttu-id="d2599-140">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2599-140">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d2599-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2599-141">Minimum supported server</span></span><br/> | <span data-ttu-id="d2599-142">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2599-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d2599-143">Header</span><span class="sxs-lookup"><span data-stu-id="d2599-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2599-144"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2599-144"><dt>Prsht.h</dt></span></span> </dl> |



 

