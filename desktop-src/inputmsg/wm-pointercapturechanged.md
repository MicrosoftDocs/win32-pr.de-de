---
title: WM_POINTERCAPTURECHANGED Meldung
description: Wird an ein Fenster gesendet, das die Erfassung eines Eingabe Zeigers verliert.
ms.assetid: 6eec37da-227c-4be1-bf0b-98704caa1322
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_POINTERCAPTURECHANGED Nachricht
topic_type:
- apiref
api_name:
- WM_POINTERCAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 768dc81be57bb61a23acab7ebea450dba577d60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341023"
---
# <a name="wm_pointercapturechanged-message"></a><span data-ttu-id="33543-104">WM_POINTERCAPTURECHANGED Meldung</span><span class="sxs-lookup"><span data-stu-id="33543-104">WM_POINTERCAPTURECHANGED message</span></span>

<span data-ttu-id="33543-105">Wird an ein Fenster gesendet, das die Erfassung eines Eingabe Zeigers verliert.</span><span class="sxs-lookup"><span data-stu-id="33543-105">Sent to a window that is losing capture of an input pointer.</span></span>

<span data-ttu-id="33543-106">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="33543-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_POINTERCAPTURECHANGED           0x024C
```



## <a name="parameters"></a><span data-ttu-id="33543-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="33543-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33543-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33543-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33543-109">Enthält Informationen über den Eingabe Zeiger, der verloren geht.</span><span class="sxs-lookup"><span data-stu-id="33543-109">Contains information about the input pointer that is being lost.</span></span> <span data-ttu-id="33543-110">Verwenden Sie [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) , um die Zeiger-ID zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="33543-110">Use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) to get the pointer ID.</span></span>

</dd> <dt>

<span data-ttu-id="33543-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33543-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33543-112">Enthält ein Handle für das Fenster, das den Eingabe Zeiger erfasst.</span><span class="sxs-lookup"><span data-stu-id="33543-112">Contains a handle to the window that is capturing the input pointer.</span></span> <span data-ttu-id="33543-113">Dieser Wert kann NULL sein, wenn der Zeiger nicht mehr vom Fenster erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="33543-113">This value can be NULL if the pointer is no longer being captured by the window.</span></span>

<span data-ttu-id="33543-114">Wenn diese Meldung aus der internen Verarbeitung generiert wird, kann der Wert das Handle des Fensters sein, in dem die Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="33543-114">If this message is generated from internal processing, the value can be the handle of the window receiving the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33543-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33543-115">Return value</span></span>

<span data-ttu-id="33543-116">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="33543-116">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="33543-117">Wenn die Anwendung diese Nachricht nicht verarbeitet, sollte Sie [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="33543-117">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="33543-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33543-118">Remarks</span></span>

<span data-ttu-id="33543-119">Ein Fenster sollte diese Benachrichtigung verwenden, um die Verarbeitung von nachfolgenden Nachrichten zu unterbinden und alle Bereinigungs Vorgänge zu initiieren, die erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="33543-119">A window should use this notification to stop processing subsequent messages and initiate any cleanup required for the pointer being lost.</span></span> <span data-ttu-id="33543-120">Die Verarbeitung der dem Zeiger zugeordneten Gesten sollte ebenfalls beendet werden (z. b. durch Aufrufen von [**stopinteraktioncontext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)) und verbleibende Kontakte, die dem Fenster erneut zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="33543-120">Processing of gestures associated with the pointer should also be terminated (for example, by calling [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)) and remaining contacts re-associated with the window.</span></span>

<span data-ttu-id="33543-121">Wenn ein Fenster die **WM_POINTERCAPTURECHANGED** Benachrichtigung empfängt, werden in der Regel keine nachfolgenden Benachrichtigungen zum Eingabe Zeiger empfangen.</span><span class="sxs-lookup"><span data-stu-id="33543-121">Typically, if a window receives the **WM_POINTERCAPTURECHANGED** notification, no subsequent notifications related to the input pointer are received.</span></span> <span data-ttu-id="33543-122">Aus diesem Grund hängen nicht von gekoppelten Benachrichtigungen wie [**WM_POINTERENTER**](wm-pointerenter.md) und [**WM_POINTERLEAVE**](wm-pointerleave.md)ab.</span><span class="sxs-lookup"><span data-stu-id="33543-122">Because of this, do not depend on paired notifications such as [**WM_POINTERENTER**](wm-pointerenter.md) and [**WM_POINTERLEAVE**](wm-pointerleave.md).</span></span>

<span data-ttu-id="33543-123">**WM_POINTERCAPTURECHANGED** enthält keine [**POINTER_INFO**](/previous-versions/windows/desktop/api) Daten.</span><span class="sxs-lookup"><span data-stu-id="33543-123">**WM_POINTERCAPTURECHANGED** does not include [**POINTER_INFO**](/previous-versions/windows/desktop/api) data.</span></span> <span data-ttu-id="33543-124">Die von [**getpointerinfo**](/previous-versions/windows/desktop/api) (oder einer beliebigen Variante) zurückgegebenen Daten sind mit denen identisch, die vor der Benachrichtigung zurückgegeben werden. [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md)</span><span class="sxs-lookup"><span data-stu-id="33543-124">Other than the [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) flag being set, the data returned by [**GetPointerInfo**](/previous-versions/windows/desktop/api) (or any variant) is identical to that returned prior to the notification.</span></span>

<span data-ttu-id="33543-125">Wenn diese Benachrichtigung von der Anwendung nicht verarbeitet wird, generiert [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) möglicherweise eine oder mehrere [**WM_GESTURE**](../wintouch/wm-gesture.md) Meldungen, oder wenn eine Geste nicht erkannt wird, generiert **defwindowproc** möglicherweise Maus Eingaben.</span><span class="sxs-lookup"><span data-stu-id="33543-125">If the application does not process this notification, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may generate one or more [**WM_GESTURE**](../wintouch/wm-gesture.md) messages or, if a gesture is not recognized, **DefWindowProc** may generate mouse input.</span></span>

<span data-ttu-id="33543-126">Wenn eine Anwendung selektiv eine Zeiger Eingabe verwendet und den Rest an [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)übergibt, ist das resultierende Verhalten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="33543-126">If an application selectively consumes some pointer input and passes the rest to [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), the resulting behavior is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="33543-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33543-127">Requirements</span></span>



| <span data-ttu-id="33543-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33543-128">Requirement</span></span> | <span data-ttu-id="33543-129">Wert</span><span class="sxs-lookup"><span data-stu-id="33543-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33543-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33543-130">Minimum supported client</span></span><br/> | <span data-ttu-id="33543-131">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33543-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="33543-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33543-132">Minimum supported server</span></span><br/> | <span data-ttu-id="33543-133">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33543-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="33543-134">Header</span><span class="sxs-lookup"><span data-stu-id="33543-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="33543-135"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="33543-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33543-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33543-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33543-137">Meldungen</span><span class="sxs-lookup"><span data-stu-id="33543-137">Messages</span></span>](messages.md)
</dt> </dl>

 

