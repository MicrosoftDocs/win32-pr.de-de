---
title: WM_RENDERALLFORMATS Meldung (Winuser. h)
description: Wird an den Besitzer der Zwischenablage gesendet, bevor er zerstört wird, wenn der Besitzer der Zwischenablage ein oder mehrere Zwischenablage Formate verzögert rendert.
ms.assetid: dff9100f-2dba-467d-be74-a9a9c2b2122b
keywords:
- WM_RENDERALLFORMATS Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_RENDERALLFORMATS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cdd3ce1fabdea4cdcae93b5243b89c53def0afa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518554"
---
# <a name="wm_renderallformats-message"></a><span data-ttu-id="c0f65-104">WM \_ renderallformats-Meldung</span><span class="sxs-lookup"><span data-stu-id="c0f65-104">WM\_RENDERALLFORMATS message</span></span>

<span data-ttu-id="c0f65-105">Wird an den Besitzer der Zwischenablage gesendet, bevor er zerstört wird, wenn der Besitzer der Zwischenablage ein oder mehrere Zwischenablage Formate verzögert rendert.</span><span class="sxs-lookup"><span data-stu-id="c0f65-105">Sent to the clipboard owner before it is destroyed, if the clipboard owner has delayed rendering one or more clipboard formats.</span></span> <span data-ttu-id="c0f65-106">Damit der Inhalt der Zwischenablage anderen Anwendungen zur Verfügung steht, muss der Besitzer der Zwischenablage Daten in allen Formaten Renderingformate renderingfähig sein und die Daten in der Zwischenablage platzieren, indem die [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c0f65-106">For the content of the clipboard to remain available to other applications, the clipboard owner must render data in all the formats it is capable of generating, and place the data on the clipboard by calling the [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) function.</span></span>

<span data-ttu-id="c0f65-107">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c0f65-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_RENDERALLFORMATS             0x0306
```



## <a name="parameters"></a><span data-ttu-id="c0f65-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0f65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0f65-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c0f65-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0f65-110">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="c0f65-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c0f65-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0f65-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0f65-112">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="c0f65-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0f65-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0f65-113">Return value</span></span>

<span data-ttu-id="c0f65-114">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c0f65-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0f65-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0f65-115">Remarks</span></span>

<span data-ttu-id="c0f65-116">Bei der Reaktion auf eine **WM- \_ renderallformats** -Nachricht muss die Anwendung die [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) -Funktion aufrufen und dann überprüfen, ob Sie noch der Besitzer der Zwischenablage ist, indem Sie die [**getclipboardowner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) -Funktion aufruft, bevor [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c0f65-116">When responding to a **WM\_RENDERALLFORMATS** message, the application must call the [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) function and then check that it is still the clipboard owner by calling the [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) function before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span></span>

<span data-ttu-id="c0f65-117">Die Anwendung muss überprüfen, ob Sie nach dem Öffnen der Zwischenablage immer noch der Besitzer der Zwischenablage ist, da nach dem Empfang der **WM- \_ renderallformats** -Nachricht, aber vor dem Öffnen der Zwischenablage eine andere Anwendung den Besitz der Zwischenablage geöffnet und übernommen hat und die Daten dieser Anwendung nicht überschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c0f65-117">The application needs to check that it is still the clipboard owner after opening the clipboard because after it receives the **WM\_RENDERALLFORMATS** message, but before it opens the clipboard, another application may have opened and taken ownership of the clipboard, and that application's data should not be overwritten.</span></span>

<span data-ttu-id="c0f65-118">In den meisten Fällen sollte die Anwendung die [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) -Funktion vor dem Aufruf von [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)nicht aufrufen, da dadurch die Zwischenablage Formate gelöscht werden, die von der Anwendung bereits gerendert wurden.</span><span class="sxs-lookup"><span data-stu-id="c0f65-118">In most cases, the application should not call the [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) function before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata), since doing so will erase the clipboard formats that the application has already rendered.</span></span>

<span data-ttu-id="c0f65-119">Wenn die Anwendung zurückgegeben wird, entfernt das System alle nicht gerenderten Formate aus der Liste der verfügbaren Zwischenablage Formate.</span><span class="sxs-lookup"><span data-stu-id="c0f65-119">When the application returns, the system removes any unrendered formats from the list of available clipboard formats.</span></span> <span data-ttu-id="c0f65-120">Weitere Informationen zum verzögerten Rendering finden Sie unter [Verzögertes Rendering](clipboard-operations.md#delayed-rendering).</span><span class="sxs-lookup"><span data-stu-id="c0f65-120">For information about delayed rendering, see [Delayed Rendering](clipboard-operations.md#delayed-rendering).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0f65-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0f65-121">Requirements</span></span>



| <span data-ttu-id="c0f65-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0f65-122">Requirement</span></span> | <span data-ttu-id="c0f65-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c0f65-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f65-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0f65-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c0f65-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0f65-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c0f65-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0f65-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c0f65-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0f65-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c0f65-128">Header</span><span class="sxs-lookup"><span data-stu-id="c0f65-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0f65-129"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c0f65-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0f65-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0f65-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="c0f65-131">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c0f65-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c0f65-132">**EmptyClipboard**</span><span class="sxs-lookup"><span data-stu-id="c0f65-132">**EmptyClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

[<span data-ttu-id="c0f65-133">**OpenClipboard**</span><span class="sxs-lookup"><span data-stu-id="c0f65-133">**OpenClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-openclipboard)
</dt> <dt>

[<span data-ttu-id="c0f65-134">**SetClipboardData**</span><span class="sxs-lookup"><span data-stu-id="c0f65-134">**SetClipboardData**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[<span data-ttu-id="c0f65-135">**WM- \_ Renderformat**</span><span class="sxs-lookup"><span data-stu-id="c0f65-135">**WM\_RENDERFORMAT**</span></span>](wm-renderformat.md)
</dt> <dt>

<span data-ttu-id="c0f65-136">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c0f65-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c0f65-137">Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="c0f65-137">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

