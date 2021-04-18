---
title: WM_TOUCH Meldung (Winuser. h)
description: Benachrichtigt das Fenster, wenn ein oder mehrere Berührungspunkte, z. b. ein Finger oder Stift, eine berührungsempfindliche Digitalisierungs Oberfläche berührt.
ms.assetid: 5dee8bab-34fa-4dd9-a65b-35883757ec80
keywords:
- Windows-Fingereingabe für WM_TOUCH Meldung
topic_type:
- apiref
api_name:
- WM_TOUCH
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b6242d43b661240d946d2883237640d1bc92b3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392051"
---
# <a name="wm_touch-message"></a><span data-ttu-id="96a07-104">WM-Fingereingabe \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="96a07-104">WM\_TOUCH message</span></span>

<span data-ttu-id="96a07-105">Benachrichtigt das Fenster, wenn ein oder mehrere Berührungspunkte, z. b. ein Finger oder Stift, eine berührungsempfindliche Digitalisierungs Oberfläche berührt.</span><span class="sxs-lookup"><span data-stu-id="96a07-105">Notifies the window when one or more touch points, such as a finger or pen, touches a touch-sensitive digitizer surface.</span></span>

## <a name="parameters"></a><span data-ttu-id="96a07-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="96a07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96a07-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96a07-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96a07-108">Das nieder wertige Wort enthält die Anzahl der der Nachricht zugeordneten Berührungspunkte.</span><span class="sxs-lookup"><span data-stu-id="96a07-108">The low-order word contains the number of touch points associated with this message.</span></span> <span data-ttu-id="96a07-109">Das höchst wertige Wort ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="96a07-109">The high-order word is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="96a07-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96a07-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96a07-111">Enthält ein Fingereingabe handle, das in einem Aufrufen von [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) verwendet werden kann, um ausführliche Informationen zu den mit dieser Meldung verknüpften Berührungspunkten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="96a07-111">Contains a touch input handle that can be used in a call to [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) to retrieve detailed information about the touch points associated with this message.</span></span>

<span data-ttu-id="96a07-112">Dieses Handle ist nur innerhalb des aktuellen Prozesses gültig und sollte nicht Prozess übergreifend übermittelt werden, außer als **LPARAM** in einem **SendMessage** -oder **PostMessage** -Befehl.</span><span class="sxs-lookup"><span data-stu-id="96a07-112">This handle is valid only within the current process and should not be passed cross-process except as the **LPARAM** in a **SendMessage** or **PostMessage** call.</span></span>

<span data-ttu-id="96a07-113">Wenn die Anwendung dieses Handle nicht mehr benötigt, muss die Anwendung **closetouchinputhandle** aufrufen, um den mit diesem Handle verknüpften Prozess Speicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="96a07-113">When the application no longer requires this handle, the application must call **CloseTouchInputHandle** to free the process memory associated with this handle.</span></span> <span data-ttu-id="96a07-114">Wenn dies nicht der Fall ist, kann dies zu einem Anwendungs Arbeitsspeicher-Fehler führen.</span><span class="sxs-lookup"><span data-stu-id="96a07-114">Failing to do so can result in an application memory leak.</span></span>

<span data-ttu-id="96a07-115">Beachten Sie, dass das Berührungs Eingabe Handle in diesem Parameter nicht mehr gültig ist, nachdem die Nachricht an [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca)übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="96a07-115">Note that the touch input handle in this parameter is no longer valid after the message has been passed to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="96a07-116">Mit [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca) wird dieses Handle geschlossen und ungültig.</span><span class="sxs-lookup"><span data-stu-id="96a07-116">[DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) will close and invalidate this handle.</span></span>

<span data-ttu-id="96a07-117">Beachten Sie auch, dass das Fingereingabe Handle in diesem Parameter nicht mehr gültig ist, nachdem die Nachricht mithilfe von [**Post Message**](sendmessage--postmessage--and-related-functions.md), **SendMessage** oder einer ihrer Varianten weitergeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="96a07-117">Note also that the touch input handle in this parameter is no longer valid after the message has been forwarded using [**PostMessage**](sendmessage--postmessage--and-related-functions.md), **SendMessage**, or one of their variants.</span></span> <span data-ttu-id="96a07-118">Diese Funktionen werden dieses Handle schließen und für ungültig erklären.</span><span class="sxs-lookup"><span data-stu-id="96a07-118">These functions will close and invalidate this handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96a07-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96a07-119">Return value</span></span>

