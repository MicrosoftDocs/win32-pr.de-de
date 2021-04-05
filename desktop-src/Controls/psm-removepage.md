---
title: PSM_REMOVEPAGE Meldung (prsht. h)
description: Entfernt eine Seite aus einem Eigenschaftenblatt. Sie können diese Nachricht explizit oder mithilfe des propsheet- \_ RemovePage-Makros senden.
ms.assetid: 2f387e97-4db4-4ad5-8600-7325da674e33
keywords:
- Windows-Steuerelemente für PSM_REMOVEPAGE Meldung
topic_type:
- apiref
api_name:
- PSM_REMOVEPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cae1611e1ed9540fce23d20681f44849903e5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859120"
---
# <a name="psm_removepage-message"></a><span data-ttu-id="e9412-105">PSM- \_ RemovePage-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e9412-105">PSM\_REMOVEPAGE message</span></span>

<span data-ttu-id="e9412-106">Entfernt eine Seite aus einem Eigenschaftenblatt.</span><span class="sxs-lookup"><span data-stu-id="e9412-106">Removes a page from a property sheet.</span></span> <span data-ttu-id="e9412-107">Sie können diese Nachricht explizit oder mithilfe des [**propsheet- \_ RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="e9412-107">You can send this message explicitly or by using the [**PropSheet\_RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e9412-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9412-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9412-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9412-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9412-110">Der null basierte Index der zu entfernenden Seite.</span><span class="sxs-lookup"><span data-stu-id="e9412-110">Zero-based index of the page to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="e9412-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9412-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9412-112">Das hpropsheetpage-Handle der zu entfernenden Seite.</span><span class="sxs-lookup"><span data-stu-id="e9412-112">The HPROPSHEETPAGE handle of the page to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9412-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9412-113">Return value</span></span>

<span data-ttu-id="e9412-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="e9412-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9412-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9412-115">Remarks</span></span>

<span data-ttu-id="e9412-116">Eine Anwendung kann den Index oder das Handle oder beides angeben.</span><span class="sxs-lookup"><span data-stu-id="e9412-116">An application can specify the index or the handle, or both.</span></span> <span data-ttu-id="e9412-117">Wenn beide angegeben sind, hat *LPARAM* Vorrang.</span><span class="sxs-lookup"><span data-stu-id="e9412-117">If both are specified, *lParam* takes precedence.</span></span>

<span data-ttu-id="e9412-118">Beim Senden von **PSM \_ RemovePage** wird die zu entfernende Eigenschaften Blattseite zerstört.</span><span class="sxs-lookup"><span data-stu-id="e9412-118">Sending **PSM\_REMOVEPAGE** destroys the property sheet page that is being removed.</span></span>

<span data-ttu-id="e9412-119">Eine Reihe von Nachrichten und ein Funktions aufruftritt auf, während das Eigenschaften Blatt die Liste der Seiten bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="e9412-119">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="e9412-120">Während diese Aktion ausgeführt wird, kann der Versuch, die Liste der Seiten zu ändern, zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="e9412-120">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="e9412-121">Dementsprechend sollten Sie die **PSM- \_ RemovePage** -Nachricht nicht in der Implementierung von [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) oder bei der Behandlung der folgenden Benachrichtigungen und Windows-Meldungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9412-121">Accordingly, you should not use the **PSM\_REMOVEPAGE** message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="e9412-122">PSN- \_ Anwendung</span><span class="sxs-lookup"><span data-stu-id="e9412-122">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="e9412-123">PSN- \_ killactive</span><span class="sxs-lookup"><span data-stu-id="e9412-123">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="e9412-124">PSN- \_ zurück Setzung</span><span class="sxs-lookup"><span data-stu-id="e9412-124">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="e9412-125">PSN- \_ SETACTIVE</span><span class="sxs-lookup"><span data-stu-id="e9412-125">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="e9412-126">**WM \_ zerstören**</span><span class="sxs-lookup"><span data-stu-id="e9412-126">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="e9412-127">**WM \_ InitDialog**</span><span class="sxs-lookup"><span data-stu-id="e9412-127">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="e9412-128">Wenn Sie eine Eigenschaften Blattseite ändern müssen, während Sie eine dieser Nachrichten verarbeiten, oder wenn [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) in Betrieb ist, stellen Sie selbst eine private Windows-Meldung bereit.</span><span class="sxs-lookup"><span data-stu-id="e9412-128">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="e9412-129">Die Anwendung empfängt diese Nachricht erst, nachdem die Aufgaben des Eigenschaften Blatt-Managers beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="e9412-129">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="e9412-130">Anschließend können Sie die Seitenliste ändern.</span><span class="sxs-lookup"><span data-stu-id="e9412-130">Then you can modify the list of pages.</span></span>

<span data-ttu-id="e9412-131">Die folgenden Benachrichtigungen sind auch von der Änderung von Eigenschaften Seiten betroffen.</span><span class="sxs-lookup"><span data-stu-id="e9412-131">The following notifications are also affected by property sheet modification.</span></span>

-   [<span data-ttu-id="e9412-132">PSN- \_ witzback</span><span class="sxs-lookup"><span data-stu-id="e9412-132">PSN\_WIZBACK</span></span>](psn-wizback.md)
-   [<span data-ttu-id="e9412-133">PSN- \_ nächstes</span><span class="sxs-lookup"><span data-stu-id="e9412-133">PSN\_WIZNEXT</span></span>](psn-wiznext.md)

<span data-ttu-id="e9412-134">Sie können Seiten als Reaktion auf diese Benachrichtigungen hinzufügen oder entfernen, vorausgesetzt, dass Sie (über DWL \_ msgresult) einen Wert ungleich 0 (null) zurückgeben, um die gewünschte neue Seite anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e9412-134">You can add or remove pages in response to these notifications, provided that you return (via DWL\_MSGRESULT) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="e9412-135">Beachten Sie jedoch Folgendes: Wenn Sie eine Seite entfernen, die sich vor der aktuellen Seite befindet (die einen kleineren Index als die aktuelle Seite aufweist), wird " [PSN \_ killactive](psn-killactive.md) " möglicherweise an die falsche Seite gesendet.</span><span class="sxs-lookup"><span data-stu-id="e9412-135">Note, however, that if you remove a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9412-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9412-136">Requirements</span></span>



| <span data-ttu-id="e9412-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9412-137">Requirement</span></span> | <span data-ttu-id="e9412-138">Wert</span><span class="sxs-lookup"><span data-stu-id="e9412-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e9412-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9412-139">Minimum supported client</span></span><br/> | <span data-ttu-id="e9412-140">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9412-140">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e9412-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9412-141">Minimum supported server</span></span><br/> | <span data-ttu-id="e9412-142">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9412-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e9412-143">Header</span><span class="sxs-lookup"><span data-stu-id="e9412-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9412-144"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9412-144"><dt>Prsht.h</dt></span></span> </dl> |



 

