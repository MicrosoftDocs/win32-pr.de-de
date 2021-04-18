---
title: WM_CONTEXTMENU Meldung (Winuser. h)
description: Benachrichtigt ein Fenster, dass der Benutzer im Fenster auf die Rechte Maustaste geklickt hat (Rechtsklick).
ms.assetid: e607a61a-0f9b-4d11-b8c0-b01a2e7fb35b
keywords:
- WM_CONTEXTMENU von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_CONTEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7764926709bfc8ab6aa95be330a9d45d38bc48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338142"
---
# <a name="wm_contextmenu-message"></a><span data-ttu-id="68d4f-104">WM- \_ ContextMenu-Meldung</span><span class="sxs-lookup"><span data-stu-id="68d4f-104">WM\_CONTEXTMENU message</span></span>

<span data-ttu-id="68d4f-105">Benachrichtigt ein Fenster, dass der Benutzer ein Kontextmenü anzeigen möchte.</span><span class="sxs-lookup"><span data-stu-id="68d4f-105">Notifies a window that the user desires a context menu to appear.</span></span>  <span data-ttu-id="68d4f-106">Der Benutzer hat möglicherweise im Fenster auf die Rechte Maustaste geklickt (mit der rechten Maustaste geklickt), die UMSCHALTTASTE + F10 gedrückt oder den Anwendungs Schlüssel (Kontextmenü Taste) gedrückt, der auf einigen Tastaturen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="68d4f-106">The user may have clicked the right mouse button (right-clicked) in the window, pressed Shift+F10 or pressed the applications key (context menu key) available on some keyboards.</span></span>


```C++
#define WM_CONTEXTMENU                  0x007B
```



## <a name="parameters"></a><span data-ttu-id="68d4f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="68d4f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68d4f-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="68d4f-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68d4f-109">Ein Handle für das Fenster, in dem der Benutzer mit der rechten Maustaste auf die Maus geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="68d4f-109">A handle to the window in which the user right-clicked the mouse.</span></span> <span data-ttu-id="68d4f-110">Dies kann ein untergeordnetes Fenster des Fensters sein, in dem die Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="68d4f-110">This can be a child window of the window receiving the message.</span></span> <span data-ttu-id="68d4f-111">Weitere Informationen zum Verarbeiten dieser Nachricht finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="68d4f-111">For more information about processing this message, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="68d4f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="68d4f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68d4f-113">Mit dem nieder wertigen Wort wird die horizontale Position des Cursors in Bildschirm Koordinaten zum Zeitpunkt der Mausklicks angegeben.</span><span class="sxs-lookup"><span data-stu-id="68d4f-113">The low-order word specifies the horizontal position of the cursor, in screen coordinates, at the time of the mouse click.</span></span>

<span data-ttu-id="68d4f-114">Das höchst wertige Wort gibt die vertikale Position des Cursors in Bildschirm Koordinaten zum Zeitpunkt der Mausklicks an.</span><span class="sxs-lookup"><span data-stu-id="68d4f-114">The high-order word specifies the vertical position of the cursor, in screen coordinates, at the time of the mouse click.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68d4f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68d4f-115">Return value</span></span>

<span data-ttu-id="68d4f-116">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="68d4f-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68d4f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68d4f-117">Remarks</span></span>

<span data-ttu-id="68d4f-118">Diese Meldung kann von einem Fenster verarbeitet werden, indem ein Kontextmenü mithilfe der [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) -Funktion oder der [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) -Funktion angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="68d4f-118">A window can process this message by displaying a shortcut menu using the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) or [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) functions.</span></span> <span data-ttu-id="68d4f-119">Verwenden Sie den folgenden Code zum Abrufen der horizontalen und vertikalen Positionen.</span><span class="sxs-lookup"><span data-stu-id="68d4f-119">To obtain the horizontal and vertical positions, use the following code.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="68d4f-120">Wenn ein Fenster kein Kontextmenü anzeigt, sollte es diese Meldung an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="68d4f-120">If a window does not display a shortcut menu it should pass this message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="68d4f-121">Wenn es sich bei einem Fenster um ein untergeordnetes Fenster handelt, sendet **defwindowproc** die Nachricht an das übergeordnete Element.</span><span class="sxs-lookup"><span data-stu-id="68d4f-121">If a window is a child window, **DefWindowProc** sends the message to the parent.</span></span> <span data-ttu-id="68d4f-122">Andernfalls zeigt **defwindowproc** ein Standardkontext Menü an, wenn die angegebene Position in der Beschriftung des Fensters angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="68d4f-122">Otherwise, **DefWindowProc** displays a default shortcut menu if the specified position is in the window's caption.</span></span>

