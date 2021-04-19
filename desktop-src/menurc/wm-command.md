---
title: WM_COMMAND Meldung (Winuser. h)
description: Wird gesendet, wenn der Benutzer ein Befehls Element aus einem Menü auswählt, wenn ein Steuerelement eine Benachrichtigungs Meldung an das übergeordnete Fenster sendet oder wenn eine Tastenkombination für die Zugriffstaste übersetzt wird.
ms.assetid: 5516098e-fd90-49c8-afb0-78164b028376
keywords:
- WM_COMMAND von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_COMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 1826c4668f3be8a2991c914e60320b55de867e33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369158"
---
# <a name="wm_command-message"></a><span data-ttu-id="2a490-104">WM- \_ Befehls Meldung</span><span class="sxs-lookup"><span data-stu-id="2a490-104">WM\_COMMAND message</span></span>

<span data-ttu-id="2a490-105">Wird gesendet, wenn der Benutzer ein Befehls Element aus einem Menü auswählt, wenn ein Steuerelement eine Benachrichtigungs Meldung an das übergeordnete Fenster sendet oder wenn eine Tastenkombination für die Zugriffstaste übersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="2a490-105">Sent when the user selects a command item from a menu, when a control sends a notification message to its parent window, or when an accelerator keystroke is translated.</span></span>


```C++
#define WM_COMMAND                      0x0111
```



## <a name="parameters"></a><span data-ttu-id="2a490-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a490-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a490-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a490-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a490-108">Eine Beschreibung dieses Parameters finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="2a490-108">For a description of this parameter, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2a490-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a490-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a490-110">Eine Beschreibung dieses Parameters finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="2a490-110">For a description of this parameter, see Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a490-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a490-111">Return value</span></span>

<span data-ttu-id="2a490-112">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2a490-112">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="2a490-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2a490-113">Example</span></span>

