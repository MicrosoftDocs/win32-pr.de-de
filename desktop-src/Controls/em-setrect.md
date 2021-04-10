---
title: EM_SETRECT Meldung (Winuser. h)
description: Legt das Formatierungs Rechteck eines mehrzeiligen Bearbeitungs Steuer Elements fest.
ms.assetid: 4f576e94-3bd3-4416-a960-b7f22da963ea
keywords:
- Windows-Steuerelemente für EM_SETRECT Meldung
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
ms.openlocfilehash: a12b171478b0cb9d47496d20d4d1b6b1e8ddd29a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040545"
---
# <a name="em_setrect-message"></a><span data-ttu-id="55c95-104">EM- \_ SetRect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="55c95-104">EM\_SETRECT message</span></span>

<span data-ttu-id="55c95-105">Legt das [Formatierungs Rechteck](about-edit-controls.md) eines mehrzeiligen Bearbeitungs Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="55c95-105">Sets the [formatting rectangle](about-edit-controls.md) of a multiline edit control.</span></span> <span data-ttu-id="55c95-106">Das Formatierungs Rechteck ist das einschränkende Rechteck, in das das Steuerelement den Text zeichnet.</span><span class="sxs-lookup"><span data-stu-id="55c95-106">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="55c95-107">Das Begrenzungs Rechteck ist unabhängig von der Größe des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="55c95-107">The limiting rectangle is independent of the size of the edit control window.</span></span>

<span data-ttu-id="55c95-108">Diese Meldung wird nur von mehrzeiligen Bearbeitungs Steuerelementen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="55c95-108">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="55c95-109">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="55c95-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="55c95-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="55c95-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55c95-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="55c95-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55c95-112">**Rich Edit 2,0 und höher:** Gibt an, ob *LPARAM* absolute oder relative Koordinaten angibt.</span><span class="sxs-lookup"><span data-stu-id="55c95-112">**Rich Edit 2.0 and later:** Indicates whether *lParam* specifies absolute or relative coordinates.</span></span> <span data-ttu-id="55c95-113">Der Wert 0 (null) gibt absolute Koordinaten an.</span><span class="sxs-lookup"><span data-stu-id="55c95-113">A value of zero indicates absolute coordinates.</span></span> <span data-ttu-id="55c95-114">Der Wert 1 gibt Offsets relativ zum aktuellen Formatierungs Rechteck an.</span><span class="sxs-lookup"><span data-stu-id="55c95-114">A value of 1 indicates offsets relative to the current formatting rectangle.</span></span> <span data-ttu-id="55c95-115">(Die Offsets können positiv oder negativ sein.)</span><span class="sxs-lookup"><span data-stu-id="55c95-115">(The offsets can be positive or negative.)</span></span>

<span data-ttu-id="55c95-116">**Bearbeitungs Steuerelemente und umfangreiche Bearbeitung 1,0:** Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="55c95-116">**Edit controls and Rich Edit 1.0:** This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="55c95-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="55c95-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55c95-118">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die neuen Abmessungen des Rechtecks angibt.</span><span class="sxs-lookup"><span data-stu-id="55c95-118">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the new dimensions of the rectangle.</span></span> <span data-ttu-id="55c95-119">Wenn dieser Parameter **null** ist, wird das Formatierungs Rechteck auf seine Standardwerte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="55c95-119">If this parameter is **NULL**, the formatting rectangle is set to its default values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55c95-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55c95-120">Return value</span></span>

<span data-ttu-id="55c95-121">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="55c95-121">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="55c95-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55c95-122">Remarks</span></span>

<span data-ttu-id="55c95-123">Das Festlegen von *LPARAM* auf **null** hat keine Auswirkungen, wenn ein Finger Eingabegerät installiert ist, oder wenn **EM \_ SetRect** von einem Thread gesendet wird, auf dem ein Hook installiert ist (siehe [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)).</span><span class="sxs-lookup"><span data-stu-id="55c95-123">Setting *lParam* to **NULL** has no effect if a touch device is installed, or if **EM\_SETRECT** is sent from a thread that has a hook installed (see [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)).</span></span> <span data-ttu-id="55c95-124">In diesen Fällen sollte *LPARAM* einen gültigen Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="55c95-124">In these cases, *lParam* should contain a valid pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span>

<span data-ttu-id="55c95-125">Die **EM- \_ SetRect** -Meldung bewirkt, dass der Text des Bearbeitungs Steuer Elements neu gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="55c95-125">The **EM\_SETRECT** message causes the text of the edit control to be redrawn.</span></span> <span data-ttu-id="55c95-126">Um die Größe des Formatierungs Rechtecks zu ändern, ohne den Text neu zu zeichnen, verwenden Sie die Nachricht [**EM \_ setrectnp**](em-setrectnp.md) .</span><span class="sxs-lookup"><span data-stu-id="55c95-126">To change the size of the formatting rectangle without redrawing the text, use the [**EM\_SETRECTNP**](em-setrectnp.md) message.</span></span>

