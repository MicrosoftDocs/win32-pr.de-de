---
title: WM_SETHOTKEY Meldung (Winuser. h)
description: Wird an ein Fenster gesendet, um dem Fenster einen Hot-Schlüssel zuzuordnen. Wenn der Benutzer die Taste "heiß" drückt, aktiviert das System das Fenster.
ms.assetid: b2c7e6ca-da71-440b-a05e-17f2da419d18
keywords:
- Tastatur-und Maus Eingaben für WM_SETHOTKEY Nachricht
topic_type:
- apiref
api_name:
- WM_SETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ed27a91ddf9506cd12b988db4bd141a988c13e
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "103761514"
---
# <a name="wm_sethotkey-message"></a><span data-ttu-id="90759-105">WM- \_ Nachricht "abkthotkey"</span><span class="sxs-lookup"><span data-stu-id="90759-105">WM\_SETHOTKEY message</span></span>

<span data-ttu-id="90759-106">Wird an ein Fenster gesendet, um dem Fenster einen Hot-Schlüssel zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="90759-106">Sent to a window to associate a hot key with the window.</span></span> <span data-ttu-id="90759-107">Wenn der Benutzer die Taste "heiß" drückt, aktiviert das System das Fenster.</span><span class="sxs-lookup"><span data-stu-id="90759-107">When the user presses the hot key, the system activates the window.</span></span>


```C++
#define WM_SETHOTKEY                    0x0032
```



## <a name="parameters"></a><span data-ttu-id="90759-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="90759-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90759-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="90759-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90759-110">Das nieder wertige Wort gibt den Code des virtuellen Schlüssels an, der dem Fenster zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="90759-110">The low-order word specifies the virtual-key code to associate with the window.</span></span>

<span data-ttu-id="90759-111">Bei dem höchst wertigen Wort kann es sich um einen oder mehrere der folgenden Werte aus "kommctrl. h" handeln.</span><span class="sxs-lookup"><span data-stu-id="90759-111">The high-order word can be one or more of the following values from CommCtrl.h.</span></span>

<span data-ttu-id="90759-112">Wenn Sie *wParam* auf **null** festlegen, wird der einem Fenster zugeordnete "Hot Key" entfernt.</span><span class="sxs-lookup"><span data-stu-id="90759-112">Setting *wParam* to **NULL** removes the hot key associated with a window.</span></span>



| <span data-ttu-id="90759-113">Wert</span><span class="sxs-lookup"><span data-stu-id="90759-113">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="90759-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="90759-114">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="HOTKEYF_ALT"></span><span id="hotkeyf_alt"></span><dl> <span data-ttu-id="90759-115"><dt>**Hotkeyf \_ ALT**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="90759-115"><dt>**HOTKEYF\_ALT**</dt> <dt>0x04</dt></span></span> </dl>             | <span data-ttu-id="90759-116">ALT-TASTE</span><span class="sxs-lookup"><span data-stu-id="90759-116">ALT key</span></span><br/>      |
| <span id="HOTKEYF_CONTROL"></span><span id="hotkeyf_control"></span><dl> <span data-ttu-id="90759-117"><dt>**Hotkeyf \_ Steuer**</dt> Element <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="90759-117"><dt>**HOTKEYF\_CONTROL**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="90759-118">STRG-Taste</span><span class="sxs-lookup"><span data-stu-id="90759-118">CTRL key</span></span><br/>     |
| <span id="HOTKEYF_EXT"></span><span id="hotkeyf_ext"></span><dl> <span data-ttu-id="90759-119"><dt>**Hotkeyf \_ EXT**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="90759-119"><dt>**HOTKEYF\_EXT**</dt> <dt>0x08</dt></span></span> </dl>             | <span data-ttu-id="90759-120">Erweiterter Schlüssel</span><span class="sxs-lookup"><span data-stu-id="90759-120">Extended key</span></span><br/> |
| <span id="HOTKEYF_SHIFT"></span><span id="hotkeyf_shift"></span><dl> <span data-ttu-id="90759-121"><dt>**Hotkeyf \_ UMSCHALT**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="90759-121"><dt>**HOTKEYF\_SHIFT**</dt> <dt>0x01</dt></span></span> </dl>       | <span data-ttu-id="90759-122">Umschalttaste</span><span class="sxs-lookup"><span data-stu-id="90759-122">SHIFT key</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="90759-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90759-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90759-124">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="90759-124">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90759-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90759-125">Return value</span></span>

<span data-ttu-id="90759-126">Der Rückgabewert ist einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="90759-126">The return value is one of the following.</span></span>



