---
description: Eine Anwendung sendet die WM \_ setredraw-Nachricht an ein Fenster, damit Änderungen in diesem Fenster neu gezeichnet werden können, oder um zu verhindern, dass Änderungen in diesem Fenster neu gezeichnet werden.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: WM_SETREDRAW Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184401e70c8233b03c57db4f8a01bbd6a42e1a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217039"
---
# <a name="wm_setredraw-message"></a><span data-ttu-id="9c8e5-103">WM- \_ Nachricht "abzeichnen"</span><span class="sxs-lookup"><span data-stu-id="9c8e5-103">WM\_SETREDRAW message</span></span>

<span data-ttu-id="9c8e5-104">Eine Anwendung sendet die **WM \_ setredraw** -Nachricht an ein Fenster, damit Änderungen in diesem Fenster neu gezeichnet werden können, oder um zu verhindern, dass Änderungen in diesem Fenster neu gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="9c8e5-104">An application sends the **WM\_SETREDRAW** message to a window to allow changes in that window to be redrawn or to prevent changes in that window from being redrawn.</span></span>

<span data-ttu-id="9c8e5-105">Um diese Nachricht zu senden, wenden Sie die [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="9c8e5-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage( 
  (HWND) hWnd,              
  WM_SETREDRAW,             
  (WPARAM) wParam,          
  (LPARAM) lParam            
);
```



## <a name="parameters"></a><span data-ttu-id="9c8e5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c8e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c8e5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c8e5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c8e5-108">Der neu zeichnen-Zustand.</span><span class="sxs-lookup"><span data-stu-id="9c8e5-108">The redraw state.</span></span> <span data-ttu-id="9c8e5-109">Wenn dieser Parameter **true** ist, kann der Inhalt nach einer Änderung neu gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="9c8e5-109">If this parameter is **TRUE**, the content can be redrawn after a change.</span></span> <span data-ttu-id="9c8e5-110">Wenn dieser Parameter **false** ist, kann der Inhalt nach einer Änderung nicht neu gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="9c8e5-110">If this parameter is **FALSE**, the content cannot be redrawn after a change.</span></span>

</dd> <dt>

<span data-ttu-id="9c8e5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c8e5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c8e5-112">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9c8e5-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c8e5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c8e5-113">Return value</span></span>

<span data-ttu-id="9c8e5-114">Eine Anwendung gibt 0 (null) zurück, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9c8e5-114">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c8e5-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c8e5-115">Remarks</span></span>

<span data-ttu-id="9c8e5-116">Diese Meldung kann nützlich sein, wenn eine Anwendung mehrere Elemente zu einem Listenfeld hinzufügen muss.</span><span class="sxs-lookup"><span data-stu-id="9c8e5-116">This message can be useful if an application must add several items to a list box.</span></span> <span data-ttu-id="9c8e5-117">Die Anwendung kann diese Nachricht mit dem Wert " **false**" von *wParam* abrufen, die Elemente hinzufügen und die Nachricht dann erneut aufzurufen, wobei *wParam* auf " **true**" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9c8e5-117">The application can call this message with *wParam* set to **FALSE**, add the items, and then call the message again with *wParam* set to **TRUE**.</span></span> <span data-ttu-id="9c8e5-118">Zum Schluss kann die Anwendung [**redrawwindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)aufrufen (*HWND*, **null**, **null**, RDW \_ Erase \| RDW- \_ Frame \| RDW \_ Invalidate \| RDW \_ AllChildren), damit das Listenfeld neu gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="9c8e5-118">Finally, the application can call [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **NULL**, **NULL**, RDW\_ERASE \| RDW\_FRAME \| RDW\_INVALIDATE \| RDW\_ALLCHILDREN) to cause the list box to be repainted.</span></span>

> [!Note]  
> <span data-ttu-id="9c8e5-119">Das redrawwindow-Element mit den angegebenen Flags wird anstelle von [**invalidatererenverwendet**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) , da das erste-Steuerelement für einige Steuerelemente erforderlich ist, die nicht über einen Client Bereich verfügen, oder über Fenster Stile verfügen, die bewirken, dass Sie einen nicht-Client Bereich erhalten (z. b. **WS- \_ thickframe** [](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) , **WS \_**-Rahmen oder **WS \_ Ex \_ clientedge**</span><span class="sxs-lookup"><span data-stu-id="9c8e5-119">[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) with the specified flags is used instead of [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) because the former is necessary for some controls that have nonclient area on their own, or have window styles that cause them to be given a nonclient area (such as **WS\_THICKFRAME**, **WS\_BORDER**, or **WS\_EX\_CLIENTEDGE**).</span></span> <span data-ttu-id="9c8e5-120">Wenn das Steuerelement nicht über einen nicht-Client Bereich verfügt, führt **redrawwindow** mit diesen Flags nur so viele ungültige Invalidierung durch wie **invalidaten.**</span><span class="sxs-lookup"><span data-stu-id="9c8e5-120">If the control does not have a nonclient area, **RedrawWindow** with these flags will do only as much invalidation as **InvalidateRect** would.</span></span>

 

<span data-ttu-id="9c8e5-121">Wenn die Anwendung die **WM \_ setredraw** -Nachricht an ein ausgeblendetes Fenster sendet, wird das Fenster sichtbar (d. h., das Betriebssystem fügt dem Fenster das **\_ sichtbare WS** -Format hinzu).</span><span class="sxs-lookup"><span data-stu-id="9c8e5-121">If the application sends the **WM\_SETREDRAW** message to a hidden window, the window becomes visible (that is, the operating system adds the **WS\_VISIBLE** style to the window).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c8e5-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9c8e5-122">Requirements</span></span>



| <span data-ttu-id="9c8e5-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c8e5-123">Requirement</span></span> | <span data-ttu-id="9c8e5-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9c8e5-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c8e5-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9c8e5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9c8e5-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c8e5-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9c8e5-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9c8e5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9c8e5-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c8e5-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9c8e5-129">Header</span><span class="sxs-lookup"><span data-stu-id="9c8e5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c8e5-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="9c8e5-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c8e5-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9c8e5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c8e5-132">Übersicht über das Zeichnen und zeichnen</span><span class="sxs-lookup"><span data-stu-id="9c8e5-132">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="9c8e5-133">Zeichnen und Zeichnen von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="9c8e5-133">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="9c8e5-134">**Redrawwindow**</span><span class="sxs-lookup"><span data-stu-id="9c8e5-134">**RedrawWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> </dl>

 

 
