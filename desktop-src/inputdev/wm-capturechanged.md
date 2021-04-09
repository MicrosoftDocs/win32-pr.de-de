---
title: WM_CAPTURECHANGED Meldung (Winuser. h)
description: Wird an das Fenster gesendet, das die Maus Aufzeichnung verliert.
ms.assetid: 79c8f65e-31fa-4bdb-9e88-0160a52b5b7d
keywords:
- Tastatur-und Maus Eingaben für WM_CAPTURECHANGED Nachricht
topic_type:
- apiref
api_name:
- WM_CAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050bc00a7ab19e22e0fe4ea1f35271707180d4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103406"
---
# <a name="wm_capturechanged-message"></a><span data-ttu-id="43a35-104">WM \_ capturechanged-Meldung</span><span class="sxs-lookup"><span data-stu-id="43a35-104">WM\_CAPTURECHANGED message</span></span>

<span data-ttu-id="43a35-105">Wird an das Fenster gesendet, das die Maus Aufzeichnung verliert.</span><span class="sxs-lookup"><span data-stu-id="43a35-105">Sent to the window that is losing the mouse capture.</span></span>

<span data-ttu-id="43a35-106">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="43a35-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CAPTURECHANGED               0x0215
```



## <a name="parameters"></a><span data-ttu-id="43a35-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="43a35-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43a35-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43a35-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43a35-109">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="43a35-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="43a35-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43a35-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43a35-111">Ein Handle für das Fenster, das die Maus Aufzeichnung erhält.</span><span class="sxs-lookup"><span data-stu-id="43a35-111">A handle to the window gaining the mouse capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43a35-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43a35-112">Return value</span></span>

<span data-ttu-id="43a35-113">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="43a35-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="43a35-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43a35-114">Remarks</span></span>

<span data-ttu-id="43a35-115">Ein Fenster empfängt diese Meldung auch dann, wenn es [**releasecapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) selbst aufruft.</span><span class="sxs-lookup"><span data-stu-id="43a35-115">A window receives this message even if it calls [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) itself.</span></span> <span data-ttu-id="43a35-116">Eine Anwendung sollte nicht versuchen, die Maus Aufzeichnung als Reaktion auf diese Meldung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="43a35-116">An application should not attempt to set the mouse capture in response to this message.</span></span>

<span data-ttu-id="43a35-117">Wenn diese Meldung empfangen wird, sollte sich ein Fenster bei Bedarf selbst neu zeichnen, um den neuen Zustand der Maus Aufzeichnung widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="43a35-117">When it receives this message, a window should redraw itself, if necessary, to reflect the new mouse-capture state.</span></span>

## <a name="requirements"></a><span data-ttu-id="43a35-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43a35-118">Requirements</span></span>



| <span data-ttu-id="43a35-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43a35-119">Requirement</span></span> | <span data-ttu-id="43a35-120">Wert</span><span class="sxs-lookup"><span data-stu-id="43a35-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43a35-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43a35-121">Minimum supported client</span></span><br/> | <span data-ttu-id="43a35-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43a35-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="43a35-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43a35-123">Minimum supported server</span></span><br/> | <span data-ttu-id="43a35-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43a35-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="43a35-125">Header</span><span class="sxs-lookup"><span data-stu-id="43a35-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="43a35-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="43a35-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43a35-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43a35-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="43a35-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="43a35-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="43a35-129">**Releasecapture**</span><span class="sxs-lookup"><span data-stu-id="43a35-129">**ReleaseCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

[<span data-ttu-id="43a35-130">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="43a35-130">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

<span data-ttu-id="43a35-131">**Licher**</span><span class="sxs-lookup"><span data-stu-id="43a35-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="43a35-132">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="43a35-132">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

