---
description: Sie senden die **WM_SETREDRAW** an ein Fenster, damit Änderungen in diesem Fenster neu gezeichnet werden können, oder um zu verhindern, dass Änderungen in diesem Fenster neu gezeichnet werden.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: WM_SETREDRAW (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1232833fc4465e2341541a0036af47fdd3b53393
ms.sourcegitcommit: e5d6fb49928cc8cea4ec77dce03b740d40076348
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/10/2021
ms.locfileid: "113593456"
---
# <a name="wm_setredraw-message"></a><span data-ttu-id="88fc8-103">WM_SETREDRAW</span><span class="sxs-lookup"><span data-stu-id="88fc8-103">WM_SETREDRAW message</span></span>

<span data-ttu-id="88fc8-104">Sie senden die **WM \_ SETREDRAW-Nachricht** an ein Fenster, um zu ermöglichen, dass Änderungen in diesem Fenster neu gezeichnet werden, oder um zu verhindern, dass Änderungen in diesem Fenster neu gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="88fc8-104">You send the **WM\_SETREDRAW** message to a window to allow changes in that window to be redrawn, or to prevent changes in that window from being redrawn.</span></span>

<span data-ttu-id="88fc8-105">Um diese Nachricht zu senden, rufen Sie die [**SendMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-sendmessage) mit den folgenden Parametern auf.</span><span class="sxs-lookup"><span data-stu-id="88fc8-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>

```C++
SendMessage(
  (HWND) hWnd,
  WM_SETREDRAW,
  (WPARAM) wParam,
  (LPARAM) lParam
);
```

## <a name="parameters"></a><span data-ttu-id="88fc8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="88fc8-106">Parameters</span></span>

`wParam`

<span data-ttu-id="88fc8-107">Der neu gezeichnete Zustand.</span><span class="sxs-lookup"><span data-stu-id="88fc8-107">The redraw state.</span></span> <span data-ttu-id="88fc8-108">Wenn dieser Parameter **TRUE ist,** kann der Inhalt nach einer Änderung neu gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="88fc8-108">If this parameter is **TRUE**, then the content can be redrawn after a change.</span></span> <span data-ttu-id="88fc8-109">Wenn dieser Parameter **FALSE ist,** kann der Inhalt nach einer Änderung nicht neu gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="88fc8-109">If this parameter is **FALSE**, then the content can't be redrawn after a change.</span></span>

`lParam`

<span data-ttu-id="88fc8-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="88fc8-110">This parameter isn't used.</span></span>

## <a name="return-value"></a><span data-ttu-id="88fc8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88fc8-111">Return value</span></span>

<span data-ttu-id="88fc8-112">Ihre Anwendung sollte 0 zurückgeben, wenn sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="88fc8-112">Your application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="88fc8-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88fc8-113">Remarks</span></span>

<span data-ttu-id="88fc8-114">Diese Meldung kann nützlich sein, wenn Ihre Anwendung einem Listenfeld mehrere Elemente hinzufügen muss.</span><span class="sxs-lookup"><span data-stu-id="88fc8-114">This message can be useful if your application must add several items to a list box.</span></span> <span data-ttu-id="88fc8-115">Ihre Anwendung kann diese Nachricht aufrufen, bei der *wParam* auf **FALSE** festgelegt ist, die Elemente hinzufügen und die Nachricht dann erneut aufrufen, während *wParam* auf **TRUE festgelegt ist.**</span><span class="sxs-lookup"><span data-stu-id="88fc8-115">Your application can call this message with *wParam* set to **FALSE**, add the items, and then call the message again with *wParam* set to **TRUE**.</span></span> <span data-ttu-id="88fc8-116">Schließlich kann Ihre Anwendung [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **NULL**, **NULL**, RDW \_ ERASE \| RDW FRAME \_ \| RDW \_ INVALIDATE \| RDW ALLCHILDREN) \_ aufrufen, damit das Listenfeld neu gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="88fc8-116">Finally, your application can call [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **NULL**, **NULL**, RDW\_ERASE \| RDW\_FRAME \| RDW\_INVALIDATE \| RDW\_ALLCHILDREN) to cause the list box to be repainted.</span></span>

> [!NOTE] 
> <span data-ttu-id="88fc8-117">Sie sollten [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) mit den angegebenen Flags anstelle von [**InvalidateRect**](/windows/win32/api/Winuser/nf-winuser-invalidaterect)verwenden, da ersteres für einige Steuerelemente erforderlich ist, die einen eigenen Nichtclientbereich haben, oder über Fensterstile verfügen, die dazu führen, dass ihnen ein Nichtclientbereich (z. B. **WS_THICKFRAME,** **WS_BORDER oder** **WS_EX_CLIENTEDGE) erteilt wird.**</span><span class="sxs-lookup"><span data-stu-id="88fc8-117">You should use [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) with the specified flags, instead of [**InvalidateRect**](/windows/win32/api/Winuser/nf-winuser-invalidaterect), because the former is necessary for some controls that have nonclient area of their own, or have window styles that cause them to be given a nonclient area (such as **WS_THICKFRAME**, **WS_BORDER**, or **WS_EX_CLIENTEDGE**).</span></span> <span data-ttu-id="88fc8-118">Wenn das Steuerelement nicht über einen Nichtclientbereich verfügt, führt **RedrawWindow** mit diesen Flags nur so viel Ungültigkeit wie **InvalidateRect** durch.</span><span class="sxs-lookup"><span data-stu-id="88fc8-118">If the control does not have a nonclient area, then **RedrawWindow** with these flags will do only as much invalidation as **InvalidateRect** would.</span></span>

<span data-ttu-id="88fc8-119">Durch übergeben **WM_SETREDRAW** meldung an die **DefWindowProc-Funktion** wird der WS_VISIBLE aus dem Fenster entfernt, wenn *wParam* auf **FALSE festgelegt ist.** </span><span class="sxs-lookup"><span data-stu-id="88fc8-119">Passing a **WM_SETREDRAW** message to the **DefWindowProc** function removes the **WS_VISIBLE** style from the window when *wParam* is set to **FALSE**.</span></span> <span data-ttu-id="88fc8-120">Obwohl der Fensterinhalt auf dem Bildschirm sichtbar bleibt, gibt die [**IsWindowVisible-Funktion**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) **FALSE** zurück, wenn sie in einem Fenster in diesem Zustand aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="88fc8-120">Although the window content remains visible on screen, the [**IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) function returns **FALSE** when called on a window in this state.</span></span> 

<span data-ttu-id="88fc8-121">Durch übergeben **WM_SETREDRAW** meldung an die **DefWindowProc-Funktion** wird dem Fenster der WS_VISIBLE-Stil hinzufügt, sofern nicht festgelegt, wenn *wParam* auf **TRUE festgelegt ist.** </span><span class="sxs-lookup"><span data-stu-id="88fc8-121">Passing a **WM_SETREDRAW** message to the **DefWindowProc** function adds the **WS_VISIBLE** style to the window, if not set, when *wParam* is set to **TRUE**.</span></span> <span data-ttu-id="88fc8-122">Wenn Ihre Anwendung  die WM_SETREDRAW-Nachricht sendet, bei der *wParam* auf **TRUE** festgelegt ist, wird das Fenster sichtbar.</span><span class="sxs-lookup"><span data-stu-id="88fc8-122">If your application sends the **WM_SETREDRAW** message with *wParam* set to **TRUE** to a hidden window, then the window becomes visible.</span></span> 

<span data-ttu-id="88fc8-123">**Windows 10 und höher; Windows Server 2016 und höher.**</span><span class="sxs-lookup"><span data-stu-id="88fc8-123">**Windows 10 and later; Windows Server 2016 and later**.</span></span> <span data-ttu-id="88fc8-124">Das System legt eine Eigenschaft namens *SysSetRedraw*  für ein Fenster fest, dessen Fensterprozedur WM_SETREDRAW an **DefWindowProc übergibt.**</span><span class="sxs-lookup"><span data-stu-id="88fc8-124">The system sets a property named *SysSetRedraw* on a window whose window procedure passes **WM_SETREDRAW** messages to **DefWindowProc**.</span></span> <span data-ttu-id="88fc8-125">Sie können die [**GetProp-Funktion**](/windows/win32/api/Winuser/nf-winuser-getpropa) verwenden, um den Eigenschaftswert zu erhalten, wenn er verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="88fc8-125">You can use the [**GetProp**](/windows/win32/api/Winuser/nf-winuser-getpropa) function to get the property value when it's available.</span></span> <span data-ttu-id="88fc8-126">**GetProp gibt** einen Wert zurück, der nicht 0 (null) ist, wenn das Neuzeichneten deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="88fc8-126">**GetProp** returns a non-zero value when redraw is disabled.</span></span> <span data-ttu-id="88fc8-127">**GetProp** gibt 0 (null) zurück, wenn das neu gezeichnete Fenster aktiviert ist oder die Fenstereigenschaft nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="88fc8-127">**GetProp** will return zero when redraw is enabled, or when the window property doesn't exist.</span></span> 

## <a name="requirements"></a><span data-ttu-id="88fc8-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88fc8-128">Requirements</span></span>

| <span data-ttu-id="88fc8-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88fc8-129">Requirement</span></span> | <span data-ttu-id="88fc8-130">Wert</span><span class="sxs-lookup"><span data-stu-id="88fc8-130">Value</span></span> |
|-|-|
| <span data-ttu-id="88fc8-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88fc8-131">Minimum supported client</span></span> | <span data-ttu-id="88fc8-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88fc8-132">Windows 2000 Professional \[desktop apps only\]</span></span> |
| <span data-ttu-id="88fc8-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88fc8-133">Minimum supported server</span></span> | <span data-ttu-id="88fc8-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88fc8-134">Windows 2000 Server \[desktop apps only\]</span></span> |
| <span data-ttu-id="88fc8-135">Header</span><span class="sxs-lookup"><span data-stu-id="88fc8-135">Header</span></span> | <dl><span data-ttu-id="88fc8-136"><dt>Winuser.h (include Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="88fc8-136"><dt>Winuser.h (include Windows.h)</dt></span></span></dl> |

## <a name="see-also"></a><span data-ttu-id="88fc8-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="88fc8-137">See also</span></span>

* [<span data-ttu-id="88fc8-138">Übersicht über Das Zeichnen und Zeichnen</span><span class="sxs-lookup"><span data-stu-id="88fc8-138">Painting and drawing overview</span></span>](painting-and-drawing.md)
* [<span data-ttu-id="88fc8-139">Zeichnen und Zeichnen von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="88fc8-139">Painting and drawing messages</span></span>](painting-and-drawing-messages.md)
* [<span data-ttu-id="88fc8-140">RedrawWindow</span><span class="sxs-lookup"><span data-stu-id="88fc8-140">RedrawWindow</span></span>](/windows/win32/api/Winuser/nf-winuser-redrawwindow)
