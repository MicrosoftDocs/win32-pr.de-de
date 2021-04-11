---
title: WM_NOTIFY Meldung (Winuser. h)
description: Wird von einem allgemeinen Steuerelement an das übergeordnete Fenster gesendet, wenn ein Ereignis aufgetreten ist oder das Steuerelement einige Informationen erfordert.
ms.assetid: vs|controls|~\controls\common\messages\wm_notify.htm
keywords:
- Windows-Steuerelemente für WM_NOTIFY Meldung
topic_type:
- apiref
api_name:
- WM_NOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1905954e7fb164f8436216fa918cc6f243f4b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956711"
---
# <a name="wm_notify-message"></a><span data-ttu-id="43ee7-104">WM- \_ Benachrichtigungs Meldung</span><span class="sxs-lookup"><span data-stu-id="43ee7-104">WM\_NOTIFY message</span></span>

<span data-ttu-id="43ee7-105">Wird von einem allgemeinen Steuerelement an das übergeordnete Fenster gesendet, wenn ein Ereignis aufgetreten ist oder das Steuerelement einige Informationen erfordert.</span><span class="sxs-lookup"><span data-stu-id="43ee7-105">Sent by a common control to its parent window when an event has occurred or the control requires some information.</span></span>

## <a name="parameters"></a><span data-ttu-id="43ee7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="43ee7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43ee7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43ee7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43ee7-108">Der Bezeichner des allgemeinen Steuer Elements, das die Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="43ee7-108">The identifier of the common control sending the message.</span></span> <span data-ttu-id="43ee7-109">Es ist nicht garantiert, dass dieser Bezeichner eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="43ee7-109">This identifier is not guaranteed to be unique.</span></span> <span data-ttu-id="43ee7-110">Eine Anwendung sollte das **hwndfrom** -oder **idfrom** -Member der [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur (übergeben als *LPARAM* -Parameter) verwenden, um das Steuerelement zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="43ee7-110">An application should use the **hwndFrom** or **idFrom** member of the [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure (passed as the *lParam* parameter) to identify the control.</span></span>

</dd> <dt>

<span data-ttu-id="43ee7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43ee7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43ee7-112">Ein Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die den Benachrichtigungs Code und zusätzliche Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="43ee7-112">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains the notification code and additional information.</span></span> <span data-ttu-id="43ee7-113">Bei einigen Benachrichtigungs Meldungen verweist dieser Parameter auf eine größere Struktur, die über die **NMHDR** -Struktur als erstes Element verfügt.</span><span class="sxs-lookup"><span data-stu-id="43ee7-113">For some notification messages, this parameter points to a larger structure that has the **NMHDR** structure as its first member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43ee7-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43ee7-114">Return value</span></span>

<span data-ttu-id="43ee7-115">Der Rückgabewert wird ignoriert, außer bei Benachrichtigungs Meldungen, die andernfalls angeben.</span><span class="sxs-lookup"><span data-stu-id="43ee7-115">The return value is ignored except for notification messages that specify otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="43ee7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43ee7-116">Remarks</span></span>

<span data-ttu-id="43ee7-117">Das Ziel der Nachricht muss das **HWND** des übergeordneten Elements des Steuer Elements sein.</span><span class="sxs-lookup"><span data-stu-id="43ee7-117">The destination of the message must be the **HWND** of the parent of the control.</span></span> <span data-ttu-id="43ee7-118">Dieser Wert kann mithilfe von [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent)abgerufen werden, wie im folgenden Beispiel gezeigt, wobei *m \_ controlhwnd* das **HWND** des Steuer Elements selbst ist.</span><span class="sxs-lookup"><span data-stu-id="43ee7-118">This value can be obtained by using [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent), as shown in the following example, where *m\_controlHwnd* is the **HWND** of the control itself.</span></span>


```
NMHDR nmh;
nmh.code = CUSTOM_SELCHANGE;    // Message type defined by control.
nmh.idFrom = GetDlgCtrlID(m_controlHwnd);
nmh.hwndFrom = m_controlHwnd;
SendMessage(GetParent(m_controlHwnd), 
    WM_NOTIFY, 
    nmh.idFrom, 
    (LPARAM)&nmh);
```



