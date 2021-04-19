---
title: WM_DRAWCLIPBOARD Meldung (Winuser. h)
description: Wird an das erste Fenster in der Zwischenablage-Viewer-Kette gesendet, wenn der Inhalt der Zwischenablage geändert wird. Dies ermöglicht es einem Fenster der Zwischenablage Anzeige, den neuen Inhalt der Zwischenablage anzuzeigen. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: ffaadf6f-588b-4a29-b26c-629087e7ce73
keywords:
- WM_DRAWCLIPBOARD Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_DRAWCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5ee6f6893375e2604cb39247745fc2758ce8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345289"
---
# <a name="wm_drawclipboard-message"></a><span data-ttu-id="7c620-106">WM- \_ drawclipboard-Nachricht</span><span class="sxs-lookup"><span data-stu-id="7c620-106">WM\_DRAWCLIPBOARD message</span></span>

<span data-ttu-id="7c620-107">Wird an das erste Fenster in der Zwischenablage-Viewer-Kette gesendet, wenn der Inhalt der Zwischenablage geändert wird.</span><span class="sxs-lookup"><span data-stu-id="7c620-107">Sent to the first window in the clipboard viewer chain when the content of the clipboard changes.</span></span> <span data-ttu-id="7c620-108">Dies ermöglicht es einem Fenster der Zwischenablage Anzeige, den neuen Inhalt der Zwischenablage anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7c620-108">This enables a clipboard viewer window to display the new content of the clipboard.</span></span>

<span data-ttu-id="7c620-109">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7c620-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DRAWCLIPBOARD                0x0308
```



## <a name="parameters"></a><span data-ttu-id="7c620-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c620-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c620-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c620-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c620-112">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7c620-112">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7c620-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c620-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c620-114">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7c620-114">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c620-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c620-115">Remarks</span></span>

<span data-ttu-id="7c620-116">Diese Meldung wird nur Zwischenablage-Viewer-Fenstern empfangen.</span><span class="sxs-lookup"><span data-stu-id="7c620-116">Only clipboard viewer windows receive this message.</span></span> <span data-ttu-id="7c620-117">Dies sind Fenster, die mithilfe der [**setclipboardviewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) -Funktion der Zwischenablage-Viewer-Kette hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="7c620-117">These are windows that have been added to the clipboard viewer chain by using the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span>

<span data-ttu-id="7c620-118">Jedes Fenster, das die " **WM \_ drawclipboard** "-Nachricht empfängt, muss die [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion anrufen, um die Nachricht an das nächste Fenster in der Zwischenablage-Viewer-Kette zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="7c620-118">Each window that receives the **WM\_DRAWCLIPBOARD** message must call the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to pass the message on to the next window in the clipboard viewer chain.</span></span> <span data-ttu-id="7c620-119">Das Handle für das nächste Fenster in der Kette wird von [**setclipboardviewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)zurückgegeben und kann sich als Reaktion auf eine [**WM- \_ CHANGECBCHAIN**](wm-changecbchain.md) -Nachricht ändern.</span><span class="sxs-lookup"><span data-stu-id="7c620-119">The handle to the next window in the chain is returned by [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer), and may change in response to a [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c620-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c620-120">Requirements</span></span>



| <span data-ttu-id="7c620-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c620-121">Requirement</span></span> | <span data-ttu-id="7c620-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7c620-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c620-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c620-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7c620-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c620-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7c620-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c620-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7c620-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c620-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7c620-127">Header</span><span class="sxs-lookup"><span data-stu-id="7c620-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c620-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="7c620-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c620-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c620-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="7c620-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="7c620-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7c620-131">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="7c620-131">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="7c620-132">**Setclipboardviewer**</span><span class="sxs-lookup"><span data-stu-id="7c620-132">**SetClipboardViewer**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[<span data-ttu-id="7c620-133">**WM \_ CHANGECBCHAIN**</span><span class="sxs-lookup"><span data-stu-id="7c620-133">**WM\_CHANGECBCHAIN**</span></span>](wm-changecbchain.md)
</dt> <dt>

<span data-ttu-id="7c620-134">**Licher**</span><span class="sxs-lookup"><span data-stu-id="7c620-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7c620-135">Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="7c620-135">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

