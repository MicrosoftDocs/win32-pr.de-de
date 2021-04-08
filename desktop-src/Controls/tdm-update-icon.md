---
title: TDM_UPDATE_ICON Meldung (kommstrg. h)
description: Aktualisiert das Symbol eines Aufgaben Dialogfelds.
ms.assetid: 1094d9ca-90b4-4ba6-a14b-0d4e96243a34
keywords:
- Windows-Steuerelemente für TDM_UPDATE_ICON Meldung
topic_type:
- apiref
api_name:
- TDM_UPDATE_ICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2da73ebb3bf0355f50bc08a08f0b35de97576b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957184"
---
# <a name="tdm_update_icon-message"></a><span data-ttu-id="e71cc-104">Meldung zum TDM- \_ Update \_ Symbol</span><span class="sxs-lookup"><span data-stu-id="e71cc-104">TDM\_UPDATE\_ICON message</span></span>

<span data-ttu-id="e71cc-105">Aktualisiert das Symbol eines Aufgaben Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="e71cc-105">Refreshes the icon of a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="e71cc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e71cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e71cc-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e71cc-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e71cc-108">Gibt an, welches Symbol Element aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e71cc-108">Indicates which icon element to update.</span></span> <span data-ttu-id="e71cc-109">Dieser Parameter muss einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="e71cc-109">This parameter must be one of the following values:</span></span>



| <span data-ttu-id="e71cc-110">Wert</span><span class="sxs-lookup"><span data-stu-id="e71cc-110">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="e71cc-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e71cc-111">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="TDIE_ICON_MAIN"></span><span id="tdie_icon_main"></span><dl> <span data-ttu-id="e71cc-112"><dt>**TDer- \_ Symbol " \_ Main"**</dt></span><span class="sxs-lookup"><span data-stu-id="e71cc-112"><dt>**TDIE\_ICON\_MAIN**</dt></span></span> </dl>       | <span data-ttu-id="e71cc-113">Hauptsymbol.</span><span class="sxs-lookup"><span data-stu-id="e71cc-113">Main icon.</span></span><br/>   |
| <span id="TDIE_ICON_FOOTER"></span><span id="tdie_icon_footer"></span><dl> <span data-ttu-id="e71cc-114"><dt>**TDie- \_ Symbol \_ Fußzeile**</dt></span><span class="sxs-lookup"><span data-stu-id="e71cc-114"><dt>**TDIE\_ICON\_FOOTER**</dt></span></span> </dl> | <span data-ttu-id="e71cc-115">Footersymbol.</span><span class="sxs-lookup"><span data-stu-id="e71cc-115">Footer icon.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e71cc-116">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e71cc-116">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e71cc-117">Ein Zeiger auf eine Zeichenfolge (pcwstr) oder ein Handle für ein Symbol (HICON), das angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e71cc-117">A pointer to a string (PCWSTR) or handle to an icon (HICON) to display.</span></span> <span data-ttu-id="e71cc-118">Wenn *LPARAM* den Wert **null** hat, wird unabhängig vom Wert von *wParam* kein Symbol angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e71cc-118">If *lParam* is **NULL**, no icon is displayed, regardless of the value of *wParam*.</span></span>

<span data-ttu-id="e71cc-119">Wenn der Wert von *wParam* den Wert TDas \_ Symbol \_ Main hat und das TDF- \_ schlüsselflag verwenden für \_ \_ den **dwFlags** -Member der [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) -Struktur, die zum Erstellen des Aufgaben Dialogfelds verwendet wird, festgelegt ist, muss *LPARAM* ein Handle für ein Symbol (HICON) enthalten, das angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e71cc-119">If the value of *wParam* is TDIE\_ICON\_MAIN and the TDF\_USE\_HICON\_MAIN flag is set on the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog, *lParam* must contain a handle to an icon (HICON) to display.</span></span>