<span data-ttu-id="43ee7-119">Anwendungen verarbeiten die Meldung in der Fenster Prozedur des übergeordneten Fensters, wie im folgenden Beispiel gezeigt, das die vom benutzerdefinierten Steuerelement im vorherigen Beispiel gesendete Benachrichtigungs Meldung behandelt.</span><span class="sxs-lookup"><span data-stu-id="43ee7-119">Applications handle the message in the window procedure of the parent window, as shown in the following example, which handles the notification message sent by the custom control in the previous example.</span></span>


```
INT_PTR CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_NOTIFY:
        switch (((LPNMHDR)lParam)->code)
        {
        case CUSTOM_SELCHANGE:
            if (((LPNMHDR)lParam)->idFrom == IDC_CUSTOMLISTBOX1)
            {
                ...   // Respond to message.
                return TRUE;
            }
            break; 
        ... // More cases on WM_NOTIFY switch.
        break;
        }
    ...  // More cases on message switch.
    }
    return FALSE;
}
```



<span data-ttu-id="43ee7-120">Einige Benachrichtigungen, vor allem diejenigen, die für einen längeren Zeitraum in der API enthalten waren, werden als [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Nachrichten gesendet.</span><span class="sxs-lookup"><span data-stu-id="43ee7-120">Some notifications, chiefly those that have been in the API for a long time, are sent as [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="43ee7-121">Weitere Informationen finden Sie unter [Control Messages](control-messages.md).</span><span class="sxs-lookup"><span data-stu-id="43ee7-121">For more information, see [Control Messages](control-messages.md).</span></span>

<span data-ttu-id="43ee7-122">Wenn sich der Nachrichten Handler in einer Dialogfeld Prozedur befindet, müssen Sie die Funktion [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) mit DWL \_ msgresult verwenden, um einen Rückgabewert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="43ee7-122">If the message handler is in a dialog box procedure, you must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT to set a return value.</span></span>

<span data-ttu-id="43ee7-123">Für Windows Vista-Systeme und spätere Systeme kann die **WM- \_ Benachrichtigungs** Meldung nicht zwischen Prozessen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="43ee7-123">For Windows Vista and later systems, the **WM\_NOTIFY** message cannot be sent between processes.</span></span>

<span data-ttu-id="43ee7-124">Viele Benachrichtigungen sind sowohl im ANSI-als auch im Unicode-Format verfügbar.</span><span class="sxs-lookup"><span data-stu-id="43ee7-124">Many notifications are available in both ANSI and Unicode formats.</span></span> <span data-ttu-id="43ee7-125">Das Fenster, das die **WM- \_ Benachrichtigungs** Meldung sendet, verwendet die [**WM \_ notifyformat**](wm-notifyformat.md) -Meldung, um zu bestimmen, welches Format verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="43ee7-125">The window sending the **WM\_NOTIFY** message uses the [**WM\_NOTIFYFORMAT**](wm-notifyformat.md) message to determine which format should be used.</span></span> <span data-ttu-id="43ee7-126">Weitere Erläuterungen finden Sie unter **WM \_ notifyformat** .</span><span class="sxs-lookup"><span data-stu-id="43ee7-126">See **WM\_NOTIFYFORMAT** for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="43ee7-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43ee7-127">Requirements</span></span>



| <span data-ttu-id="43ee7-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43ee7-128">Requirement</span></span> | <span data-ttu-id="43ee7-129">Wert</span><span class="sxs-lookup"><span data-stu-id="43ee7-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="43ee7-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43ee7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="43ee7-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43ee7-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="43ee7-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43ee7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="43ee7-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43ee7-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="43ee7-134">Header</span><span class="sxs-lookup"><span data-stu-id="43ee7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="43ee7-135"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="43ee7-135"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43ee7-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43ee7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43ee7-137">**WM \_ notifyformat**</span><span class="sxs-lookup"><span data-stu-id="43ee7-137">**WM\_NOTIFYFORMAT**</span></span>](wm-notifyformat.md)
</dt> </dl>

 

