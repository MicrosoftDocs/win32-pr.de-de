---
description: Die WM- \_ Druck Meldung wird an ein Fenster gesendet, um anzufordern, dass Sie sich im angegebenen Gerätekontext befindet, in der Regel in einem Drucker Gerätekontext.
ms.assetid: e6be2ecd-603a-405f-8a48-68d971e1f6de
title: WM_PRINT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a012d26e4357a639a7eb8d7930937a06a991124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042117"
---
# <a name="wm_print-message"></a><span data-ttu-id="3d7ce-103">WM- \_ Druck Meldung</span><span class="sxs-lookup"><span data-stu-id="3d7ce-103">WM\_PRINT message</span></span>

<span data-ttu-id="3d7ce-104">Die **WM- \_ Druck** Meldung wird an ein Fenster gesendet, um anzufordern, dass Sie sich im angegebenen Gerätekontext befindet, in der Regel in einem Drucker Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-104">The **WM\_PRINT** message is sent to a window to request that it draw itself in the specified device context, most commonly in a printer device context.</span></span>

<span data-ttu-id="3d7ce-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="3d7ce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d7ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d7ce-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3d7ce-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d7ce-108">Ein Handle für den Gerätekontext, in dem gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-108">A handle to the device context to draw in.</span></span>

</dd> <dt>

<span data-ttu-id="3d7ce-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d7ce-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d7ce-110">Die Zeichnungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-110">The drawing options.</span></span> <span data-ttu-id="3d7ce-111">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-111">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="3d7ce-112">Wert</span><span class="sxs-lookup"><span data-stu-id="3d7ce-112">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="3d7ce-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3d7ce-113">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <span data-ttu-id="3d7ce-114"><dt>**PRF \_ checkvisible**</dt></span><span class="sxs-lookup"><span data-stu-id="3d7ce-114"><dt>**PRF\_CHECKVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="3d7ce-115">Zeichnet das Fenster nur, wenn es sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-115">Draws the window only if it is visible.</span></span><br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <span data-ttu-id="3d7ce-116"><dt>**untergeordnete Elemente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d7ce-116"><dt>**PRF\_CHILDREN**</dt></span></span> </dl>             | <span data-ttu-id="3d7ce-117">Zeichnet alle sichtbaren untergeordneten Fenster.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-117">Draws all visible children windows.</span></span><br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <span data-ttu-id="3d7ce-118"><dt>**PRF- \_ Client**</dt></span><span class="sxs-lookup"><span data-stu-id="3d7ce-118"><dt>**PRF\_CLIENT**</dt></span></span> </dl>                   | <span data-ttu-id="3d7ce-119">Zeichnet den Client Bereich des Fensters.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-119">Draws the client area of the window.</span></span><br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <span data-ttu-id="3d7ce-120"><dt>**PRF \_ erasebkgnd**</dt></span><span class="sxs-lookup"><span data-stu-id="3d7ce-120"><dt>**PRF\_ERASEBKGND**</dt></span></span> </dl>       | <span data-ttu-id="3d7ce-121">Löscht den Hintergrund vor dem Zeichnen des Fensters.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-121">Erases the background before drawing the window.</span></span><br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <span data-ttu-id="3d7ce-122"><dt>**PRF- \_ nonclient**</dt></span><span class="sxs-lookup"><span data-stu-id="3d7ce-122"><dt>**PRF\_NONCLIENT**</dt></span></span> </dl>          | <span data-ttu-id="3d7ce-123">Zeichnet den nicht-Client Bereich des Fensters.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-123">Draws the nonclient area of the window.</span></span><br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <span data-ttu-id="3d7ce-124"><dt>**PRF- \_ Besitzer**</dt></span><span class="sxs-lookup"><span data-stu-id="3d7ce-124"><dt>**PRF\_OWNED**</dt></span></span> </dl>                      | <span data-ttu-id="3d7ce-125">Zeichnet alle eigenen Fenster.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-125">Draws all owned windows.</span></span><br/>                         |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d7ce-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d7ce-126">Remarks</span></span>

<span data-ttu-id="3d7ce-127">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion verarbeitet diese Nachricht auf der Grundlage der angegebenen Zeichnungs Option: Wenn PRF \_ checkvisible angegeben und das Fenster nicht sichtbar ist, führen Sie Nothing aus, wenn PRF- \_ nicht angegeben ist, den nicht-Client Bereich im angegebenen Gerätekontext zeichnen. wenn PRF \_ erasebkgnd angegeben ist, senden Sie das Fenster eine [**WM \_ erasebkgnd**](../winmsg/wm-erasebkgnd.md) -Meldung, wenn der PRF- \_ Client angegeben ist, das Fenster eine [**WM \_ printclient**](wm-printclient.md) -Nachricht senden, wenn PRF-untergeordnete \_ Fenster festgelegt ist, jedes sichtbare untergeordnete Fenster an eine **WM- \_ Druck** Nachricht senden, wenn PRF- \_ Besitzer festgelegt ist. **\_**</span><span class="sxs-lookup"><span data-stu-id="3d7ce-127">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function processes this message based on which drawing option is specified: if PRF\_CHECKVISIBLE is specified and the window is not visible, do nothing, if PRF\_NONCLIENT is specified, draw the nonclient area in the specified device context, if PRF\_ERASEBKGND is specified, send the window a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message, if PRF\_CLIENT is specified, send the window a [**WM\_PRINTCLIENT**](wm-printclient.md) message, if PRF\_CHILDREN is set, send each visible child window a **WM\_PRINT** message, if PRF\_OWNED is set, send each visible owned window a **WM\_PRINT** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d7ce-128">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3d7ce-128">Requirements</span></span>



| <span data-ttu-id="3d7ce-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d7ce-129">Requirement</span></span> | <span data-ttu-id="3d7ce-130">Wert</span><span class="sxs-lookup"><span data-stu-id="3d7ce-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d7ce-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d7ce-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3d7ce-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d7ce-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3d7ce-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d7ce-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3d7ce-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d7ce-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3d7ce-135">Header</span><span class="sxs-lookup"><span data-stu-id="3d7ce-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d7ce-136"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="3d7ce-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d7ce-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3d7ce-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d7ce-138">Übersicht über das Zeichnen und zeichnen</span><span class="sxs-lookup"><span data-stu-id="3d7ce-138">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="3d7ce-139">Zeichnen und Zeichnen von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="3d7ce-139">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="3d7ce-140">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="3d7ce-140">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="3d7ce-141">**WM- \_ erasebkgnd**</span><span class="sxs-lookup"><span data-stu-id="3d7ce-141">**WM\_ERASEBKGND**</span></span>](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[<span data-ttu-id="3d7ce-142">**WM- \_ printclient**</span><span class="sxs-lookup"><span data-stu-id="3d7ce-142">**WM\_PRINTCLIENT**</span></span>](wm-printclient.md)
</dt> </dl>

 

 
