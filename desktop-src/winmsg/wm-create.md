---
description: Wird gesendet, wenn eine Anwendung anfordert, dass ein Fenster durch Aufrufen der CreateWindowEx-oder CreateWindow-Funktion erstellt wird.
ms.assetid: d484d0fc-bad0-4fcb-bf4b-37cbc50846ee
title: WM_CREATE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37437adbb4df714d7604af59a2abdd11ac9d00a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347483"
---
# <a name="wm_create-message"></a><span data-ttu-id="bfb98-103">WM- \_ Nachricht erstellen</span><span class="sxs-lookup"><span data-stu-id="bfb98-103">WM\_CREATE message</span></span>

<span data-ttu-id="bfb98-104">Wird gesendet, wenn eine Anwendung anfordert, dass ein Fenster durch Aufrufen der [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) -oder [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) -Funktion erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bfb98-104">Sent when an application requests that a window be created by calling the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) or [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function.</span></span> <span data-ttu-id="bfb98-105">(Die Nachricht wird gesendet, bevor die Funktion zurückgegeben wird.) Die Fenster Prozedur des neuen Fensters empfängt diese Meldung, nachdem das Fenster erstellt wurde, aber bevor das Fenster sichtbar wird.</span><span class="sxs-lookup"><span data-stu-id="bfb98-105">(The message is sent before the function returns.) The window procedure of the new window receives this message after the window is created, but before the window becomes visible.</span></span>

<span data-ttu-id="bfb98-106">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="bfb98-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CREATE                       0x0001
```



## <a name="parameters"></a><span data-ttu-id="bfb98-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfb98-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfb98-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bfb98-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfb98-109">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfb98-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bfb98-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bfb98-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfb98-111">Ein Zeiger auf eine [**kreatestruct**](/windows/win32/api/winuser/ns-winuser-createstructa) -Struktur, die Informationen über das Fenster enthält, das erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bfb98-111">A pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure that contains information about the window being created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfb98-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bfb98-112">Return value</span></span>

<span data-ttu-id="bfb98-113">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="bfb98-113">Type: **LRESULT**</span></span>

<span data-ttu-id="bfb98-114">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben, um die Erstellung des Fensters fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="bfb98-114">If an application processes this message, it should return zero to continue creation of the window.</span></span> <span data-ttu-id="bfb98-115">Wenn die Anwendung "– 1" zurückgibt, wird das Fenster zerstört, und die Funktion " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " oder " [**kreatewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) " gibt ein **null** -Handle zurück.</span><span class="sxs-lookup"><span data-stu-id="bfb98-115">If the application returns –1, the window is destroyed and the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) or [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function returns a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfb98-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfb98-116">Requirements</span></span>



| <span data-ttu-id="bfb98-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfb98-117">Requirement</span></span> | <span data-ttu-id="bfb98-118">Wert</span><span class="sxs-lookup"><span data-stu-id="bfb98-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfb98-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bfb98-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bfb98-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfb98-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bfb98-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bfb98-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bfb98-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfb98-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bfb98-123">Header</span><span class="sxs-lookup"><span data-stu-id="bfb98-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfb98-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="bfb98-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfb98-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfb98-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="bfb98-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="bfb98-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bfb98-127">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="bfb98-127">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="bfb98-128">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="bfb98-128">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="bfb98-129">**CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="bfb98-129">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="bfb98-130">**WM- \_ nccreate**</span><span class="sxs-lookup"><span data-stu-id="bfb98-130">**WM\_NCCREATE**</span></span>](wm-nccreate.md)
</dt> <dt>

<span data-ttu-id="bfb98-131">**Licher**</span><span class="sxs-lookup"><span data-stu-id="bfb98-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bfb98-132">Windows</span><span class="sxs-lookup"><span data-stu-id="bfb98-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
