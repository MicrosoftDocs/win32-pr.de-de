---
title: PSM_INSERTPAGE Meldung (prsht. h)
description: Fügt eine neue Seite in ein vorhandenes Eigenschaften Blatt ein. Die Seite kann entweder an einem angegebenen Index oder nach einer angegebenen Seite eingefügt werden. Sie können diese Nachricht explizit oder mithilfe des "propsheet \_ insertpage"-Makros senden.
ms.assetid: 69d55e68-510d-45f1-93d6-ce2bf5dfdb6d
keywords:
- Windows-Steuerelemente für PSM_INSERTPAGE Meldung
topic_type:
- apiref
api_name:
- PSM_INSERTPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afdd58536a5cdd18d39a331df4b18c9bbae93842
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346728"
---
# <a name="psm_insertpage-message"></a><span data-ttu-id="7abc0-106">PSM \_ insertpage-Nachricht</span><span class="sxs-lookup"><span data-stu-id="7abc0-106">PSM\_INSERTPAGE message</span></span>

<span data-ttu-id="7abc0-107">Fügt eine neue Seite in ein vorhandenes Eigenschaften Blatt ein.</span><span class="sxs-lookup"><span data-stu-id="7abc0-107">Inserts a new page into an existing property sheet.</span></span> <span data-ttu-id="7abc0-108">Die Seite kann entweder an einem angegebenen Index oder nach einer angegebenen Seite eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7abc0-108">The page can be inserted either at a specified index or after a specified page.</span></span> <span data-ttu-id="7abc0-109">Sie können diese Nachricht explizit oder mithilfe des " [**propsheet \_ insertpage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) "-Makros senden.</span><span class="sxs-lookup"><span data-stu-id="7abc0-109">You can send this message explicitly or by using the [**PropSheet\_InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7abc0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7abc0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7abc0-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7abc0-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7abc0-112">Der Ort, an dem die Seite eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7abc0-112">Where the page is to be inserted.</span></span> <span data-ttu-id="7abc0-113">Legen Sie diesen Parameter auf **null** fest, um die neue Seite als erste Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7abc0-113">Set this parameter to **NULL** to make the new page the first page.</span></span> <span data-ttu-id="7abc0-114">Um anzugeben, wo die neue Seite eingefügt werden soll, können Sie entweder einen Index oder das hpropsheetpage-Handle einer vorhandenen Seite übergeben.</span><span class="sxs-lookup"><span data-stu-id="7abc0-114">To specify where the new page is to be inserted, you can either pass an index or an existing page's HPROPSHEETPAGE handle.</span></span>



| <span data-ttu-id="7abc0-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7abc0-115">Value</span></span>                                                                                                                                             | <span data-ttu-id="7abc0-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7abc0-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7abc0-117"><dt></dt> <dt>index</dt></span><span class="sxs-lookup"><span data-stu-id="7abc0-117"><dt></dt> <dt>index</dt></span></span> </dl>            | <span data-ttu-id="7abc0-118">Wenn der *wParam* -Parameter kleiner als maxushort (die größte ganze Zahl ohne Vorzeichen) ist, gibt der *wParam* -Parameter den NULL basierten Index für die neue Seite an.</span><span class="sxs-lookup"><span data-stu-id="7abc0-118">If the *wParam* parameter is less than MAXUSHORT (the largest unsigned short integer), the *wParam* specifies the zero-based index for the new page.</span></span> <span data-ttu-id="7abc0-119">Wenn Sie z. b. die eingefügte Seite zur dritten Seite auf dem Eigenschaften Blatt machen möchten, legen Sie *wParam* auf 2 fest.</span><span class="sxs-lookup"><span data-stu-id="7abc0-119">For example, to make the inserted page the third page on the property sheet, set *wParam* to 2.</span></span> <span data-ttu-id="7abc0-120">Legen Sie *wParam* auf 0 fest, um es als erste Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7abc0-120">To make it the first page, set *wParam* to 0.</span></span> <span data-ttu-id="7abc0-121">Wenn für *wParam* ein Wert größer als die Anzahl der Seiten und kleiner als maxushort angegeben ist, wird die Seite angefügt.</span><span class="sxs-lookup"><span data-stu-id="7abc0-121">If *wParam* has a value greater than the number of pages and less than MAXUSHORT, the page will be appended.</span></span><br/> |
| <dl> <span data-ttu-id="7abc0-122"><dt></dt><dt>hpagumsertafter</dt></span><span class="sxs-lookup"><span data-stu-id="7abc0-122"><dt></dt> <dt>hpageInsertAfter</dt></span></span> </dl> | <span data-ttu-id="7abc0-123">Wenn Sie den *wParam* -Parameter auf das hpropsheetpage-Handle einer vorhandenen Seite festlegen, wird die neue Seite eingefügt.</span><span class="sxs-lookup"><span data-stu-id="7abc0-123">If you set the *wParam* parameter to an existing page's HPROPSHEETPAGE handle, the new page will be inserted after it.</span></span><br/>                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="7abc0-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7abc0-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7abc0-125">Handle für die einzufügende Seite.</span><span class="sxs-lookup"><span data-stu-id="7abc0-125">Handle to the page to be inserted.</span></span> <span data-ttu-id="7abc0-126">Die Seite muss zuerst durch einen aufzurufenden Befehl für [**die Funktion "**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) -Funktion" erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7abc0-126">The page must first be created by a call to the [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7abc0-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7abc0-127">Return value</span></span>

