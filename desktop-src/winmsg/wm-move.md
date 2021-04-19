---
description: Wird gesendet, nachdem ein Fenster verschoben wurde.
ms.assetid: 552ddc26-fe63-449b-8c82-bb927a2c1c41
title: WM_MOVE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56004ec47266a50bf2ac82a828b9046c84a8ebfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363480"
---
# <a name="wm_move-message"></a><span data-ttu-id="964bb-103">WM-Verschiebungs \_ Meldung</span><span class="sxs-lookup"><span data-stu-id="964bb-103">WM\_MOVE message</span></span>

<span data-ttu-id="964bb-104">Wird gesendet, nachdem ein Fenster verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="964bb-104">Sent after a window has been moved.</span></span>

<span data-ttu-id="964bb-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="964bb-105">A window receives this message through its [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>


```C++
#define WM_MOVE                         0x0003
```



## <a name="parameters"></a><span data-ttu-id="964bb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="964bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="964bb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="964bb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="964bb-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="964bb-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="964bb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="964bb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="964bb-110">Die x-und y-Koordinaten der oberen linken Ecke des Client Bereichs des Fensters.</span><span class="sxs-lookup"><span data-stu-id="964bb-110">The x and y coordinates of the upper-left corner of the client area of the window.</span></span> <span data-ttu-id="964bb-111">Das nieder wertige Wort enthält die x-Koordinate, während das Haupt Wort die y-Koordinate enthält.</span><span class="sxs-lookup"><span data-stu-id="964bb-111">The low-order word contains the x-coordinate while the high-order word contains the y coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="964bb-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="964bb-112">Return value</span></span>

<span data-ttu-id="964bb-113">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="964bb-113">Type: **LRESULT**</span></span>

<span data-ttu-id="964bb-114">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="964bb-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="964bb-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="964bb-115">Remarks</span></span>

<span data-ttu-id="964bb-116">Die Parameter werden in Bildschirm Koordinaten für überlappende und Popup Fenster sowie in den übergeordneten Client Koordinaten für untergeordnete Fenster angegeben.</span><span class="sxs-lookup"><span data-stu-id="964bb-116">The parameters are given in screen coordinates for overlapped and pop-up windows and in parent-client coordinates for child windows.</span></span>

<span data-ttu-id="964bb-117">Im folgenden Beispiel wird veranschaulicht, wie die Position aus dem *LPARAM* -Parameter abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="964bb-117">The following example demonstrates how to obtain the position from the *lParam* parameter.</span></span>


```
xPos = (int)(short) LOWORD(lParam);   // horizontal position 
yPos = (int)(short) HIWORD(lParam);   // vertical position 
```



<span data-ttu-id="964bb-118">Sie können auch das [**makepoints**](/windows/win32/api/wingdi/nf-wingdi-makepoints) -Makro verwenden, um den *LPARAM* -Parameter in eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="964bb-118">You can also use the [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) macro to convert the *lParam* parameter to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure.</span></span>

<span data-ttu-id="964bb-119">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion sendet die **WM- \_ Größe** und die WM-Verschiebungs Nachricht, wenn Sie die [**WM- \_ windowposchge**](wm-windowposchanged.md) -Nachricht verarbeitet. **\_**</span><span class="sxs-lookup"><span data-stu-id="964bb-119">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the **WM\_SIZE** and **WM\_MOVE** messages when it processes the [**WM\_WINDOWPOSCHANGED**](wm-windowposchanged.md) message.</span></span>
<span data-ttu-id="964bb-120">Die **WM- \_ Größe** und die WM-Verschiebungs Nachricht werden nicht gesendet, wenn eine Anwendung die **WM- \_ windowposchangsnachricht** verarbeitet, ohne **defwindowproc** Aufrufs. **\_**</span><span class="sxs-lookup"><span data-stu-id="964bb-120">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="964bb-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="964bb-121">Requirements</span></span>



| <span data-ttu-id="964bb-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="964bb-122">Requirement</span></span> | <span data-ttu-id="964bb-123">Wert</span><span class="sxs-lookup"><span data-stu-id="964bb-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="964bb-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="964bb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="964bb-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="964bb-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="964bb-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="964bb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="964bb-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="964bb-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="964bb-128">Header</span><span class="sxs-lookup"><span data-stu-id="964bb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="964bb-129"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="964bb-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="964bb-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="964bb-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="964bb-131">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="964bb-131">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="964bb-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="964bb-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="964bb-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="964bb-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="964bb-134">**WM-Windows-Server \_**</span><span class="sxs-lookup"><span data-stu-id="964bb-134">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="964bb-135">**Licher**</span><span class="sxs-lookup"><span data-stu-id="964bb-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="964bb-136">Windows</span><span class="sxs-lookup"><span data-stu-id="964bb-136">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="964bb-137">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="964bb-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="964bb-138">**Makepoints**</span><span class="sxs-lookup"><span data-stu-id="964bb-138">**MAKEPOINTS**</span></span>](/windows/win32/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="964bb-139">[**Punkt**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="964bb-139">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

 
