---
description: Wird gesendet, wenn ein Fenster zerstört wird. Sie wird an die Fenster Prozedur des Fensters gesendet, das zerstört wird, nachdem das Fenster aus dem Bildschirm entfernt wurde.
ms.assetid: 089c0645-199b-4a90-9cbc-740f0cf3267d
title: WM_DESTROY Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db195c22c38759146fb76e98edf4ca7f605a1c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216960"
---
# <a name="wm_destroy-message"></a><span data-ttu-id="7a7fc-104">WM-Lösch \_ Meldung</span><span class="sxs-lookup"><span data-stu-id="7a7fc-104">WM\_DESTROY message</span></span>

<span data-ttu-id="7a7fc-105">Wird gesendet, wenn ein Fenster zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="7a7fc-105">Sent when a window is being destroyed.</span></span> <span data-ttu-id="7a7fc-106">Sie wird an die Fenster Prozedur des Fensters gesendet, das zerstört wird, nachdem das Fenster aus dem Bildschirm entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="7a7fc-106">It is sent to the window procedure of the window being destroyed after the window is removed from the screen.</span></span>

<span data-ttu-id="7a7fc-107">Diese Meldung wird zuerst an das Fenster gesendet, das zerstört wird, und dann an die untergeordneten Fenster (sofern vorhanden), wenn Sie zerstört werden.</span><span class="sxs-lookup"><span data-stu-id="7a7fc-107">This message is sent first to the window being destroyed and then to the child windows (if any) as they are destroyed.</span></span> <span data-ttu-id="7a7fc-108">Bei der Verarbeitung der Nachricht kann davon ausgegangen werden, dass alle untergeordneten Fenster noch vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="7a7fc-108">During the processing of the message, it can be assumed that all child windows still exist.</span></span>

<span data-ttu-id="7a7fc-109">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7a7fc-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DESTROY                      0x0002
```



## <a name="parameters"></a><span data-ttu-id="7a7fc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a7fc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a7fc-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7a7fc-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a7fc-112">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a7fc-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7a7fc-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a7fc-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a7fc-114">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a7fc-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a7fc-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a7fc-115">Return value</span></span>

<span data-ttu-id="7a7fc-116">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="7a7fc-116">Type: **LRESULT**</span></span>

<span data-ttu-id="7a7fc-117">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7a7fc-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a7fc-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a7fc-118">Remarks</span></span>

<span data-ttu-id="7a7fc-119">Wenn das Fenster, das zerstört wird, Teil der Zwischenablage-Viewer-Kette ist (durch Aufrufen der [**setclipboardviewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) -Funktion festgelegt), muss sich das Fenster selbst aus der Kette entfernen, indem die [**changeclipboardchain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) -Funktion verarbeitet wird, bevor die WM-Lösch Nachricht zurückgegeben wird. **\_**</span><span class="sxs-lookup"><span data-stu-id="7a7fc-119">If the window being destroyed is part of the clipboard viewer chain (set by calling the [**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) function), the window must remove itself from the chain by processing the [**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) function before returning from the **WM\_DESTROY** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a7fc-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a7fc-120">Requirements</span></span>



| <span data-ttu-id="7a7fc-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a7fc-121">Requirement</span></span> | <span data-ttu-id="7a7fc-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7a7fc-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a7fc-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a7fc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7a7fc-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a7fc-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7a7fc-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a7fc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7a7fc-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a7fc-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7a7fc-127">Header</span><span class="sxs-lookup"><span data-stu-id="7a7fc-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a7fc-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="7a7fc-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a7fc-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a7fc-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="7a7fc-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="7a7fc-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7a7fc-131">**Changeclipboardchain**</span><span class="sxs-lookup"><span data-stu-id="7a7fc-131">**ChangeClipboardChain**</span></span>](/windows/win32/api/winuser/nf-winuser-changeclipboardchain)
</dt> <dt>

[<span data-ttu-id="7a7fc-132">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="7a7fc-132">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="7a7fc-133">**PostQuitMessage**</span><span class="sxs-lookup"><span data-stu-id="7a7fc-133">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[<span data-ttu-id="7a7fc-134">**Setclipboardviewer**</span><span class="sxs-lookup"><span data-stu-id="7a7fc-134">**SetClipboardViewer**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[<span data-ttu-id="7a7fc-135">**WM \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="7a7fc-135">**WM\_CLOSE**</span></span>](wm-close.md)
</dt> <dt>

<span data-ttu-id="7a7fc-136">**Licher**</span><span class="sxs-lookup"><span data-stu-id="7a7fc-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7a7fc-137">Windows</span><span class="sxs-lookup"><span data-stu-id="7a7fc-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