<span data-ttu-id="7abc0-128">Gibt einen Wert ungleich 0 (null) zurück, wenn die Seite erfolgreich eingefügt wurde, andernfalls 0 (null).</span><span class="sxs-lookup"><span data-stu-id="7abc0-128">Returns a nonzero value if the page was successfully inserted, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7abc0-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7abc0-129">Remarks</span></span>

<span data-ttu-id="7abc0-130">Die Seiten nach der Einfügemarke werden nach rechts verschoben, um der neuen Seite Rechnung zu tragen.</span><span class="sxs-lookup"><span data-stu-id="7abc0-130">The pages after the insertion point are shifted to the right to accommodate the new page.</span></span>

<span data-ttu-id="7abc0-131">Die Größe des Eigenschaften Blatts wird nicht an die neue Seite angepasst.</span><span class="sxs-lookup"><span data-stu-id="7abc0-131">The property sheet is not resized to fit the new page.</span></span> <span data-ttu-id="7abc0-132">Machen Sie die neue Seite nicht größer als die größte Seite des Eigenschaften Blatts.</span><span class="sxs-lookup"><span data-stu-id="7abc0-132">Do not make the new page larger than the property sheet's largest page.</span></span>

<span data-ttu-id="7abc0-133">Eine Reihe von Nachrichten und ein Funktions aufruftritt auf, während das Eigenschaften Blatt die Liste der Seiten bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="7abc0-133">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="7abc0-134">Während diese Aktion ausgeführt wird, kann der Versuch, die Liste der Seiten zu ändern, zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="7abc0-134">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="7abc0-135">Dementsprechend sollten Sie die PSM \_ insertpage-Nachricht nicht in der Implementierung von [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) oder bei der Behandlung der folgenden Benachrichtigungen und Windows-Meldungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="7abc0-135">Accordingly, you should not use the PSM\_INSERTPAGE message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="7abc0-136">PSN- \_ Anwendung</span><span class="sxs-lookup"><span data-stu-id="7abc0-136">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="7abc0-137">PSN- \_ killactive</span><span class="sxs-lookup"><span data-stu-id="7abc0-137">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="7abc0-138">PSN- \_ zurück Setzung</span><span class="sxs-lookup"><span data-stu-id="7abc0-138">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="7abc0-139">PSN- \_ SETACTIVE</span><span class="sxs-lookup"><span data-stu-id="7abc0-139">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="7abc0-140">**WM \_ zerstören**</span><span class="sxs-lookup"><span data-stu-id="7abc0-140">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="7abc0-141">**WM \_ InitDialog**</span><span class="sxs-lookup"><span data-stu-id="7abc0-141">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="7abc0-142">Wenn Sie eine Eigenschaften Blattseite ändern müssen, während Sie eine dieser Nachrichten verarbeiten, oder wenn [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) in Betrieb ist, stellen Sie selbst eine private Windows-Meldung bereit.</span><span class="sxs-lookup"><span data-stu-id="7abc0-142">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="7abc0-143">Die Anwendung empfängt diese Nachricht erst, nachdem die Aufgaben des Eigenschaften Blatt-Managers beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="7abc0-143">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="7abc0-144">Anschließend können Sie die Seitenliste ändern.</span><span class="sxs-lookup"><span data-stu-id="7abc0-144">Then you can modify the list of pages.</span></span>

<span data-ttu-id="7abc0-145">Die folgenden Benachrichtigungen sind auch von der Änderung von Eigenschaften Seiten betroffen.</span><span class="sxs-lookup"><span data-stu-id="7abc0-145">The following notifications are also affected by property sheet modification.</span></span>

-   [<span data-ttu-id="7abc0-146">PSN- \_ witzback</span><span class="sxs-lookup"><span data-stu-id="7abc0-146">PSN\_WIZBACK</span></span>](psn-wizback.md)
-   [<span data-ttu-id="7abc0-147">PSN- \_ nächstes</span><span class="sxs-lookup"><span data-stu-id="7abc0-147">PSN\_WIZNEXT</span></span>](psn-wiznext.md)

<span data-ttu-id="7abc0-148">Sie können Seiten als Reaktion auf diese Benachrichtigungen hinzufügen oder entfernen, vorausgesetzt, dass Sie (über DWL \_ msgresult) einen Wert ungleich 0 (null) zurückgeben, um die gewünschte neue Seite anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7abc0-148">You can add or remove pages in response to these notifications, provided that you return (via DWL\_MSGRESULT) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="7abc0-149">Beachten Sie jedoch Folgendes: Wenn Sie eine Seite einfügen, die sich vor der aktuellen Seite befindet (die einen kleineren Index als die aktuelle Seite aufweist), wird " [PSN \_ killactive](psn-killactive.md) " möglicherweise an die falsche Seite gesendet.</span><span class="sxs-lookup"><span data-stu-id="7abc0-149">Note, however, that if you insert a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

> [!Note]  
> <span data-ttu-id="7abc0-150">Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7abc0-150">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7abc0-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7abc0-151">Requirements</span></span>



| <span data-ttu-id="7abc0-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7abc0-152">Requirement</span></span> | <span data-ttu-id="7abc0-153">Wert</span><span class="sxs-lookup"><span data-stu-id="7abc0-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7abc0-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7abc0-154">Minimum supported client</span></span><br/> | <span data-ttu-id="7abc0-155">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7abc0-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7abc0-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7abc0-156">Minimum supported server</span></span><br/> | <span data-ttu-id="7abc0-157">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7abc0-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7abc0-158">Header</span><span class="sxs-lookup"><span data-stu-id="7abc0-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="7abc0-159"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="7abc0-159"><dt>Prsht.h</dt></span></span> </dl> |



 

