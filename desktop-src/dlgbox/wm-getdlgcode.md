---
title: WM_GETDLGCODE Meldung (Winuser. h)
description: Wird an die Fenster Prozedur gesendet, die einem Steuerelement zugeordnet ist.
ms.assetid: 96d2caee-be6e-46e9-98b3-bffc3af1c003
keywords:
- Dialog Felder WM_GETDLGCODE Meldung
topic_type:
- apiref
api_name:
- WM_GETDLGCODE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d6e1ddb3be21e227c4dad404a06113f5c50a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337531"
---
# <a name="wm_getdlgcode-message"></a><span data-ttu-id="11797-104">WM \_ getdlgcode-Meldung</span><span class="sxs-lookup"><span data-stu-id="11797-104">WM\_GETDLGCODE message</span></span>

<span data-ttu-id="11797-105">Wird an die Fenster Prozedur gesendet, die einem Steuerelement zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="11797-105">Sent to the window procedure associated with a control.</span></span> <span data-ttu-id="11797-106">Standardmäßig verarbeitet das System alle Tastatureingaben für das Steuerelement. Das System interpretiert bestimmte Typen von Tastatureingaben als Dialogfeld-Navigationstasten.</span><span class="sxs-lookup"><span data-stu-id="11797-106">By default, the system handles all keyboard input to the control; the system interprets certain types of keyboard input as dialog box navigation keys.</span></span> <span data-ttu-id="11797-107">Um dieses Standardverhalten zu überschreiben, kann das-Steuerelement auf die **WM- \_ getdlgcode** -Meldung reagieren, um die Eingabetypen anzugeben, die verarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="11797-107">To override this default behavior, the control can respond to the **WM\_GETDLGCODE** message to indicate the types of input it wants to process itself.</span></span>


```C++
#define WM_GETDLGCODE                   0x0087
```



## <a name="parameters"></a><span data-ttu-id="11797-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="11797-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11797-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="11797-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11797-110">Der vom Benutzer gedrückte virtuelle Schlüssel, der Windows aufgefordert hat, diese Benachrichtigung auszugeben.</span><span class="sxs-lookup"><span data-stu-id="11797-110">The virtual key, pressed by the user, that prompted Windows to issue this notification.</span></span> <span data-ttu-id="11797-111">Der Handler muss diese Schlüssel selektiv verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="11797-111">The handler must selectively handle these keys.</span></span> <span data-ttu-id="11797-112">Beispielsweise kann der Handler die " **VK \_ Return** "-Rückgabe, aber die **\_ Registerkarte "VK** " an das Besitzer Fenster delegieren und verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="11797-112">For instance, the handler might accept and process **VK\_RETURN** but delegate **VK\_TAB** to the owner window.</span></span> <span data-ttu-id="11797-113">Eine Liste der Werte finden Sie unter [**Virtual Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="11797-113">For a list of values, see [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span>

</dd> <dt>

<span data-ttu-id="11797-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="11797-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11797-115">Ein Zeiger auf eine [**msg**](/windows/win32/api/winuser/ns-winuser-msg) -Struktur (oder **null** , wenn das System eine Abfrage ausführt).</span><span class="sxs-lookup"><span data-stu-id="11797-115">A pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure (or **NULL** if the system is performing a query).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11797-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11797-116">Return value</span></span>

<span data-ttu-id="11797-117">Der Rückgabewert ist einer oder mehrere der folgenden Werte, die angeben, welche Art von Eingabe die Anwendung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="11797-117">The return value is one or more of the following values, indicating which type of input the application processes.</span></span>



