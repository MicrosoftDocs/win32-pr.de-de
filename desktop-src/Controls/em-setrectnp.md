---
title: EM_SETRECTNP Meldung (Winuser. h)
description: Legt das Formatierungs Rechteck eines mehrzeiligen Bearbeitungs Steuer Elements fest.
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- Windows-Steuerelemente für EM_SETRECTNP Meldung
topic_type:
- apiref
api_name:
- EM_SETRECTNP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e017bd4737c843c2452382918d71ef63345917cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957001"
---
# <a name="em_setrectnp-message"></a><span data-ttu-id="81d21-104">EM \_ setrectnp-Meldung</span><span class="sxs-lookup"><span data-stu-id="81d21-104">EM\_SETRECTNP message</span></span>

<span data-ttu-id="81d21-105">Legt das [Formatierungs Rechteck](about-edit-controls.md) eines mehrzeiligen Bearbeitungs Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="81d21-105">Sets the [formatting rectangle](about-edit-controls.md) of a multiline edit control.</span></span> <span data-ttu-id="81d21-106">Die **EM- \_ setrectnp** -Nachricht ist mit der [**EM- \_ SetRect**](em-setrect.md) -Nachricht identisch, mit dem Unterschied, dass **EM \_ setrectnp** das Bearbeitungs Steuerelement Fenster *nicht* neu zeichnet.</span><span class="sxs-lookup"><span data-stu-id="81d21-106">The **EM\_SETRECTNP** message is identical to the [**EM\_SETRECT**](em-setrect.md) message, except that **EM\_SETRECTNP** does *not* redraw the edit control window.</span></span>

<span data-ttu-id="81d21-107">Das Formatierungs Rechteck ist das einschränkende Rechteck, in das das Steuerelement den Text zeichnet.</span><span class="sxs-lookup"><span data-stu-id="81d21-107">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="81d21-108">Das Begrenzungs Rechteck ist unabhängig von der Größe des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="81d21-108">The limiting rectangle is independent of the size of the edit control window.</span></span>

<span data-ttu-id="81d21-109">Diese Meldung wird nur von mehrzeiligen Bearbeitungs Steuerelementen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="81d21-109">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="81d21-110">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="81d21-110">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="81d21-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="81d21-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81d21-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81d21-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81d21-113">**Rich Edit 3,0 und höher:** Gibt an, ob das neue Rechteck absolute oder relative Koordinaten enthält.</span><span class="sxs-lookup"><span data-stu-id="81d21-113">**Rich Edit 3.0 and later:** Indicates whether the new rectangle contains absolute or relative coordinates.</span></span> <span data-ttu-id="81d21-114">Der Wert 0 (null) gibt absolute Koordinaten an.</span><span class="sxs-lookup"><span data-stu-id="81d21-114">A value of zero indicates absolute coordinates.</span></span> <span data-ttu-id="81d21-115">Der Wert 1 gibt Offsets relativ zum aktuellen Formatierungs Rechteck an.</span><span class="sxs-lookup"><span data-stu-id="81d21-115">A value of 1 indicates offsets relative to the current formatting rectangle.</span></span> <span data-ttu-id="81d21-116">(Die Offsets können positiv oder negativ sein.)</span><span class="sxs-lookup"><span data-stu-id="81d21-116">(The offsets can be positive or negative.)</span></span>

<span data-ttu-id="81d21-117">Steuer **Elemente bearbeiten:** Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="81d21-117">**Edit controls:** This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="81d21-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81d21-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81d21-119">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die neuen Abmessungen des Rechtecks angibt.</span><span class="sxs-lookup"><span data-stu-id="81d21-119">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the new dimensions of the rectangle.</span></span> <span data-ttu-id="81d21-120">Wenn dieser Parameter **null** ist, wird das Formatierungs Rechteck auf seine Standardwerte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="81d21-120">If this parameter is **NULL**, the formatting rectangle is set to its default values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81d21-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81d21-121">Return value</span></span>

<span data-ttu-id="81d21-122">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="81d21-122">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81d21-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81d21-123">Remarks</span></span>

<span data-ttu-id="81d21-124">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 3,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="81d21-124">**Rich Edit:** Supported in Microsoft Rich Edit 3.0 and later.</span></span> <span data-ttu-id="81d21-125">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="81d21-125">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81d21-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81d21-126">Requirements</span></span>



| <span data-ttu-id="81d21-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81d21-127">Requirement</span></span> | <span data-ttu-id="81d21-128">Wert</span><span class="sxs-lookup"><span data-stu-id="81d21-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81d21-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81d21-129">Minimum supported client</span></span><br/> | <span data-ttu-id="81d21-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81d21-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="81d21-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81d21-131">Minimum supported server</span></span><br/> | <span data-ttu-id="81d21-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81d21-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="81d21-133">Header</span><span class="sxs-lookup"><span data-stu-id="81d21-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="81d21-134"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="81d21-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81d21-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81d21-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="81d21-136">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="81d21-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="81d21-137">**EM \_ SetRect**</span><span class="sxs-lookup"><span data-stu-id="81d21-137">**EM\_SETRECT**</span></span>](em-setrect.md)
</dt> <dt>

<span data-ttu-id="81d21-138">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="81d21-138">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="81d21-139">[**Rect**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="81d21-139">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

