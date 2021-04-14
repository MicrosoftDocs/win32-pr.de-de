---
title: WM_MOUSELEAVE Meldung (Winuser. h)
description: Wird an ein Fenster gesendet, wenn der Cursor den Client Bereich des Fensters verlässt, das in einem vorherigen Befehl von trackmouserevent angegeben wurde.
ms.assetid: b23d24ff-531a-4b6d-8848-f82ac5568995
keywords:
- Tastatur-und Maus Eingaben für WM_MOUSELEAVE Nachricht
topic_type:
- apiref
api_name:
- WM_MOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc96022e94df7f518b21b1c9a46895fc9204b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476143"
---
# <a name="wm_mouseleave-message"></a><span data-ttu-id="e0157-104">WM- \_ MouseLeave-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e0157-104">WM\_MOUSELEAVE message</span></span>

<span data-ttu-id="e0157-105">Wird an ein Fenster gesendet, wenn der Cursor den Client Bereich des Fensters verlässt, das in einem vorherigen Befehl von [**trackmouserevent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="e0157-105">Posted to a window when the cursor leaves the client area of the window specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="e0157-106">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e0157-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSELEAVE                   0x02A3
```



## <a name="parameters"></a><span data-ttu-id="e0157-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0157-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0157-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e0157-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0157-109">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="e0157-109">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e0157-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0157-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0157-111">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="e0157-111">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0157-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0157-112">Return value</span></span>

<span data-ttu-id="e0157-113">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e0157-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0157-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0157-114">Remarks</span></span>

<span data-ttu-id="e0157-115">Wenn diese Meldung generiert wird, wird die gesamte von [**trackmouserevent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) angeforderte Überwachung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="e0157-115">All tracking requested by [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) is canceled when this message is generated.</span></span> <span data-ttu-id="e0157-116">Die Anwendung muss **TrackMouseEvent** aufrufen, wenn der Mauszeiger wieder in das Fenster wechselt, wenn Sie das Verhalten der Mausbewegung weiter verfolgen muss.</span><span class="sxs-lookup"><span data-stu-id="e0157-116">The application must call **TrackMouseEvent** when the mouse reenters its window if it requires further tracking of mouse hover behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0157-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0157-117">Requirements</span></span>



| <span data-ttu-id="e0157-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0157-118">Requirement</span></span> | <span data-ttu-id="e0157-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e0157-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0157-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0157-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e0157-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0157-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e0157-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0157-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e0157-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0157-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e0157-124">Header</span><span class="sxs-lookup"><span data-stu-id="e0157-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0157-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="e0157-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0157-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0157-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="e0157-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="e0157-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e0157-128">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="e0157-128">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="e0157-129">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="e0157-129">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="e0157-130">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="e0157-130">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="e0157-131">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="e0157-131">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="e0157-132">**WM- \_ ncmouseleave**</span><span class="sxs-lookup"><span data-stu-id="e0157-132">**WM\_NCMOUSELEAVE**</span></span>](wm-ncmouseleave.md)
</dt> <dt>

<span data-ttu-id="e0157-133">**Licher**</span><span class="sxs-lookup"><span data-stu-id="e0157-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e0157-134">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="e0157-134">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

