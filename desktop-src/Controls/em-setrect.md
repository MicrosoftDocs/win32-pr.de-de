---
title: EM_SETRECT (Winuser.h)
description: 'EM_SETRECT Meldung: Legt das Formatierungsrechteck eines mehrzweckigen Bearbeitungssteuer steuerelements fest.'
ms.assetid: 4f576e94-3bd3-4416-a960-b7f22da963ea
keywords:
- EM_SETRECT Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- EM_SETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042428a236b8e9a23f03cdcceaf5d76eb977efd8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085968"
---
# <a name="em_setrect-message"></a><span data-ttu-id="5c7cb-104">EM \_ SETRECT-Nachricht</span><span class="sxs-lookup"><span data-stu-id="5c7cb-104">EM\_SETRECT message</span></span>

<span data-ttu-id="5c7cb-105">Legt das [Formatierungsrechteck eines](about-edit-controls.md) mehrzweckigen Bearbeitungssteuer steuerelements fest.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-105">Sets the [formatting rectangle](about-edit-controls.md) of a multiline edit control.</span></span> <span data-ttu-id="5c7cb-106">Das Formatierungrechteck ist das einschränkende Rechteck, in das das Steuerelement den Text zeichnet.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-106">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="5c7cb-107">Das einschränkende Rechteck ist unabhängig von der Größe des Bearbeitungssteuerfensters.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-107">The limiting rectangle is independent of the size of the edit control window.</span></span>

<span data-ttu-id="5c7cb-108">Diese Meldung wird nur von mehrline-Bearbeitungssteuerelementen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-108">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="5c7cb-109">Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5c7cb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c7cb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c7cb-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5c7cb-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c7cb-112">**Rich Edit 2.0 und höher:** Gibt an, *ob lParam* absolute oder relative Koordinaten angibt.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-112">**Rich Edit 2.0 and later:** Indicates whether *lParam* specifies absolute or relative coordinates.</span></span> <span data-ttu-id="5c7cb-113">Der Wert 0 (null) gibt absolute Koordinaten an.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-113">A value of zero indicates absolute coordinates.</span></span> <span data-ttu-id="5c7cb-114">Der Wert 1 gibt Offsets relativ zum aktuellen Formatierungsrechteck an.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-114">A value of 1 indicates offsets relative to the current formatting rectangle.</span></span> <span data-ttu-id="5c7cb-115">(Die Offsets können positiv oder negativ sein.)</span><span class="sxs-lookup"><span data-stu-id="5c7cb-115">(The offsets can be positive or negative.)</span></span>

<span data-ttu-id="5c7cb-116">**Steuerelemente bearbeiten und Rich Edit 1.0:** Dieser Parameter wird nicht verwendet und muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-116">**Edit controls and Rich Edit 1.0:** This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5c7cb-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5c7cb-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c7cb-118">Ein Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die die neuen Dimensionen des Rechtecks angibt.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-118">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the new dimensions of the rectangle.</span></span> <span data-ttu-id="5c7cb-119">Wenn dieser Parameter **NULL ist,** wird das Formatierungsrechteck auf seine Standardwerte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-119">If this parameter is **NULL**, the formatting rectangle is set to its default values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c7cb-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c7cb-120">Return value</span></span>

<span data-ttu-id="5c7cb-121">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-121">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c7cb-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c7cb-122">Remarks</span></span>

