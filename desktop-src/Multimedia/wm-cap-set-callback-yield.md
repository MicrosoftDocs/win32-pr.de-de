---
title: WM_CAP_SET_CALLBACK_YIELD Meldung (VFW. h)
description: Die "WM \_ Cap \_ Set Callback yield"- \_ \_ Nachricht legt eine Rückruffunktion in der Anwendung fest. Avicap ruft dieses Verfahren auf, wenn das Erfassungsfenster während der streamingerfassung ergibt. Sie können diese Nachricht explizit oder mithilfe des capsetcallbackonyield-Makros senden.
ms.assetid: d978dc3b-4336-46a4-85ae-7d588a63489b
keywords:
- WM_CAP_SET_CALLBACK_YIELD-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_YIELD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95c9ba0be7a0abeb99c0590e255adb0bd442343
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337903"
---
# <a name="wm_cap_set_callback_yield-message"></a><span data-ttu-id="1811d-106">Zurück \_ gebende \_ \_ Rückruf \_ Meldung für die WM-Abdeckung</span><span class="sxs-lookup"><span data-stu-id="1811d-106">WM\_CAP\_SET\_CALLBACK\_YIELD message</span></span>

<span data-ttu-id="1811d-107">Die " **WM \_ Cap \_ Set \_ Callback \_ Yield** "-Nachricht legt eine Rückruffunktion in der Anwendung fest.</span><span class="sxs-lookup"><span data-stu-id="1811d-107">The **WM\_CAP\_SET\_CALLBACK\_YIELD** message sets a callback function in the application.</span></span> <span data-ttu-id="1811d-108">Avicap ruft dieses Verfahren auf, wenn das Erfassungsfenster während der streamingerfassung ergibt.</span><span class="sxs-lookup"><span data-stu-id="1811d-108">AVICap calls this procedure when the capture window yields during streaming capture.</span></span> <span data-ttu-id="1811d-109">Sie können diese Nachricht explizit oder mithilfe des [**capsetcallbackonyield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="1811d-109">You can send this message explicitly or by using the [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_YIELD 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="1811d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1811d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1811d-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpproc*</span><span class="sxs-lookup"><span data-stu-id="1811d-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="1811d-112">Ein Zeiger auf die Yield Callback-Funktion vom Typ [**capyieldcallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback).</span><span class="sxs-lookup"><span data-stu-id="1811d-112">Pointer to the yield callback function, of type [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback).</span></span> <span data-ttu-id="1811d-113">Geben Sie **null** für diesen Parameter an, um eine zuvor installierte Yield-Rückruffunktion zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="1811d-113">Specify **NULL** for this parameter to disable a previously installed yield callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1811d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1811d-114">Return Value</span></span>

<span data-ttu-id="1811d-115">Gibt **true** zurück, wenn erfolgreich oder **false** , wenn eine streamingerfassung oder eine Single-Frame-Erfassungs Sitzung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1811d-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="1811d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1811d-116">Remarks</span></span>

<span data-ttu-id="1811d-117">Anwendungen können optional eine Yield-Rückruffunktion festlegen.</span><span class="sxs-lookup"><span data-stu-id="1811d-117">Applications can optionally set a yield callback function.</span></span> <span data-ttu-id="1811d-118">Die Yield Callback-Funktion wird für jeden Video Frame, der während der streamingerfassung aufgezeichnet wurde, mindestens einmal aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1811d-118">The yield callback function is called at least once for each video frame captured during streaming capture.</span></span> <span data-ttu-id="1811d-119">Wenn eine Yield Callback-Funktion installiert ist, wird Sie unabhängig vom Zustand des **fyield** -Members der [**captuprojektstruktur**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1811d-119">If a yield callback function is installed, it will be called regardless of the state of the **fYield** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

<span data-ttu-id="1811d-120">Wenn die Yield Callback-Funktion verwendet wird, muss Sie vor dem Start der Erfassungs Sitzung installiert werden, und Sie muss für die Dauer der Sitzung aktiviert bleiben.</span><span class="sxs-lookup"><span data-stu-id="1811d-120">If the yield callback function is used, it must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="1811d-121">Sie kann nach Ende der streamingerfassung deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="1811d-121">It can be disabled after streaming capture ends.</span></span>

<span data-ttu-id="1811d-122">Anwendungen führen in der Regel eine Art der Nachrichtenverarbeitung in der Rückruffunktion aus, die aus einer " [Peer-Message](/windows/win32/api/winuser/nf-winuser-peekmessagea)", " [translatemess Age](/windows/win32/api/winuser/nf-winuser-translatemessage)" und " [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) "-Schleife besteht, wie in der Nachrichten Schleife einer [WinMain](/windows/win32/api/winbase/nf-winbase-winmain) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="1811d-122">Applications typically perform some type of message processing in the callback function consisting of a [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) loop, as in the message loop of a [WinMain](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="1811d-123">Die Yield Callback-Funktion muss auch Nachrichten filtern und entfernen, die Probleme bei der Wiedereintritts Fähigkeit verursachen können.</span><span class="sxs-lookup"><span data-stu-id="1811d-123">The yield callback function must also filter and remove messages that can cause reentrancy problems.</span></span>

<span data-ttu-id="1811d-124">Eine Anwendung gibt in der Regel " **true** " zurück, um die streamingerfassung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="1811d-124">An application typically returns **TRUE** in the yield procedure to continue streaming capture.</span></span> <span data-ttu-id="1811d-125">Wenn eine Yield Callback-Funktion **false** zurückgibt, hält das Erfassungsfenster den Erfassungsprozess an.</span><span class="sxs-lookup"><span data-stu-id="1811d-125">If a yield callback function returns **FALSE**, the capture window stops the capture process.</span></span>

## <a name="requirements"></a><span data-ttu-id="1811d-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1811d-126">Requirements</span></span>



| <span data-ttu-id="1811d-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1811d-127">Requirement</span></span> | <span data-ttu-id="1811d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="1811d-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1811d-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1811d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1811d-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1811d-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1811d-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1811d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1811d-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1811d-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1811d-133">Header</span><span class="sxs-lookup"><span data-stu-id="1811d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1811d-134"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="1811d-134"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1811d-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1811d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1811d-136">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="1811d-136">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="1811d-137">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="1811d-137">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