<span data-ttu-id="55c95-127">Wenn ein Bearbeitungs Steuerelement erstmalig erstellt wird, wird das Formatierungs Rechteck auf eine Standardgröße festgelegt.</span><span class="sxs-lookup"><span data-stu-id="55c95-127">When an edit control is first created, the formatting rectangle is set to a default size.</span></span> <span data-ttu-id="55c95-128">Sie können die Nachricht **EM \_ SetRect** verwenden, um das Formatierungs Rechteck größer oder kleiner als das Bearbeitungs Steuerelement Fenster zu machen.</span><span class="sxs-lookup"><span data-stu-id="55c95-128">You can use the **EM\_SETRECT** message to make the formatting rectangle larger or smaller than the edit control window.</span></span>

<span data-ttu-id="55c95-129">Wenn das Bearbeitungs Steuerelement keine horizontale Schiebe Leiste hat und das Formatierungs Rechteck auf größer als das Bearbeitungs Steuerelement festgelegt ist, werden Textzeilen, die die Breite des Bearbeitungs Steuer Elements überschreiten (jedoch kleiner als die Breite des Formatierungs Rechtecks), abgeschnitten anstatt umschließen.</span><span class="sxs-lookup"><span data-stu-id="55c95-129">If the edit control does not have a horizontal scroll bar, and the formatting rectangle is set to be larger than the edit control window, lines of text exceeding the width of the edit control window (but smaller than the width of the formatting rectangle) are clipped instead of wrapped.</span></span>

<span data-ttu-id="55c95-130">Wenn das Bearbeitungs Steuerelement einen Rahmen enthält, wird das Formatierungs Rechteck um die Größe des Rahmens reduziert.</span><span class="sxs-lookup"><span data-stu-id="55c95-130">If the edit control contains a border, the formatting rectangle is reduced by the size of the border.</span></span> <span data-ttu-id="55c95-131">Wenn Sie das von einer [**EM \_ GetRect**](em-getrect.md) -Nachricht zurückgegebene Rechteck anpassen, müssen Sie die Größe des Rahmens entfernen, bevor Sie das Rechteck mit der **EM- \_ SetRect** -Nachricht verwenden.</span><span class="sxs-lookup"><span data-stu-id="55c95-131">If you are adjusting the rectangle returned by an [**EM\_GETRECT**](em-getrect.md) message, you must remove the size of the border before using the rectangle with the **EM\_SETRECT** message.</span></span>

<span data-ttu-id="55c95-132">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="55c95-132">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="55c95-133">Das Formatierungs Rechteck enthält nicht die Auswahl Leiste, bei der es sich um einen nicht markierten Bereich links neben den einzelnen Absätzen handelt.</span><span class="sxs-lookup"><span data-stu-id="55c95-133">The formatting rectangle does not include the selection bar, which is an unmarked area to the left of each paragraph.</span></span> <span data-ttu-id="55c95-134">Wenn der Benutzer in der Auswahl Leiste auf klickt, wird die entsprechende Zeile ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="55c95-134">When the user clicks in the selection bar, the corresponding line is selected.</span></span> <span data-ttu-id="55c95-135">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="55c95-135">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55c95-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55c95-136">Requirements</span></span>



| <span data-ttu-id="55c95-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55c95-137">Requirement</span></span> | <span data-ttu-id="55c95-138">Wert</span><span class="sxs-lookup"><span data-stu-id="55c95-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55c95-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55c95-139">Minimum supported client</span></span><br/> | <span data-ttu-id="55c95-140">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55c95-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="55c95-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55c95-141">Minimum supported server</span></span><br/> | <span data-ttu-id="55c95-142">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55c95-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="55c95-143">Header</span><span class="sxs-lookup"><span data-stu-id="55c95-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="55c95-144"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="55c95-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55c95-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55c95-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="55c95-146">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="55c95-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="55c95-147">**EM \_ GetRect**</span><span class="sxs-lookup"><span data-stu-id="55c95-147">**EM\_GETRECT**</span></span>](em-getrect.md)
</dt> <dt>

[<span data-ttu-id="55c95-148">**EM \_ setrectnp**</span><span class="sxs-lookup"><span data-stu-id="55c95-148">**EM\_SETRECTNP**</span></span>](em-setrectnp.md)
</dt> <dt>

<span data-ttu-id="55c95-149">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="55c95-149">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="55c95-150">[**Rect**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="55c95-150">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

