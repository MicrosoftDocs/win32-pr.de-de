---
description: Wird gesendet, um bestimmte Modi abzubrechen, z. b. die Maus Aufzeichnung
ms.assetid: c801233a-c4d8-4fd9-aaf0-3d4503bbce26
title: WM_CANCELMODE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23b842dfdfde7dc550d8ec6d942bcc83ea25f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359163"
---
# <a name="wm_cancelmode-message"></a><span data-ttu-id="d6db6-103">WM \_ cancelmode-Meldung</span><span class="sxs-lookup"><span data-stu-id="d6db6-103">WM\_CANCELMODE message</span></span>

<span data-ttu-id="d6db6-104">Wird gesendet, um bestimmte Modi abzubrechen, z. b. die Maus Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="d6db6-104">Sent to cancel certain modes, such as mouse capture.</span></span> <span data-ttu-id="d6db6-105">Das System sendet diese Meldung z. b. an das aktive Fenster, wenn ein Dialogfeld oder ein Meldungs Feld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d6db6-105">For example, the system sends this message to the active window when a dialog box or message box is displayed.</span></span> <span data-ttu-id="d6db6-106">Bestimmte Funktionen senden diese Nachricht auch explizit an das angegebene Fenster, unabhängig davon, ob es sich um das aktive Fenster handelt.</span><span class="sxs-lookup"><span data-stu-id="d6db6-106">Certain functions also send this message explicitly to the specified window regardless of whether it is the active window.</span></span> <span data-ttu-id="d6db6-107">Die [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) -Funktion sendet diese Meldung z. b., wenn das angegebene Fenster deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="d6db6-107">For example, the [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) function sends this message when disabling the specified window.</span></span>

<span data-ttu-id="d6db6-108">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d6db6-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CANCELMODE                   0x001F
```



## <a name="parameters"></a><span data-ttu-id="d6db6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6db6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6db6-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d6db6-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6db6-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d6db6-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d6db6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d6db6-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6db6-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d6db6-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6db6-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6db6-114">Return value</span></span>

<span data-ttu-id="d6db6-115">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="d6db6-115">Type: **LRESULT**</span></span>

<span data-ttu-id="d6db6-116">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d6db6-116">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6db6-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6db6-117">Remarks</span></span>

<span data-ttu-id="d6db6-118">Wenn die **WM \_ cancelmode** -Meldung gesendet wird, bricht die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die interne Verarbeitung der Standardbild Lauf leisten Eingabe ab, bricht die interne Menü Verarbeitung ab und gibt die Maus Aufzeichnung frei.</span><span class="sxs-lookup"><span data-stu-id="d6db6-118">When the **WM\_CANCELMODE** message is sent, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function cancels internal processing of standard scroll bar input, cancels internal menu processing, and releases the mouse capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6db6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6db6-119">Requirements</span></span>



| <span data-ttu-id="d6db6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6db6-120">Requirement</span></span> | <span data-ttu-id="d6db6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d6db6-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6db6-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6db6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d6db6-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6db6-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d6db6-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6db6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d6db6-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6db6-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d6db6-126">Header</span><span class="sxs-lookup"><span data-stu-id="d6db6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6db6-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="d6db6-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6db6-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6db6-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="d6db6-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d6db6-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d6db6-130">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="d6db6-130">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="d6db6-131">**EnableWindow**</span><span class="sxs-lookup"><span data-stu-id="d6db6-131">**EnableWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

[<span data-ttu-id="d6db6-132">**Releasecapture**</span><span class="sxs-lookup"><span data-stu-id="d6db6-132">**ReleaseCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

<span data-ttu-id="d6db6-133">**Licher**</span><span class="sxs-lookup"><span data-stu-id="d6db6-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d6db6-134">Windows</span><span class="sxs-lookup"><span data-stu-id="d6db6-134">Windows</span></span>](windows.md)
</dt> </dl>

 

 