| <span data-ttu-id="90759-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90759-127">Return value</span></span>                                                                  | <span data-ttu-id="90759-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90759-128">Description</span></span>                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="90759-129"><dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="90759-129"><dt>-1</dt></span></span> </dl> | <span data-ttu-id="90759-130">Die Funktion ist nicht erfolgreich. die Hot-Taste ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="90759-130">The function is unsuccessful; the hot key is invalid.</span></span><br/>                        |
| <dl> <span data-ttu-id="90759-131"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="90759-131"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="90759-132">Die Funktion ist nicht erfolgreich. Das Fenster ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="90759-132">The function is unsuccessful; the window is invalid.</span></span><br/>                         |
| <dl> <span data-ttu-id="90759-133"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="90759-133"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="90759-134">Die Funktion ist erfolgreich, und kein anderes Fenster hat dieselbe heiße Taste.</span><span class="sxs-lookup"><span data-stu-id="90759-134">The function is successful, and no other window has the same hot key.</span></span><br/>        |
| <dl> <span data-ttu-id="90759-135"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="90759-135"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="90759-136">Die Funktion ist erfolgreich, aber ein anderes Fenster hat bereits dieselbe heiße Taste.</span><span class="sxs-lookup"><span data-stu-id="90759-136">The function is successful, but another window already has the same hot key.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="90759-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90759-137">Remarks</span></span>

<span data-ttu-id="90759-138">Ein "Hot"-Schlüssel kann keinem untergeordneten Fenster zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="90759-138">A hot key cannot be associated with a child window.</span></span>

<span data-ttu-id="90759-139">**VK \_ Escape**, **VK \_ Space** und die **\_ Registerkarte VK** sind ungültige heiße Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="90759-139">**VK\_ESCAPE**, **VK\_SPACE**, and **VK\_TAB** are invalid hot keys.</span></span>

<span data-ttu-id="90759-140">Wenn der Benutzer die Taste "heiß" drückt, generiert das System eine [**WM- \_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Nachricht mit *wParam* -Wert **SC \_ Hotkey** und *LPARAM* gleich dem Handle des Fensters.</span><span class="sxs-lookup"><span data-stu-id="90759-140">When the user presses the hot key, the system generates a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message with *wParam* equal to **SC\_HOTKEY** and *lParam* equal to the window's handle.</span></span> <span data-ttu-id="90759-141">Wenn diese Nachricht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)weitergegeben wird, führt das System das letzte aktive Popup Fenster (sofern vorhanden) oder das Fenster selbst (wenn es kein Popup Fenster gibt) im Vordergrund aus.</span><span class="sxs-lookup"><span data-stu-id="90759-141">If this message is passed on to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the system will bring the window's last active popup (if it exists) or the window itself (if there is no popup window) to the foreground.</span></span>

<span data-ttu-id="90759-142">Ein Fenster kann nur über eine heiße Taste verfügen.</span><span class="sxs-lookup"><span data-stu-id="90759-142">A window can only have one hot key.</span></span> <span data-ttu-id="90759-143">Wenn dem Fenster bereits ein Abkürzungs Schlüssel zugeordnet ist, ersetzt die neue heiße Taste die alte.</span><span class="sxs-lookup"><span data-stu-id="90759-143">If the window already has a hot key associated with it, the new hot key replaces the old one.</span></span> <span data-ttu-id="90759-144">Wenn mehr als ein Fenster die gleiche Abkürzungs Taste hat, ist das Fenster, das von der Hot-Taste aktiviert wird, zufällig.</span><span class="sxs-lookup"><span data-stu-id="90759-144">If more than one window has the same hot key, the window that is activated by the hot key is random.</span></span>

<span data-ttu-id="90759-145">Diese Hotkeys sind nicht mit den von [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)festgelegten Hotkeys verknüpft.</span><span class="sxs-lookup"><span data-stu-id="90759-145">These hot keys are unrelated to the hot keys set by [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey).</span></span>

## <a name="requirements"></a><span data-ttu-id="90759-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90759-146">Requirements</span></span>



| <span data-ttu-id="90759-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90759-147">Requirement</span></span> | <span data-ttu-id="90759-148">Wert</span><span class="sxs-lookup"><span data-stu-id="90759-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90759-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90759-149">Minimum supported client</span></span><br/> | <span data-ttu-id="90759-150">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90759-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="90759-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90759-151">Minimum supported server</span></span><br/> | <span data-ttu-id="90759-152">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90759-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="90759-153">Header</span><span class="sxs-lookup"><span data-stu-id="90759-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="90759-154"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="90759-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90759-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90759-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="90759-156">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="90759-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="90759-157">**RegisterHotKey**</span><span class="sxs-lookup"><span data-stu-id="90759-157">**RegisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[<span data-ttu-id="90759-158">**WM- \_ GetHotKey**</span><span class="sxs-lookup"><span data-stu-id="90759-158">**WM\_GETHOTKEY**</span></span>](wm-gethotkey.md)
</dt> <dt>

[<span data-ttu-id="90759-159">**WM ( \_ syscommand)**</span><span class="sxs-lookup"><span data-stu-id="90759-159">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="90759-160">**Licher**</span><span class="sxs-lookup"><span data-stu-id="90759-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="90759-161">Tastatureingabe</span><span class="sxs-lookup"><span data-stu-id="90759-161">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

