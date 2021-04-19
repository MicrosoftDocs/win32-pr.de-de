---
title: WM_MENUSELECT Meldung (Winuser. h)
description: Wird an das Besitzer Fenster eines Menüs gesendet, wenn der Benutzer ein Menü Element auswählt.
ms.assetid: 57684a19-dfaa-4e0c-a8ff-010533322cb0
keywords:
- WM_MENUSELECT von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_MENUSELECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdee9187ba2074944b3611fee10f5a22c2cc25ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342675"
---
# <a name="wm_menuselect-message"></a><span data-ttu-id="0e5ef-104">WM- \_ MenuSelect-Meldung</span><span class="sxs-lookup"><span data-stu-id="0e5ef-104">WM\_MENUSELECT message</span></span>

<span data-ttu-id="0e5ef-105">Wird an das Besitzer Fenster eines Menüs gesendet, wenn der Benutzer ein Menü Element auswählt.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-105">Sent to a menu's owner window when the user selects a menu item.</span></span>


```C++
#define WM_MENUSELECT                   0x011F
```



## <a name="parameters"></a><span data-ttu-id="0e5ef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e5ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e5ef-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e5ef-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e5ef-108">Das nieder wertige Wort gibt das Menü Element oder den unter Menü Index an.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-108">The low-order word specifies the menu item or submenu index.</span></span> <span data-ttu-id="0e5ef-109">Wenn das ausgewählte Element ein Befehls Element ist, enthält dieser Parameter den Bezeichner des Menü Elements.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-109">If the selected item is a command item, this parameter contains the identifier of the menu item.</span></span> <span data-ttu-id="0e5ef-110">Wenn das ausgewählte Element ein Dropdown Menü oder ein Untermenü öffnet, enthält dieser Parameter den Index des Dropdown Menüs oder des Untermenüs im Hauptmenü, und der *LPARAM* -Parameter enthält das Handle für das Hauptmenü (geklickt). Verwenden Sie die [**getsubmenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) -Funktion, um das Menü Handle im Dropdown Menü oder Untermenü zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-110">If the selected item opens a drop-down menu or submenu, this parameter contains the index of the drop-down menu or submenu in the main menu, and the *lParam* parameter contains the handle to the main (clicked) menu; use the [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) function to get the menu handle to the drop-down menu or submenu.</span></span>

<span data-ttu-id="0e5ef-111">Das höchst wertige Wort gibt mindestens ein menüflags an.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-111">The high-order word specifies one or more menu flags.</span></span> <span data-ttu-id="0e5ef-112">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="0e5ef-113">Wert</span><span class="sxs-lookup"><span data-stu-id="0e5ef-113">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="0e5ef-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0e5ef-114">Meaning</span></span>                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_BITMAP"></span><span id="mf_bitmap"></span><dl> <span data-ttu-id="0e5ef-115"><dt>**MF \_ Bitmap**</dt> <dt>0x00000004l</dt></span><span class="sxs-lookup"><span data-stu-id="0e5ef-115"><dt>**MF\_BITMAP**</dt> <dt>0x00000004L</dt></span></span> </dl>                | <span data-ttu-id="0e5ef-116">Element zeigt eine Bitmap an.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-116">Item displays a bitmap.</span></span><br/>                                                                                                 |
| <span id="MF_CHECKED"></span><span id="mf_checked"></span><dl> <span data-ttu-id="0e5ef-117"><dt>**MF \_**</dt> <dt>0x00000008l</dt> wurde geprüft.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-117"><dt>**MF\_CHECKED**</dt> <dt>0x00000008L</dt></span></span> </dl>             | <span data-ttu-id="0e5ef-118">Das Element ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-118">Item is checked.</span></span><br/>                                                                                                        |
| <span id="MF_DISABLED"></span><span id="mf_disabled"></span><dl> <span data-ttu-id="0e5ef-119"><dt>**MF \_**</dt> <dt>0x00000002l</dt> deaktiviert</span><span class="sxs-lookup"><span data-stu-id="0e5ef-119"><dt>**MF\_DISABLED**</dt> <dt>0x00000002L</dt></span></span> </dl>          | <span data-ttu-id="0e5ef-120">Element ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-120">Item is disabled.</span></span><br/>                                                                                                       |
| <span id="MF_GRAYED"></span><span id="mf_grayed"></span><dl> <span data-ttu-id="0e5ef-121"><dt>**MF \_**</dt>Abgeblendet <dt>0x00000001l</dt></span><span class="sxs-lookup"><span data-stu-id="0e5ef-121"><dt>**MF\_GRAYED**</dt> <dt>0x00000001L</dt></span></span> </dl>                | <span data-ttu-id="0e5ef-122">Das Element ist ausgegraut.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-122">Item is grayed.</span></span><br/>                                                                                                         |
| <span id="MF_HILITE"></span><span id="mf_hilite"></span><dl> <span data-ttu-id="0e5ef-123"><dt>**MF \_ Hilite**</dt> <dt>0x00000080l</dt></span><span class="sxs-lookup"><span data-stu-id="0e5ef-123"><dt>**MF\_HILITE**</dt> <dt>0x00000080L</dt></span></span> </dl>                | <span data-ttu-id="0e5ef-124">Das Element ist hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-124">Item is highlighted.</span></span><br/>                                                                                                    |
| <span id="MF_MOUSESELECT"></span><span id="mf_mouseselect"></span><dl> <span data-ttu-id="0e5ef-125"><dt>**MF \_ Mouseselect**</dt> <dt>0x00008000l</dt></span><span class="sxs-lookup"><span data-stu-id="0e5ef-125"><dt>**MF\_MOUSESELECT**</dt> <dt>0x00008000L</dt></span></span> </dl> | <span data-ttu-id="0e5ef-126">Das Element wird mit der Maus ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-126">Item is selected with the mouse.</span></span><br/>                                                                                        |
| <span id="MF_OWNERDRAW"></span><span id="mf_ownerdraw"></span><dl> <span data-ttu-id="0e5ef-127"><dt>**MF \_ Besitzdraw**</dt> <dt>0x00000100l</dt></span><span class="sxs-lookup"><span data-stu-id="0e5ef-127"><dt>**MF\_OWNERDRAW**</dt> <dt>0x00000100L</dt></span></span> </dl>       | <span data-ttu-id="0e5ef-128">Item ist ein vom Besitzer gezeichnetes Element.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-128">Item is an owner-drawn item.</span></span><br/>                                                                                            |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="0e5ef-129"><dt>**MF \_ Popup**</dt> <dt>0x00000010l</dt></span><span class="sxs-lookup"><span data-stu-id="0e5ef-129"><dt>**MF\_POPUP**</dt> <dt>0x00000010L</dt></span></span> </dl>                   | <span data-ttu-id="0e5ef-130">Element öffnet ein Dropdown Menü oder ein Untermenü.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-130">Item opens a drop-down menu or submenu.</span></span><br/>                                                                                 |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <span data-ttu-id="0e5ef-131"><dt>**MF \_ Sysmenu**</dt> <dt>0x00002000l</dt></span><span class="sxs-lookup"><span data-stu-id="0e5ef-131"><dt>**MF\_SYSMENU**</dt> <dt>0x00002000L</dt></span></span> </dl>             | <span data-ttu-id="0e5ef-132">Das Element ist im Menü Fenster enthalten.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-132">Item is contained in the window menu.</span></span> <span data-ttu-id="0e5ef-133">Der *LPARAM* -Parameter enthält ein Handle für das Menü, das der Nachricht zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-133">The *lParam* parameter contains a handle to the menu associated with the message.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0e5ef-134">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e5ef-134">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e5ef-135">Ein Handle für das Menü, auf das geklickt wurde.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-135">A handle to the menu that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e5ef-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e5ef-136">Return value</span></span>

