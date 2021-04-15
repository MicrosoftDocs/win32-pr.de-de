---
title: EM_CHARFROMPOS Meldung (Winuser. h)
description: Ruft Informationen über das Zeichen ab, das einem angegebenen Punkt im Client Bereich eines Bearbeitungs Steuer Elements am nächsten liegt. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: fe9f96f2-5b3c-4039-befd-5e9a456ba32d
keywords:
- Windows-Steuerelemente für EM_CHARFROMPOS Meldung
topic_type:
- apiref
api_name:
- EM_CHARFROMPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1156d69c012faa0141726c00ab880d954fe2857
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477607"
---
# <a name="em_charfrompos-message"></a><span data-ttu-id="d1cc1-105">EM \_ charfrompos-Meldung</span><span class="sxs-lookup"><span data-stu-id="d1cc1-105">EM\_CHARFROMPOS message</span></span>

<span data-ttu-id="d1cc1-106">Ruft Informationen über das Zeichen ab, das einem angegebenen Punkt im Client Bereich eines Bearbeitungs Steuer Elements am nächsten liegt.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-106">Gets information about the character closest to a specified point in the client area of an edit control.</span></span> <span data-ttu-id="d1cc1-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1cc1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1cc1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1cc1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1cc1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1cc1-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1cc1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1cc1-112">Die Koordinaten eines Punkts im Client Bereich des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-112">The coordinates of a point in the control's client area.</span></span> <span data-ttu-id="d1cc1-113">Die Koordinaten befinden sich in Bildschirm Einheiten und sind relativ zur oberen linken Ecke des Client Bereichs des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-113">The coordinates are in screen units and are relative to the upper-left corner of the control's client area.</span></span>

<span data-ttu-id="d1cc1-114">**Rich Edit-Steuerelemente:** Ein Zeiger auf eine [**pointl**](/previous-versions//dd162807(v=vs.85)) -Struktur, die die horizontalen und vertikalen Koordinaten enthält.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-114">**Rich edit controls:** A pointer to a [**POINTL**](/previous-versions//dd162807(v=vs.85)) structure that contains the horizontal and vertical coordinates.</span></span>

<span data-ttu-id="d1cc1-115">Steuer **Elemente bearbeiten:** Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält die horizontale Koordinate.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-115">**Edit controls:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the horizontal coordinate.</span></span> <span data-ttu-id="d1cc1-116">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) enthält die vertikale Koordinate.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-116">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the vertical coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1cc1-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1cc1-117">Return value</span></span>

<span data-ttu-id="d1cc1-118">**Rich Edit-Steuerelemente:** Der Rückgabewert gibt den NULL basierten Zeichen Index des Zeichens an, das dem angegebenen Punkt am nächsten liegt.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-118">**Rich edit controls:** The return value specifies the zero-based character index of the character nearest the specified point.</span></span> <span data-ttu-id="d1cc1-119">Der Rückgabewert gibt das letzte Zeichen im Bearbeitungs Steuerelement an, wenn der angegebene Punkt hinter dem letzten Zeichen im Steuerelement liegt.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-119">The return value indicates the last character in the edit control if the specified point is beyond the last character in the control.</span></span>

<span data-ttu-id="d1cc1-120">Steuer **Elemente bearbeiten:** Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den NULL basierten Index des Zeichens an, das dem angegebenen Punkt am nächsten liegt.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-120">**Edit controls:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the character nearest the specified point.</span></span> <span data-ttu-id="d1cc1-121">Dieser Index ist relativ zum Anfang des Steuer Elements, nicht zum Anfang der Zeile.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-121">This index is relative to the beginning of the control, not the beginning of the line.</span></span> <span data-ttu-id="d1cc1-122">Wenn der angegebene Punkt hinter dem letzten Zeichen im Bearbeitungs Steuerelement liegt, gibt der Rückgabewert das letzte Zeichen im Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-122">If the specified point is beyond the last character in the edit control, the return value indicates the last character in the control.</span></span> <span data-ttu-id="d1cc1-123">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den NULL basierten Index der Zeile an, in der das Zeichen enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-123">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the zero-based index of the line that contains the character.</span></span> <span data-ttu-id="d1cc1-124">Für einzeilige Bearbeitungs Steuerelemente ist dieser Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-124">For single-line edit controls, this value is zero.</span></span> <span data-ttu-id="d1cc1-125">Der Index gibt das Zeilen Trennzeichen an, wenn der angegebene Punkt hinter dem letzten sichtbaren Zeichen in einer Zeile liegt.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-125">The index indicates the line delimiter if the specified point is beyond the last visible character in a line.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1cc1-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1cc1-126">Remarks</span></span>

<span data-ttu-id="d1cc1-127">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-127">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="d1cc1-128">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-128">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="d1cc1-129">Wenn ein Punkt als *LPARAM* an **EM \_ charfrompos** und der Punkt außerhalb der Begrenzungen des Bearbeitungs Steuer Elements liegt, ist das *LRESULT* (65535, 65535).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-129">If a point is passed to **EM\_CHARFROMPOS** as the *lParam* and the point is outside the bounds of the edit control, then the *lResult* is (65535, 65535).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1cc1-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1cc1-130">Requirements</span></span>



| <span data-ttu-id="d1cc1-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1cc1-131">Requirement</span></span> | <span data-ttu-id="d1cc1-132">Wert</span><span class="sxs-lookup"><span data-stu-id="d1cc1-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1cc1-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1cc1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d1cc1-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1cc1-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d1cc1-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1cc1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d1cc1-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1cc1-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d1cc1-137">Header</span><span class="sxs-lookup"><span data-stu-id="d1cc1-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1cc1-138"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="d1cc1-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1cc1-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1cc1-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="d1cc1-140">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d1cc1-141">**EM \_ posfromchar**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-141">**EM\_POSFROMCHAR**</span></span>](em-posfromchar.md)
</dt> <dt>

<span data-ttu-id="d1cc1-142">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="d1cc1-143">**Makelparam**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-143">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

<span data-ttu-id="d1cc1-144">[**Pointl**](/previous-versions//dd162807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d1cc1-144">[**POINTL**](/previous-versions//dd162807(v=vs.85))</span></span>
</dt> </dl>

 

