---
title: EM_POSFROMCHAR Meldung (Winuser. h)
description: Ruft die Client Bereichs Koordinaten eines angegebenen Zeichens in einem Bearbeitungs Steuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: a32532fa-976f-4c19-ac6e-29e5614fc410
keywords:
- Windows-Steuerelemente für EM_POSFROMCHAR Meldung
topic_type:
- apiref
api_name:
- EM_POSFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d98968873ad006b2e91cf3add2429bf7630fae1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517981"
---
# <a name="em_posfromchar-message"></a><span data-ttu-id="b024b-105">EM \_ posfromchar-Nachricht</span><span class="sxs-lookup"><span data-stu-id="b024b-105">EM\_POSFROMCHAR message</span></span>

<span data-ttu-id="b024b-106">Ruft die Client Bereichs Koordinaten eines angegebenen Zeichens in einem Bearbeitungs Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="b024b-106">Retrieves the client area coordinates of a specified character in an edit control.</span></span> <span data-ttu-id="b024b-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="b024b-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b024b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b024b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b024b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b024b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b024b-110">Umfassende **Bearbeitung 1,0 und 3,0:** Ein Zeiger auf eine [**pointl**](/previous-versions//dd162807(v=vs.85)) -Struktur, die die Client Bereichs Koordinaten des Zeichens empfängt.</span><span class="sxs-lookup"><span data-stu-id="b024b-110">**Rich Edit 1.0 and 3.0:** A pointer to a [**POINTL**](/previous-versions//dd162807(v=vs.85)) structure that receives the client area coordinates of the character.</span></span> <span data-ttu-id="b024b-111">Die Koordinaten befinden sich in Bildschirm Einheiten und sind relativ zur oberen linken Ecke des Client Bereichs des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="b024b-111">The coordinates are in screen units and are relative to the upper-left corner of the control's client area.</span></span>

<span data-ttu-id="b024b-112">**Bearbeitungs Steuerelemente und umfangreiche Bearbeitung 2,0:** Der null basierte Index des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="b024b-112">**Edit controls and Rich Edit 2.0:** The zero-based index of the character.</span></span>

</dd> <dt>

<span data-ttu-id="b024b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b024b-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b024b-114">Umfassende **Bearbeitung 1,0 und 3,0:** Der null basierte Index des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="b024b-114">**Rich Edit 1.0 and 3.0:** The zero-based index of the character.</span></span>

<span data-ttu-id="b024b-115">**Bearbeitungs Steuerelemente und umfangreiche Bearbeitung 2,0:** Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b024b-115">**Edit controls and Rich Edit 2.0:** This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b024b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b024b-116">Return value</span></span>

<span data-ttu-id="b024b-117">Umfassende **Bearbeitung 1,0 und 3,0:** Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b024b-117">**Rich Edit 1.0 and 3.0:** The return value is not used.</span></span>

<span data-ttu-id="b024b-118">**Bearbeitungs Steuerelemente und umfangreiche Bearbeitung 2,0:** Der Rückgabewert enthält die Client Bereichs Koordinaten des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="b024b-118">**Edit controls and Rich Edit 2.0:** The return value contains the client area coordinates of the character.</span></span> <span data-ttu-id="b024b-119">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält die horizontale Koordinate, und das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) enthält die vertikale Koordinate.</span><span class="sxs-lookup"><span data-stu-id="b024b-119">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the horizontal coordinate and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the vertical coordinate.</span></span>

## <a name="remarks"></a><span data-ttu-id="b024b-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b024b-120">Remarks</span></span>

<span data-ttu-id="b024b-121">Eine zurückgegebene Koordinate kann ein negativer Wert sein, wenn das angegebene Zeichen nicht im Client Bereich des Bearbeitungs Steuer Elements angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b024b-121">A returned coordinate can be a negative value if the specified character is not displayed in the edit control's client area.</span></span> <span data-ttu-id="b024b-122">Die Koordinaten werden auf ganzzahlige Werte gekürzt.</span><span class="sxs-lookup"><span data-stu-id="b024b-122">The coordinates are truncated to integer values.</span></span>

<span data-ttu-id="b024b-123">Wenn das Zeichen ein Zeilen Trennzeichen ist, geben die zurückgegebenen Koordinaten einen Punkt direkt hinter dem letzten sichtbaren Zeichen in der Zeile an.</span><span class="sxs-lookup"><span data-stu-id="b024b-123">If the character is a line delimiter, the returned coordinates indicate a point just beyond the last visible character in the line.</span></span> <span data-ttu-id="b024b-124">Wenn der angegebene Index größer als der Index des letzten Zeichens im-Steuerelement ist, gibt das Steuerelement-1 zurück.</span><span class="sxs-lookup"><span data-stu-id="b024b-124">If the specified index is greater than the index of the last character in the control, the control returns -1.</span></span>

<span data-ttu-id="b024b-125">**Rich Edit 3,0 und höher:** Aus Gründen der Abwärtskompatibilität unterstützt Microsoft Rich Edit 3,0 die Syntax, die von Microsoft Rich Edit 2,0 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b024b-125">**Rich Edit 3.0 and later:** For backward compatibility, Microsoft Rich Edit 3.0 supports the syntax used by Microsoft Rich Edit 2.0.</span></span> <span data-ttu-id="b024b-126">Wenn Microsoft Rich Edit 3,0 erkennt, dass *wParam* kein gültiger [**pointl**](/previous-versions//dd162807(v=vs.85)) -Zeiger ist, wird davon ausgegangen, dass die Nachricht mit der Microsoft Rich Edit 2,0-Syntax gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b024b-126">If Microsoft Rich Edit 3.0 detects that *wParam* is not a valid [**POINTL**](/previous-versions//dd162807(v=vs.85)) pointer, it assumes the message was sent using the Microsoft Rich Edit 2.0 syntax.</span></span> <span data-ttu-id="b024b-127">In diesem Fall wird der Rückgabewert verwendet, um die Koordinaten zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="b024b-127">In this case, it uses the return value to return the coordinates.</span></span>

<span data-ttu-id="b024b-128">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b024b-128">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="b024b-129">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="b024b-129">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b024b-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b024b-130">Requirements</span></span>



| <span data-ttu-id="b024b-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b024b-131">Requirement</span></span> | <span data-ttu-id="b024b-132">Wert</span><span class="sxs-lookup"><span data-stu-id="b024b-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b024b-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b024b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b024b-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b024b-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b024b-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b024b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b024b-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b024b-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b024b-137">Header</span><span class="sxs-lookup"><span data-stu-id="b024b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b024b-138"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="b024b-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b024b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b024b-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="b024b-140">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="b024b-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b024b-141">**EM \_ charfrompos**</span><span class="sxs-lookup"><span data-stu-id="b024b-141">**EM\_CHARFROMPOS**</span></span>](em-charfrompos.md)
</dt> <dt>

<span data-ttu-id="b024b-142">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="b024b-142">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="b024b-143">[**Pointl**](/previous-versions//dd162807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b024b-143">[**POINTL**](/previous-versions//dd162807(v=vs.85))</span></span>
</dt> </dl>

 