| <span data-ttu-id="11797-118">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="11797-118">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="11797-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11797-119">Description</span></span>                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11797-120"><dt>**Dlgc \_ Schaltfläche**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="11797-120"><dt>**DLGC\_BUTTON**</dt> <dt>0x2000</dt></span></span> </dl>          | <span data-ttu-id="11797-121">Gedrückt.</span><span class="sxs-lookup"><span data-stu-id="11797-121">Button.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="11797-122"><dt>**Dlgc \_ DEFPUSHBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="11797-122"><dt>**DLGC\_DEFPUSHBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>   | <span data-ttu-id="11797-123">Standard Schaltfläche "Push".</span><span class="sxs-lookup"><span data-stu-id="11797-123">Default push button.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="11797-124"><dt>**Dlgc \_ Hassetsel**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="11797-124"><dt>**DLGC\_HASSETSEL**</dt> <dt>0x0008</dt></span></span> </dl>       | <span data-ttu-id="11797-125">[**EM \_ Nachrichten**](/windows/desktop/Controls/em-setsel) Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="11797-125">[**EM\_SETSEL**](/windows/desktop/Controls/em-setsel) messages.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="11797-126"><dt>**Dlgc \_ RadioButton**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="11797-126"><dt>**DLGC\_RADIOBUTTON**</dt> <dt>0x0040</dt></span></span> </dl>     | <span data-ttu-id="11797-127">Optionsfeld.</span><span class="sxs-lookup"><span data-stu-id="11797-127">Radio button.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="11797-128"><dt>**Dlgc \_ Statisch**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="11797-128"><dt>**DLGC\_STATIC**</dt> <dt>0x0100</dt></span></span> </dl>          | <span data-ttu-id="11797-129">Statisches Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="11797-129">Static control.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="11797-130"><dt>**Dlgc \_ Undefpushbutton**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="11797-130"><dt>**DLGC\_UNDEFPUSHBUTTON**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="11797-131">Nicht standardmäßige pushschaltfläche.</span><span class="sxs-lookup"><span data-stu-id="11797-131">Non-default push button.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="11797-132"><dt>**Dlgc \_ Wantallkeys**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="11797-132"><dt>**DLGC\_WANTALLKEYS**</dt> <dt>0x0004</dt></span></span> </dl>     | <span data-ttu-id="11797-133">Alle Tastatureingaben.</span><span class="sxs-lookup"><span data-stu-id="11797-133">All keyboard input.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="11797-134"><dt>**Dlgc \_ Wantpfeile**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="11797-134"><dt>**DLGC\_WANTARROWS**</dt> <dt>0x0001</dt></span></span> </dl>      | <span data-ttu-id="11797-135">Richtungs Tasten.</span><span class="sxs-lookup"><span data-stu-id="11797-135">Direction keys.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="11797-136"><dt>**Dlgc \_ Wantchars**</dt> <dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="11797-136"><dt>**DLGC\_WANTCHARS**</dt> <dt>0x0080</dt></span></span> </dl>       | <span data-ttu-id="11797-137">[**WM \_ CHAR**](/windows/desktop/inputdev/wm-char) -Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="11797-137">[**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="11797-138"><dt>**Dlgc \_ Wantmessage**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="11797-138"><dt>**DLGC\_WANTMESSAGE**</dt> <dt>0x0004</dt></span></span> </dl>     | <span data-ttu-id="11797-139">Alle Tastatureingaben (die Anwendung übergibt diese Nachricht in der [**msg**](/windows/win32/api/winuser/ns-winuser-msg) -Struktur an das-Steuerelement).</span><span class="sxs-lookup"><span data-stu-id="11797-139">All keyboard input (the application passes this message in the [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure to the control).</span></span><br/> |
| <dl> <span data-ttu-id="11797-140"><dt>**Dlgc \_ Wanttab**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="11797-140"><dt>**DLGC\_WANTTAB**</dt> <dt>0x0002</dt></span></span> </dl>         | <span data-ttu-id="11797-141">Tab-Taste.</span><span class="sxs-lookup"><span data-stu-id="11797-141">TAB key.</span></span><br/>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="11797-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11797-142">Remarks</span></span>

<span data-ttu-id="11797-143">Obwohl die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion immer NULL als Antwort auf die **WM- \_ getdlgcode** -Meldung zurückgibt, gibt die Fenster Prozedur für die vordefinierten Steuerelement Klassen einen für jede Klasse geeigneten Code zurück.</span><span class="sxs-lookup"><span data-stu-id="11797-143">Although the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function always returns zero in response to the **WM\_GETDLGCODE** message, the window procedure for the predefined control classes return a code appropriate for each class.</span></span>

<span data-ttu-id="11797-144">Die " **WM \_ getdlgcode** "-Meldung und die zurückgegebenen Werte sind nur für benutzerdefinierte Dialogfeld Steuerelemente oder Standard Steuerelemente hilfreich, die durch Unterklassen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="11797-144">The **WM\_GETDLGCODE** message and the returned values are useful only with user-defined dialog box controls or standard controls modified by subclassing.</span></span>

## <a name="requirements"></a><span data-ttu-id="11797-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11797-145">Requirements</span></span>



| <span data-ttu-id="11797-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11797-146">Requirement</span></span> | <span data-ttu-id="11797-147">Wert</span><span class="sxs-lookup"><span data-stu-id="11797-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11797-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11797-148">Minimum supported client</span></span><br/> | <span data-ttu-id="11797-149">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11797-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="11797-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11797-150">Minimum supported server</span></span><br/> | <span data-ttu-id="11797-151">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11797-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="11797-152">Header</span><span class="sxs-lookup"><span data-stu-id="11797-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="11797-153"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="11797-153"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11797-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11797-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="11797-155">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="11797-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="11797-156">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="11797-156">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="11797-157">**EM- \_ tsel**</span><span class="sxs-lookup"><span data-stu-id="11797-157">**EM\_SETSEL**</span></span>](/windows/desktop/Controls/em-setsel)
</dt> <dt>

[<span data-ttu-id="11797-158">**Meldung**</span><span class="sxs-lookup"><span data-stu-id="11797-158">**MSG**</span></span>](/windows/win32/api/winuser/ns-winuser-msg)
</dt> <dt>

[<span data-ttu-id="11797-159">**WM \_ -Zeichen**</span><span class="sxs-lookup"><span data-stu-id="11797-159">**WM\_CHAR**</span></span>](/windows/desktop/inputdev/wm-char)
</dt> <dt>

<span data-ttu-id="11797-160">**Licher**</span><span class="sxs-lookup"><span data-stu-id="11797-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="11797-161">Dialog Felder</span><span class="sxs-lookup"><span data-stu-id="11797-161">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