<span data-ttu-id="68d4f-123">[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) generiert bei der Verarbeitung der " [**WM \_ rbuttonup**](/windows/desktop/inputdev/wm-rbuttonup) "-oder " [**WM \_ ncrbuttonup**](/windows/desktop/inputdev/wm-ncrbuttonup) "-Meldung die WM-Meldung " **\_ ContextMenu** ", oder wenn der Benutzer UMSCHALT + F10 eingibt.</span><span class="sxs-lookup"><span data-stu-id="68d4f-123">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) generates the **WM\_CONTEXTMENU** message when it processes the [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) or [**WM\_NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) message or when the user types SHIFT+F10.</span></span> <span data-ttu-id="68d4f-124">Die " **WM \_ ContextMenu** "-Meldung wird auch generiert, wenn der Benutzer den Schlüssel " [**VK \_ apps**](/windows/desktop/inputdev/virtual-key-codes) " drückt und freigibt.</span><span class="sxs-lookup"><span data-stu-id="68d4f-124">The **WM\_CONTEXTMENU** message is also generated when the user presses and releases the [**VK\_APPS**](/windows/desktop/inputdev/virtual-key-codes) key.</span></span>

<span data-ttu-id="68d4f-125">Wenn das Kontextmenü z. b. aus der Tastatur generiert wird, wenn der Benutzer UMSCHALT + F10 eingibt, sind die x-und y-Koordinaten-1, und die Anwendung sollte das Kontextmenü an der Position der aktuellen Auswahl anstelle von (xpos, ypos) anzeigen.</span><span class="sxs-lookup"><span data-stu-id="68d4f-125">If the context menu is generated from the keyboard for example, if the user types SHIFT+F10 then the x- and y-coordinates are -1 and the application should display the context menu at the location of the current selection rather than at (xPos, yPos).</span></span>

## <a name="requirements"></a><span data-ttu-id="68d4f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68d4f-126">Requirements</span></span>



| <span data-ttu-id="68d4f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68d4f-127">Requirement</span></span> | <span data-ttu-id="68d4f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="68d4f-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68d4f-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68d4f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="68d4f-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68d4f-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="68d4f-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68d4f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="68d4f-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68d4f-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="68d4f-133">Header</span><span class="sxs-lookup"><span data-stu-id="68d4f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="68d4f-134"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="68d4f-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68d4f-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68d4f-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="68d4f-136">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="68d4f-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="68d4f-137">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="68d4f-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="68d4f-138">**GET \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="68d4f-138">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="68d4f-139">**\_Y- \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="68d4f-139">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="68d4f-140">**TrackPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="68d4f-140">**TrackPopupMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)
</dt> <dt>

[<span data-ttu-id="68d4f-141">**TrackPopupMenuEx**</span><span class="sxs-lookup"><span data-stu-id="68d4f-141">**TrackPopupMenuEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)
</dt> <dt>

[<span data-ttu-id="68d4f-142">**WM- \_ ncrbuttonup**</span><span class="sxs-lookup"><span data-stu-id="68d4f-142">**WM\_NCRBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-ncrbuttonup)
</dt> <dt>

[<span data-ttu-id="68d4f-143">**WM- \_ rbuttonup**</span><span class="sxs-lookup"><span data-stu-id="68d4f-143">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)
</dt> <dt>

<span data-ttu-id="68d4f-144">**Licher**</span><span class="sxs-lookup"><span data-stu-id="68d4f-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="68d4f-145">Menüs</span><span class="sxs-lookup"><span data-stu-id="68d4f-145">Menus</span></span>](menus.md)
</dt> </dl>

 