<span data-ttu-id="0e5ef-137">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e5ef-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e5ef-138">Remarks</span></span>

<span data-ttu-id="0e5ef-139">Wenn das hochwertige Wort von *wParam* den Wert 0xFFFF enthält und der *LPARAM* -Parameter **null** enthält, hat das System das Menü geschlossen.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-139">If the high-order word of *wParam* contains 0xFFFF and the *lParam* parameter contains **NULL**, the system has closed the menu.</span></span>

<span data-ttu-id="0e5ef-140">Verwenden Sie nicht den Wert 1 für das hochwertige Wort von *wParam*, da dieser Wert als (**uint**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-140">Do not use the value  1 for the high-order word of *wParam*, because this value is specified as (**UINT**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*).</span></span> <span data-ttu-id="0e5ef-141">Wenn der Wert 0xFFFF ist, wird er aufgrund der Umwandlung in einen **uint** als 0X0000FFFF, nicht als 1 interpretiert.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-141">If the value is 0xFFFF, it would be interpreted as 0x0000FFFF, not  1, because of the cast to a **UINT**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e5ef-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e5ef-142">Requirements</span></span>



| <span data-ttu-id="0e5ef-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e5ef-143">Requirement</span></span> | <span data-ttu-id="0e5ef-144">Wert</span><span class="sxs-lookup"><span data-stu-id="0e5ef-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e5ef-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0e5ef-145">Minimum supported client</span></span><br/> | <span data-ttu-id="0e5ef-146">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e5ef-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0e5ef-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0e5ef-147">Minimum supported server</span></span><br/> | <span data-ttu-id="0e5ef-148">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e5ef-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0e5ef-149">Header</span><span class="sxs-lookup"><span data-stu-id="0e5ef-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e5ef-150"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="0e5ef-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e5ef-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e5ef-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="0e5ef-152">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="0e5ef-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0e5ef-153">**Getsubmenu**</span><span class="sxs-lookup"><span data-stu-id="0e5ef-153">**GetSubMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)
</dt> <dt>

<span data-ttu-id="0e5ef-154">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0e5ef-154">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="0e5ef-155">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0e5ef-155">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="0e5ef-156">**Licher**</span><span class="sxs-lookup"><span data-stu-id="0e5ef-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0e5ef-157">Tastaturkürzel</span><span class="sxs-lookup"><span data-stu-id="0e5ef-157">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