```c
BOOL AboutDlg (
    HWND hDlg, 
    UINT message, 
    WPARAM wParam, 
    LPARAM lParam)
{
    BOOL bRet = FALSE;
    
    switch (message) 
    {
        case WM_INITDIALOG:
            bRet = TRUE;
            break;

        case WM_COMMAND:
            if (wParam == IDOK ||
                wParam == IDCANCEL) 
            {
                EndDialog(hDlg, TRUE);
                bRet = TRUE;
            }
            break;
    }

    return bRet;
}
```
<span data-ttu-id="2a490-114">Beispiel für [klassische Windows-Beispiele](https://github.com/microsoft/Windows-classic-samples) auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="2a490-114">Example taken from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>


## <a name="remarks"></a><span data-ttu-id="2a490-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a490-115">Remarks</span></span>

<span data-ttu-id="2a490-116">Die Verwendung der Parameter *wParam* und *LPARAM* wird hier zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="2a490-116">Use of the *wParam* and *lParam* parameters are summarized here.</span></span>



| <span data-ttu-id="2a490-117">Nachrichtenquelle</span><span class="sxs-lookup"><span data-stu-id="2a490-117">Message Source</span></span> | <span data-ttu-id="2a490-118">wParam (hohes Wort)</span><span class="sxs-lookup"><span data-stu-id="2a490-118">wParam (high word)</span></span>                | <span data-ttu-id="2a490-119">wParam (niedriges Wort)</span><span class="sxs-lookup"><span data-stu-id="2a490-119">wParam (low word)</span></span>                | <span data-ttu-id="2a490-120">lParam</span><span class="sxs-lookup"><span data-stu-id="2a490-120">lParam</span></span>                       |
|----------------|-----------------------------------|----------------------------------|------------------------------|
| <span data-ttu-id="2a490-121">Menü</span><span class="sxs-lookup"><span data-stu-id="2a490-121">Menu</span></span>           | <span data-ttu-id="2a490-122">0</span><span class="sxs-lookup"><span data-stu-id="2a490-122">0</span></span>                                 | <span data-ttu-id="2a490-123">Menü Bezeichner (IDM \_ \* )</span><span class="sxs-lookup"><span data-stu-id="2a490-123">Menu identifier (IDM\_\*)</span></span>        | <span data-ttu-id="2a490-124">0</span><span class="sxs-lookup"><span data-stu-id="2a490-124">0</span></span>                            |
| <span data-ttu-id="2a490-125">Accelerator</span><span class="sxs-lookup"><span data-stu-id="2a490-125">Accelerator</span></span>    | <span data-ttu-id="2a490-126">1</span><span class="sxs-lookup"><span data-stu-id="2a490-126">1</span></span>                                 | <span data-ttu-id="2a490-127">Zugriffstasten-ID (IDM \_ \* )</span><span class="sxs-lookup"><span data-stu-id="2a490-127">Accelerator identifier (IDM\_\*)</span></span> | <span data-ttu-id="2a490-128">0</span><span class="sxs-lookup"><span data-stu-id="2a490-128">0</span></span>                            |
| <span data-ttu-id="2a490-129">Control</span><span class="sxs-lookup"><span data-stu-id="2a490-129">Control</span></span>        | <span data-ttu-id="2a490-130">Steuerelement definierter Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="2a490-130">Control-defined notification code</span></span> | <span data-ttu-id="2a490-131">Steuerelement Bezeichner</span><span class="sxs-lookup"><span data-stu-id="2a490-131">Control identifier</span></span>               | <span data-ttu-id="2a490-132">Handle für das Steuerelement Fenster</span><span class="sxs-lookup"><span data-stu-id="2a490-132">Handle to the control window</span></span> |



 

### <a name="menus"></a><span data-ttu-id="2a490-133">Menüs</span><span class="sxs-lookup"><span data-stu-id="2a490-133">Menus</span></span>

<span data-ttu-id="2a490-134">Wenn eine Anwendung ein Menü Trennzeichen aktiviert, sendet das System eine **WM- \_ Befehls** Nachricht, bei der das niedrige Wort des *wParam* -Parameters auf NULL festgelegt ist, wenn der Benutzer das Trennzeichen auswählt.</span><span class="sxs-lookup"><span data-stu-id="2a490-134">If an application enables a menu separator, the system sends a **WM\_COMMAND** message with the low-word of the *wParam* parameter set to zero when the user selects the separator.</span></span>

<span data-ttu-id="2a490-135">Wenn ein Menü mit einem [**menuinfo. dwstyle**](/windows/win32/api/winuser/ns-winuser-menuinfo) -Wert von **MNS \_ notifybypos** definiert ist, wird [**WM \_ MenuCommand**](wm-menucommand.md) anstelle des **WM- \_ Befehls** gesendet.</span><span class="sxs-lookup"><span data-stu-id="2a490-135">If a menu is defined with a [**MENUINFO.dwStyle**](/windows/win32/api/winuser/ns-winuser-menuinfo) value of **MNS\_NOTIFYBYPOS**, [**WM\_MENUCOMMAND**](wm-menucommand.md) is sent instead of **WM\_COMMAND**.</span></span>

### <a name="accelerators"></a><span data-ttu-id="2a490-136">Zugriffstasten</span><span class="sxs-lookup"><span data-stu-id="2a490-136">Accelerators</span></span>

<span data-ttu-id="2a490-137">Tastenkombinationen, die Elemente aus dem Menü Fenster auswählen, werden in die [**WM- \_ syscommand**](wm-syscommand.md) -Meldungen übersetzt.</span><span class="sxs-lookup"><span data-stu-id="2a490-137">Accelerator keystrokes that select items from the window menu are translated into [**WM\_SYSCOMMAND**](wm-syscommand.md) messages.</span></span>

<span data-ttu-id="2a490-138">Wenn eine Zugriffstasten-Tastatureingabe auftritt, die einem Menü Element entspricht, wenn das Fenster, das das Menü besitzt, minimiert ist, wird keine **WM- \_ Befehls** Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="2a490-138">If an accelerator keystroke occurs that corresponds to a menu item when the window that owns the menu is minimized, no **WM\_COMMAND** message is sent.</span></span> <span data-ttu-id="2a490-139">Wenn jedoch eine Tastenkombination angezeigt wird, die nicht mit den Elementen im Menü des Fensters oder im Menü Fenster identisch ist, wird eine WM- **\_ Befehls** Nachricht gesendet, auch wenn das Fenster minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="2a490-139">However, if an accelerator keystroke occurs that does not match any of the items in the window's menu or in the window menu, a **WM\_COMMAND** message is sent, even if the window is minimized.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a490-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a490-140">Requirements</span></span>



| <span data-ttu-id="2a490-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a490-141">Requirement</span></span> | <span data-ttu-id="2a490-142">Wert</span><span class="sxs-lookup"><span data-stu-id="2a490-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a490-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a490-143">Minimum supported client</span></span><br/> | <span data-ttu-id="2a490-144">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a490-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2a490-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a490-145">Minimum supported server</span></span><br/> | <span data-ttu-id="2a490-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a490-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2a490-147">Header</span><span class="sxs-lookup"><span data-stu-id="2a490-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a490-148"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="2a490-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a490-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a490-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="2a490-150">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="2a490-150">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="2a490-151">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2a490-151">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="2a490-152">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2a490-152">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="2a490-153">**Licher**</span><span class="sxs-lookup"><span data-stu-id="2a490-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2a490-154">Menüs</span><span class="sxs-lookup"><span data-stu-id="2a490-154">Menus</span></span>](menus.md)
</dt> </dl>

 