<span data-ttu-id="5c7cb-123">Das *Festlegen von lParam* auf **NULL** hat keine Auswirkungen, wenn ein Touchgerät installiert ist oder **EM \_ SETRECT** von einem Thread gesendet wird, auf dem ein Hook installiert ist (siehe [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)).</span><span class="sxs-lookup"><span data-stu-id="5c7cb-123">Setting *lParam* to **NULL** has no effect if a touch device is installed, or if **EM\_SETRECT** is sent from a thread that has a hook installed (see [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)).</span></span> <span data-ttu-id="5c7cb-124">In diesen Fällen sollte *lParam* einen gültigen Zeiger auf eine [**RECT-Struktur**](/previous-versions//dd162897(v=vs.85)) enthalten.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-124">In these cases, *lParam* should contain a valid pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span>

<span data-ttu-id="5c7cb-125">Die **EM \_ SETRECT-Meldung** bewirkt, dass der Text des Bearbeitungssteuerfelds neu gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-125">The **EM\_SETRECT** message causes the text of the edit control to be redrawn.</span></span> <span data-ttu-id="5c7cb-126">Verwenden Sie die [**EM \_ SETRECTNP-Meldung,**](em-setrectnp.md) um die Größe des Formatierungsrechtecks zu ändern, ohne den Text neu zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-126">To change the size of the formatting rectangle without redrawing the text, use the [**EM\_SETRECTNP**](em-setrectnp.md) message.</span></span>

<span data-ttu-id="5c7cb-127">Wenn ein Bearbeitungssteuerelement zum ersten Mal erstellt wird, wird das Formatierungsrechteck auf eine Standardgröße festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-127">When an edit control is first created, the formatting rectangle is set to a default size.</span></span> <span data-ttu-id="5c7cb-128">Sie können die **EM \_ SETRECT-Nachricht** verwenden, um das Formatierungsrechteck größer oder kleiner als das Bearbeitungssteuerelementfenster zu machen.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-128">You can use the **EM\_SETRECT** message to make the formatting rectangle larger or smaller than the edit control window.</span></span>

<span data-ttu-id="5c7cb-129">Wenn das Bearbeitungssteuerelement keine horizontale Bildlaufleiste aufweist und das Formatierungsrechteck größer als das Bearbeitungssteuerelementfenster ist, werden Textzeilen, die die Breite des Bearbeitungssteuerelementfensters überschreiten (aber kleiner als die Breite des Formatierungsrechtecks sind), abgeschnitten und nicht umschlossen.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-129">If the edit control does not have a horizontal scroll bar, and the formatting rectangle is set to be larger than the edit control window, lines of text exceeding the width of the edit control window (but smaller than the width of the formatting rectangle) are clipped instead of wrapped.</span></span>

<span data-ttu-id="5c7cb-130">Wenn das Bearbeitungssteuerelement einen Rahmen enthält, wird das Formatierungsrechteck um die Größe des Rahmens reduziert.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-130">If the edit control contains a border, the formatting rectangle is reduced by the size of the border.</span></span> <span data-ttu-id="5c7cb-131">Wenn Sie das von einer [**EM \_ GETRECT-Nachricht**](em-getrect.md) zurückgegebene Rechteck anpassen, müssen Sie die Größe des Rahmens entfernen, bevor Sie das Rechteck mit der **EM \_ SETRECT-Nachricht** verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-131">If you are adjusting the rectangle returned by an [**EM\_GETRECT**](em-getrect.md) message, you must remove the size of the border before using the rectangle with the **EM\_SETRECT** message.</span></span>

<span data-ttu-id="5c7cb-132">**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-132">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="5c7cb-133">Das Formatierungsrechteck enthält nicht die Auswahlleiste, bei der es sich um einen nicht markierten Bereich links neben jedem Absatz handelt.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-133">The formatting rectangle does not include the selection bar, which is an unmarked area to the left of each paragraph.</span></span> <span data-ttu-id="5c7cb-134">Wenn der Benutzer auf die Auswahlleiste klickt, wird die entsprechende Zeile ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="5c7cb-134">When the user clicks in the selection bar, the corresponding line is selected.</span></span> <span data-ttu-id="5c7cb-135">Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)</span><span class="sxs-lookup"><span data-stu-id="5c7cb-135">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c7cb-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c7cb-136">Requirements</span></span>



| <span data-ttu-id="5c7cb-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c7cb-137">Requirement</span></span> | <span data-ttu-id="5c7cb-138">Wert</span><span class="sxs-lookup"><span data-stu-id="5c7cb-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c7cb-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c7cb-139">Minimum supported client</span></span><br/> | <span data-ttu-id="5c7cb-140">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c7cb-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5c7cb-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c7cb-141">Minimum supported server</span></span><br/> | <span data-ttu-id="5c7cb-142">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c7cb-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5c7cb-143">Header</span><span class="sxs-lookup"><span data-stu-id="5c7cb-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c7cb-144"><dt>Winuser.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="5c7cb-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c7cb-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5c7cb-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="5c7cb-146">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="5c7cb-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5c7cb-147">**EM \_ GETRECT**</span><span class="sxs-lookup"><span data-stu-id="5c7cb-147">**EM\_GETRECT**</span></span>](em-getrect.md)
</dt> <dt>

[<span data-ttu-id="5c7cb-148">**EM \_ SETRECTNP**</span><span class="sxs-lookup"><span data-stu-id="5c7cb-148">**EM\_SETRECTNP**</span></span>](em-setrectnp.md)
</dt> <dt>

<span data-ttu-id="5c7cb-149">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="5c7cb-149">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="5c7cb-150">[**Rect**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5c7cb-150">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

