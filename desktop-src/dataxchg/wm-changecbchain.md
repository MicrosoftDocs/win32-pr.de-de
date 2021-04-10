---
title: WM_CHANGECBCHAIN Meldung (Winuser. h)
description: Wird an das erste Fenster in der Zwischenablage-Viewer-Kette gesendet, wenn ein Fenster aus der Kette entfernt wird. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 7be87342-87fa-4cd2-b066-0b36b7ef52f5
keywords:
- WM_CHANGECBCHAIN Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_CHANGECBCHAIN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab91640320e3659d0e9fb130f5c773ccbb7c4e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104090"
---
# <a name="wm_changecbchain-message"></a><span data-ttu-id="47a39-105">WM \_ CHANGECBCHAIN-Meldung</span><span class="sxs-lookup"><span data-stu-id="47a39-105">WM\_CHANGECBCHAIN message</span></span>

<span data-ttu-id="47a39-106">Wird an das erste Fenster in der Zwischenablage-Viewer-Kette gesendet, wenn ein Fenster aus der Kette entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="47a39-106">Sent to the first window in the clipboard viewer chain when a window is being removed from the chain.</span></span>

<span data-ttu-id="47a39-107">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="47a39-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CHANGECBCHAIN                0x030D
```



## <a name="parameters"></a><span data-ttu-id="47a39-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="47a39-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47a39-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="47a39-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="47a39-110">Ein Handle für das Fenster, das aus der Zwischenablage-Viewer-Kette entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="47a39-110">A handle to the window being removed from the clipboard viewer chain.</span></span>

</dd> <dt>

<span data-ttu-id="47a39-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="47a39-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="47a39-112">Ein Handle für das nächste Fenster in der Kette nach dem Fenster, das entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="47a39-112">A handle to the next window in the chain following the window being removed.</span></span> <span data-ttu-id="47a39-113">Dieser Parameter ist **null** , wenn das Fenster, das entfernt wird, das letzte Fenster in der Kette ist.</span><span class="sxs-lookup"><span data-stu-id="47a39-113">This parameter is **NULL** if the window being removed is the last window in the chain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47a39-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47a39-114">Return value</span></span>

<span data-ttu-id="47a39-115">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="47a39-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="47a39-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47a39-116">Remarks</span></span>

<span data-ttu-id="47a39-117">Jedes Fenster der Zwischenablage Anzeige speichert das Handle für das nächste Fenster in der Zwischenablage-Viewer-Kette.</span><span class="sxs-lookup"><span data-stu-id="47a39-117">Each clipboard viewer window saves the handle to the next window in the clipboard viewer chain.</span></span> <span data-ttu-id="47a39-118">Anfänglich ist dieses Handle der Rückgabewert der Funktion [**setclipboardviewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .</span><span class="sxs-lookup"><span data-stu-id="47a39-118">Initially, this handle is the return value of the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span>

<span data-ttu-id="47a39-119">Wenn ein Fenster der Zwischenablage Anzeige die **WM- \_ CHANGECBCHAIN** -Nachricht empfängt, sollte die [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion aufgerufen werden, um die Nachricht an das nächste Fenster in der Kette zu übergeben, es sei denn, das Fenster wird im nächsten Fenster entfernt.</span><span class="sxs-lookup"><span data-stu-id="47a39-119">When a clipboard viewer window receives the **WM\_CHANGECBCHAIN** message, it should call the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to pass the message to the next window in the chain, unless the next window is the window being removed.</span></span> <span data-ttu-id="47a39-120">In diesem Fall sollte der Zwischenablage-Viewer das durch den *LPARAM* -Parameter angegebene Handle als das nächste Fenster in der Kette speichern.</span><span class="sxs-lookup"><span data-stu-id="47a39-120">In this case, the clipboard viewer should save the handle specified by the *lParam* parameter as the next window in the chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="47a39-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47a39-121">Requirements</span></span>



| <span data-ttu-id="47a39-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47a39-122">Requirement</span></span> | <span data-ttu-id="47a39-123">Wert</span><span class="sxs-lookup"><span data-stu-id="47a39-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47a39-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47a39-124">Minimum supported client</span></span><br/> | <span data-ttu-id="47a39-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47a39-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="47a39-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47a39-126">Minimum supported server</span></span><br/> | <span data-ttu-id="47a39-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47a39-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="47a39-128">Header</span><span class="sxs-lookup"><span data-stu-id="47a39-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="47a39-129"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="47a39-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47a39-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47a39-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="47a39-131">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="47a39-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="47a39-132">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="47a39-132">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="47a39-133">**Setclipboardviewer**</span><span class="sxs-lookup"><span data-stu-id="47a39-133">**SetClipboardViewer**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

<span data-ttu-id="47a39-134">**Licher**</span><span class="sxs-lookup"><span data-stu-id="47a39-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="47a39-135">Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="47a39-135">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

