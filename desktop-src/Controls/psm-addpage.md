---
title: PSM_ADDPAGE Meldung (prsht. h)
description: Fügt am Ende eines vorhandenen Eigenschaften Blatts eine neue Seite hinzu. Sie können diese Nachricht explizit oder mithilfe des propsheet- \_ addPage-Makros senden.
ms.assetid: 41f9a09e-6de6-466b-bdfa-c8c4e8f193e4
keywords:
- Windows-Steuerelemente für PSM_ADDPAGE Meldung
topic_type:
- apiref
api_name:
- PSM_ADDPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4d09e07dfa2be86e11fa33863f091732955714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859123"
---
# <a name="psm_addpage-message"></a><span data-ttu-id="e3a5e-105">PSM \_ addPage-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e3a5e-105">PSM\_ADDPAGE message</span></span>

<span data-ttu-id="e3a5e-106">Fügt am Ende eines vorhandenen Eigenschaften Blatts eine neue Seite hinzu.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-106">Adds a new page to the end of an existing property sheet.</span></span> <span data-ttu-id="e3a5e-107">Sie können diese Nachricht explizit oder mithilfe des [**propsheet- \_ addPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-107">You can send this message explicitly or by using the [**PropSheet\_AddPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e3a5e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3a5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3a5e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e3a5e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3a5e-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e3a5e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3a5e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3a5e-112">Handle für die hinzu zufügende Seite.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-112">Handle to the page to add.</span></span> <span data-ttu-id="e3a5e-113">Die Seite muss durch einen vorherigen Aufrufen der Funktion "-Funktion" von "| [**atepropertysheetpage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) " erstellt worden sein.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-113">The page must have been created by a previous call to the [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3a5e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3a5e-114">Return value</span></span>

<span data-ttu-id="e3a5e-115">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="e3a5e-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3a5e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3a5e-116">Remarks</span></span>

<span data-ttu-id="e3a5e-117">Die neue Seite sollte nicht größer als die größte Seite sein, die sich derzeit im Eigenschaften Blatt befindet, da die Größe des Eigenschaften Blatts nicht an die neue Seite angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-117">The new page should be no larger than the largest page currently in the property sheet because the property sheet is not resized to fit the new page.</span></span>

<span data-ttu-id="e3a5e-118">Eine Reihe von Nachrichten und ein Funktions aufruftritt auf, während das Eigenschaften Blatt die Liste der Seiten bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-118">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="e3a5e-119">Während diese Aktion ausgeführt wird, kann der Versuch, die Liste der Seiten zu ändern, zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-119">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="e3a5e-120">Dementsprechend sollten Sie die PSM \_ -addPage-Nachricht nicht in der Implementierung von [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) oder bei der Behandlung der folgenden Benachrichtigungen und Windows-Meldungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-120">Accordingly, you should not use the PSM\_ADDPAGE message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="e3a5e-121">PSN- \_ Anwendung</span><span class="sxs-lookup"><span data-stu-id="e3a5e-121">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="e3a5e-122">PSN- \_ killactive</span><span class="sxs-lookup"><span data-stu-id="e3a5e-122">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="e3a5e-123">PSN- \_ zurück Setzung</span><span class="sxs-lookup"><span data-stu-id="e3a5e-123">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="e3a5e-124">PSN- \_ SETACTIVE</span><span class="sxs-lookup"><span data-stu-id="e3a5e-124">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="e3a5e-125">**WM \_ zerstören**</span><span class="sxs-lookup"><span data-stu-id="e3a5e-125">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="e3a5e-126">**WM \_ InitDialog**</span><span class="sxs-lookup"><span data-stu-id="e3a5e-126">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="e3a5e-127">Wenn Sie eine Eigenschaften Blattseite ändern müssen, während Sie eine dieser Nachrichten verarbeiten, oder wenn [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) in Betrieb ist, stellen Sie selbst eine private Windows-Meldung bereit.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-127">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="e3a5e-128">Die Anwendung empfängt diese Nachricht erst, nachdem die Aufgaben des Eigenschaften Blatt-Managers beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-128">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="e3a5e-129">Anschließend können Sie die Seitenliste ändern.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-129">Then you can modify the list of pages.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a5e-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3a5e-130">Requirements</span></span>



| <span data-ttu-id="e3a5e-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3a5e-131">Requirement</span></span> | <span data-ttu-id="e3a5e-132">Wert</span><span class="sxs-lookup"><span data-stu-id="e3a5e-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a5e-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3a5e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e3a5e-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3a5e-134">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e3a5e-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3a5e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e3a5e-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3a5e-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e3a5e-137">Header</span><span class="sxs-lookup"><span data-stu-id="e3a5e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3a5e-138"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3a5e-138"><dt>Prsht.h</dt></span></span> </dl> |



 