<span data-ttu-id="e71cc-120">Wenn der Wert von *wParam* dem TDer \_ \_ -Symbol-Footer entspricht und das Flag für die TDF- \_ \_ Fußzeile verwenden für \_ den **dwFlags** -Member der [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) -Struktur festgelegt ist, die zum Erstellen des Aufgaben Dialogfelds verwendet wird, muss *LPARAM* ein Handle für ein Symbol (HICON) enthalten, das angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e71cc-120">If the value of *wParam* is TDIE\_ICON\_FOOTER and the TDF\_USE\_HICON\_FOOTER flag is set on the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog, *lParam* must contain a handle to an icon (HICON) to display.</span></span>

<span data-ttu-id="e71cc-121">Wenn die TDF \_ " \_ HICON \_ Main" oder "TDF verwenden" \_ verwenden \_ , werden HICON- \_ footerflags **nicht** für den **dwFlags** -Member festgelegt. *LPARAM* muss auf eine mit NULL endende Unicode-Zeichenfolge (pcwstr) verweisen, die einen gültigen Ressourcen Bezeichner enthält, der über das [**makeintresource**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) -Makro übergeben wurde</span><span class="sxs-lookup"><span data-stu-id="e71cc-121">If the TDF\_USE\_HICON\_MAIN or TDF\_USE\_HICON\_FOOTER flags are **not** set on the **dwFlags** member, *lParam* must point to a null-terminated, Unicode string (PCWSTR) that contains a valid resource identifier passed through the [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="e71cc-122">Das Symbol wird basierend auf dem Wert von " *wParam*" angezeigt: Wenn der Wert "TDas \_ Symbol Main" lautet \_ , wird das Symbol in der Kopfzeile angezeigt. wenn der Wert "TDie \_ Icon \_ Footer" ist, wird das Symbol in der Fußzeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e71cc-122">The icon is displayed based on the value of *wParam*: if the value is TDIE\_ICON\_MAIN, the icon is displayed in the header; if the value is TDIE\_ICON\_FOOTER, the icon is displayed in the footer.</span></span> <span data-ttu-id="e71cc-123">Die Ressource muss entweder aus dem Ressourcen Modul der Anwendung (angegeben im **HINSTANCE** -Member der [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) -Struktur) oder, wenn **HINSTANCE** **null** ist, aus dem Ressourcen Modul des Systems (imageres.dll) sein.</span><span class="sxs-lookup"><span data-stu-id="e71cc-123">The resource must be either from the application's resource module (specified in the **hInstance** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure), or if **hInstance** is **NULL**, from the system's resource module (imageres.dll).</span></span> <span data-ttu-id="e71cc-124">Um eine System Ressource zu identifizieren, verwenden Sie einen gültigen System Bezeichner, der über das **makeintresource** -Makro oder einen der folgenden vordefinierten Werte aus "kommctrl. h" übermittelt wird:</span><span class="sxs-lookup"><span data-stu-id="e71cc-124">To identify a system resource, use a valid system identifier passed through the **MAKEINTRESOURCE** macro or one of the following predefined values from commctrl.h:</span></span>



| <span data-ttu-id="e71cc-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e71cc-125">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="e71cc-126">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e71cc-126">Meaning</span></span>                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="TD_ERROR_ICON"></span><span id="td_error_icon"></span><dl> <span data-ttu-id="e71cc-127"><dt>**\_Fehler \_ Symbol für TD**</dt></span><span class="sxs-lookup"><span data-stu-id="e71cc-127"><dt>**TD\_ERROR\_ICON**</dt></span></span> </dl>                   | <span data-ttu-id="e71cc-128">Ein Symbol zum Signieren von Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="e71cc-128">A stop sign icon.</span></span><br/>                        |
| <span id="TD_WARNING_ICON"></span><span id="td_warning_icon"></span><dl> <span data-ttu-id="e71cc-129"><dt>**Symbol für TD- \_ Warnung \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e71cc-129"><dt>**TD\_WARNING\_ICON**</dt></span></span> </dl>             | <span data-ttu-id="e71cc-130">Ein Ausrufezeichen Symbol.</span><span class="sxs-lookup"><span data-stu-id="e71cc-130">An exclamation point icon.</span></span><br/>               |
| <span id="TD_INFORMATION_ICON"></span><span id="td_information_icon"></span><dl> <span data-ttu-id="e71cc-131"><dt>**Symbol für TD- \_ Informationen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e71cc-131"><dt>**TD\_INFORMATION\_ICON**</dt></span></span> </dl> | <span data-ttu-id="e71cc-132">Ein Kleinbuchstabe "i" in einem Kreis Symbol.</span><span class="sxs-lookup"><span data-stu-id="e71cc-132">A lowercase letter "i" in a circle icon.</span></span><br/> |
| <span id="TD_SHIELD_ICON"></span><span id="td_shield_icon"></span><dl> <span data-ttu-id="e71cc-133"><dt>**Symbol für TD- \_ Schild \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e71cc-133"><dt>**TD\_SHIELD\_ICON**</dt></span></span> </dl>                | <span data-ttu-id="e71cc-134">Ein Sicherheitsschild Symbol.</span><span class="sxs-lookup"><span data-stu-id="e71cc-134">A security shield icon.</span></span><br/>                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e71cc-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e71cc-135">Return value</span></span>

<span data-ttu-id="e71cc-136">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e71cc-136">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="e71cc-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e71cc-137">Remarks</span></span>

<span data-ttu-id="e71cc-138">Das Layout des Aufgaben Dialogfelds mit dem Symbol schlägt möglicherweise fehl, und dies wird möglicherweise nicht im Rückgabewert widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="e71cc-138">The layout of the task dialog with the icon may fail and this may not be reflected in the return value.</span></span> <span data-ttu-id="e71cc-139">Der Rückgabewert S \_ OK gibt nur an, dass das Aufgaben Dialogfeld die Nachricht empfangen und versucht hat, Sie zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e71cc-139">A return value of S\_OK reflects only that the task dialog received the message and attempted to process it.</span></span> <span data-ttu-id="e71cc-140">Wenn das Layout des Aufgaben Dialogfelds fehlschlägt, wird das Dialogfeld geschlossen, und ein **HRESULT** -Code wird bei der registrierten Rückruffunktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e71cc-140">If the layout of the task dialog fails, the dialog will close and an **HRESULT** code is returned at the registered callback function.</span></span> <span data-ttu-id="e71cc-141">Weitere Informationen zur Syntax der Rückruffunktion finden Sie unter [*taskdialogcallbackproc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span><span class="sxs-lookup"><span data-stu-id="e71cc-141">For more information on the callback function syntax, see [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span></span>

<span data-ttu-id="e71cc-142">Wenn das Aufgaben Dialogfeld ohne Fußzeile erstellt wird (d. h., die entsprechenden footermember der [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) -Struktur, die zum Erstellen des Aufgaben Dialogfelds verwendet wurden, sind **null**) und diese Nachricht gesendet wird, wird dem Aufgaben Dialogfeld nicht dynamisch eine Fußzeile hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e71cc-142">If the task dialog is created without a footer (that is, the appropriate footer members of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog are **NULL**) and this message is sent, a footer is not dynamically added to the task dialog.</span></span> <span data-ttu-id="e71cc-143">Dasselbe gilt für das Senden dieser Nachricht zum Aktualisieren eines Header Symbols, wenn ein Aufgaben Dialogfeld ohne Header erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e71cc-143">The same is true for sending this message to update a header icon when a task dialog is created without a header.</span></span> <span data-ttu-id="e71cc-144">Um zur Laufzeit eine Kopfzeile oder Fußzeile hinzuzufügen, verwenden Sie die Funktionen der [**TDM- \_ Navigations \_ Seite**](tdm-navigate-page.md) .</span><span class="sxs-lookup"><span data-stu-id="e71cc-144">To add a header or footer at run time, use the [**TDM\_NAVIGATE\_PAGE**](tdm-navigate-page.md) functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="e71cc-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e71cc-145">Requirements</span></span>



| <span data-ttu-id="e71cc-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e71cc-146">Requirement</span></span> | <span data-ttu-id="e71cc-147">Wert</span><span class="sxs-lookup"><span data-stu-id="e71cc-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e71cc-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e71cc-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e71cc-149">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e71cc-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e71cc-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e71cc-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e71cc-151">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e71cc-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e71cc-152">Header</span><span class="sxs-lookup"><span data-stu-id="e71cc-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="e71cc-153"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e71cc-153"><dt>Commctrl.h</dt></span></span> </dl> |



 

