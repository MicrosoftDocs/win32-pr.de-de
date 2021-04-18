---
title: WM_NCMOUSELEAVE Meldung (Winuser. h)
description: Wird an ein Fenster gesendet, wenn der Cursor den nicht-Client Bereich des Fensters verlässt, das in einem vorherigen Befehl von trackmouserevent angegeben wurde.
ms.assetid: b3ada6db-93ce-45d7-b408-d08692328aeb
keywords:
- Tastatur-und Maus Eingaben für WM_NCMOUSELEAVE Nachricht
topic_type:
- apiref
api_name:
- WM_NCMOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf7f9d0931c2623d2e92010abfca96f391107b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341374"
---
# <a name="wm_ncmouseleave-message"></a><span data-ttu-id="b95d2-104">WM- \_ ncmouseleave-Nachricht</span><span class="sxs-lookup"><span data-stu-id="b95d2-104">WM\_NCMOUSELEAVE message</span></span>

<span data-ttu-id="b95d2-105">Wird an ein Fenster gesendet, wenn der Cursor den nicht-Client Bereich des Fensters verlässt, das in einem vorherigen Befehl von [**trackmouserevent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b95d2-105">Posted to a window when the cursor leaves the nonclient area of the window specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="b95d2-106">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b95d2-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMOUSELEAVE                 0x02A2
```



## <a name="parameters"></a><span data-ttu-id="b95d2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b95d2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b95d2-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b95d2-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b95d2-109">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b95d2-109">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b95d2-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b95d2-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b95d2-111">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b95d2-111">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b95d2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b95d2-112">Return value</span></span>

<span data-ttu-id="b95d2-113">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b95d2-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b95d2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b95d2-114">Remarks</span></span>

<span data-ttu-id="b95d2-115">Wenn diese Meldung generiert wird, wird die gesamte von [**trackmouserevent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) angeforderte Überwachung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="b95d2-115">All tracking requested by [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) is canceled when this message is generated.</span></span> <span data-ttu-id="b95d2-116">Die Anwendung muss **TrackMouseEvent** aufrufen, wenn der Mauszeiger wieder in das Fenster wechselt, wenn Sie das Verhalten der Mausbewegung weiter verfolgen muss.</span><span class="sxs-lookup"><span data-stu-id="b95d2-116">The application must call **TrackMouseEvent** when the mouse reenters its window if it requires further tracking of mouse hover behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="b95d2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b95d2-117">Requirements</span></span>



| <span data-ttu-id="b95d2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b95d2-118">Requirement</span></span> | <span data-ttu-id="b95d2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b95d2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b95d2-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b95d2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b95d2-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b95d2-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b95d2-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b95d2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b95d2-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b95d2-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b95d2-124">Header</span><span class="sxs-lookup"><span data-stu-id="b95d2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b95d2-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="b95d2-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b95d2-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b95d2-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b95d2-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="b95d2-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b95d2-128">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="b95d2-128">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="b95d2-129">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="b95d2-129">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="b95d2-130">**WM ( \_ syscommand)**</span><span class="sxs-lookup"><span data-stu-id="b95d2-130">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[<span data-ttu-id="b95d2-131">**WM- \_ MouseLeave**</span><span class="sxs-lookup"><span data-stu-id="b95d2-131">**WM\_MOUSELEAVE**</span></span>](wm-mouseleave.md)
</dt> <dt>

<span data-ttu-id="b95d2-132">**Licher**</span><span class="sxs-lookup"><span data-stu-id="b95d2-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b95d2-133">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="b95d2-133">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