<span data-ttu-id="96a07-120">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="96a07-120">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="96a07-121">Wenn die Anwendung die Nachricht nicht verarbeitet, muss Sie [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="96a07-121">If the application does not process the message, it must call [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="96a07-122">Wenn Sie dies nicht tun, wird der Arbeitsspeicher nicht durch die Anwendung getrennt, da der Fingereingabe Handle nicht geschlossen und zugeordneter Prozess Speicher nicht freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="96a07-122">Not doing so causes the application to leak memory because the touch input handle is not closed and associated process memory is not freed.</span></span>

## <a name="remarks"></a><span data-ttu-id="96a07-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96a07-123">Remarks</span></span>

<span data-ttu-id="96a07-124">**WM \_** Die Fingereingabe-Nachrichten berücksichtigen keine " **httransparent** "-Fensterbereiche.</span><span class="sxs-lookup"><span data-stu-id="96a07-124">**WM\_TOUCH** messages do not respect **HTTRANSPARENT** regions of windows.</span></span> <span data-ttu-id="96a07-125">Wenn ein Fenster als Antwort auf eine **WM- \_ nchittest** -Nachricht " **httransparent** " zurückgibt, werden die Maus Meldungen an das übergeordnete Element gesendet, und **WM \_** -Finger Eingaben werden direkt an das Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="96a07-125">If a window returns **HTTRANSPARENT** in response to a **WM\_NCHITTEST** message, mouse messages go to the parent, and **WM\_TOUCH** messages go directly to the window.</span></span>

## <a name="examples"></a><span data-ttu-id="96a07-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96a07-126">Examples</span></span>

<span data-ttu-id="96a07-127">Der folgende Code ist ein Beispiel für das Abrufen detaillierter Fingereingabe Informationen, die dieser Nachricht zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="96a07-127">The following code is an example of how to obtain detailed touch input information associated with this message.</span></span>


```C++
UINT cInputs = LOWORD(wParam);
PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
if (NULL != pInputs)
{
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
                          cInputs,
                          pInputs,
                          sizeof(TOUCHINPUT)))
    {
        // process pInputs
        if (!CloseTouchInputHandle((HTOUCHINPUT)lParam))
        {
            // error handling
        }
    }
    else
    {
        // GetLastError() and error handling
    }
    delete [] pInputs;
}
else
{
    // error handling, presumably out of memory
}
return DefWindowProc(hWnd, message, wParam, lParam);
```



## <a name="requirements"></a><span data-ttu-id="96a07-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96a07-128">Requirements</span></span>



| <span data-ttu-id="96a07-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96a07-129">Requirement</span></span> | <span data-ttu-id="96a07-130">Wert</span><span class="sxs-lookup"><span data-stu-id="96a07-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96a07-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96a07-131">Minimum supported client</span></span><br/> | <span data-ttu-id="96a07-132">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96a07-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="96a07-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="96a07-133">Minimum supported server</span></span><br/> | <span data-ttu-id="96a07-134">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96a07-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="96a07-135">Header</span><span class="sxs-lookup"><span data-stu-id="96a07-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="96a07-136"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="96a07-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96a07-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96a07-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96a07-138">Meldungen</span><span class="sxs-lookup"><span data-stu-id="96a07-138">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="96a07-139">Programmier Handbuch zu Manipulationen und Trägheit</span><span class="sxs-lookup"><span data-stu-id="96a07-139">Manipulations and Inertia Programming Guide</span></span>](manipulation-and-inertia.md)
</dt> <dt>

[<span data-ttu-id="96a07-140">Leitfaden zur Eingabe der Windows-Eingabe Eingabe</span><span class="sxs-lookup"><span data-stu-id="96a07-140">Windows Touch Input Programming Guide</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

