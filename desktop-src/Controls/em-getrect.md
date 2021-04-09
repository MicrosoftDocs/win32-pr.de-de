---
title: EM_GETRECT Meldung (Winuser. h)
description: Ruft das Formatierungs Rechteck eines Bearbeitungs Steuer Elements ab.
ms.assetid: eef0150d-9b7a-4247-acbf-6fea2efd1dc3
keywords:
- Windows-Steuerelemente für EM_GETRECT Meldung
topic_type:
- apiref
api_name:
- EM_GETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8192fd4c3aa7fbe953a36217f6b1408f055d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858961"
---
# <a name="em_getrect-message"></a><span data-ttu-id="64f8d-104">EM \_ GetRect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="64f8d-104">EM\_GETRECT message</span></span>

<span data-ttu-id="64f8d-105">Ruft das [Formatierungs Rechteck](about-edit-controls.md) eines Bearbeitungs Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="64f8d-105">Gets the [formatting rectangle](about-edit-controls.md) of an edit control.</span></span> <span data-ttu-id="64f8d-106">Das Formatierungs Rechteck ist das einschränkende Rechteck, in das das Steuerelement den Text zeichnet.</span><span class="sxs-lookup"><span data-stu-id="64f8d-106">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="64f8d-107">Das Begrenzungs Rechteck ist unabhängig von der Größe des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="64f8d-107">The limiting rectangle is independent of the size of the edit-control window.</span></span> <span data-ttu-id="64f8d-108">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="64f8d-108">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="64f8d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="64f8d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64f8d-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="64f8d-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64f8d-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="64f8d-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="64f8d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64f8d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64f8d-113">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das Formatierungs Rechteck empfängt.</span><span class="sxs-lookup"><span data-stu-id="64f8d-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the formatting rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64f8d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64f8d-114">Return value</span></span>

<span data-ttu-id="64f8d-115">Der Rückgabewert ist nicht sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="64f8d-115">The return value is not meaningful.</span></span>

## <a name="remarks"></a><span data-ttu-id="64f8d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64f8d-116">Remarks</span></span>

<span data-ttu-id="64f8d-117">Sie können das Formatierungs Rechteck eines mehrzeiligen Bearbeitungs Steuer Elements ändern, indem Sie die Meldungen " [**EM \_ SetRect**](em-setrect.md) " und " [**EM \_ setrectnp**](em-setrectnp.md) " verwenden.</span><span class="sxs-lookup"><span data-stu-id="64f8d-117">You can modify the formatting rectangle of a multiline edit control by using the [**EM\_SETRECT**](em-setrect.md) and [**EM\_SETRECTNP**](em-setrectnp.md) messages.</span></span>

<span data-ttu-id="64f8d-118">Unter bestimmten Bedingungen gibt **EM \_ GetRect** möglicherweise nicht die exakten Werte zurück, die von [**EM \_ SetRect**](em-setrect.md) oder [**EM \_ setrectnp**](em-setrectnp.md) festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="64f8d-118">Under certain conditions, **EM\_GETRECT** might not return the exact values that [**EM\_SETRECT**](em-setrect.md) or [**EM\_SETRECTNP**](em-setrectnp.md) set it will be approximately correct, but it can be off by a few pixels.</span></span>

<span data-ttu-id="64f8d-119">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="64f8d-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="64f8d-120">Das Formatierungs Rechteck enthält nicht die Auswahl Leiste, bei der es sich um einen nicht markierten Bereich links neben den einzelnen Absätzen handelt.</span><span class="sxs-lookup"><span data-stu-id="64f8d-120">The formatting rectangle does not include the selection bar, which is an unmarked area to the left of each paragraph.</span></span> <span data-ttu-id="64f8d-121">Wenn Sie darauf klicken, wählt die Auswahl Leiste die Zeile aus.</span><span class="sxs-lookup"><span data-stu-id="64f8d-121">When clicked, the selection bar selects the line.</span></span> <span data-ttu-id="64f8d-122">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="64f8d-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="64f8d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64f8d-123">Requirements</span></span>



| <span data-ttu-id="64f8d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64f8d-124">Requirement</span></span> | <span data-ttu-id="64f8d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="64f8d-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64f8d-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64f8d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="64f8d-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64f8d-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="64f8d-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64f8d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="64f8d-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64f8d-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="64f8d-130">Header</span><span class="sxs-lookup"><span data-stu-id="64f8d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="64f8d-131"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="64f8d-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64f8d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64f8d-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="64f8d-133">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="64f8d-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="64f8d-134">**EM \_ SetRect**</span><span class="sxs-lookup"><span data-stu-id="64f8d-134">**EM\_SETRECT**</span></span>](em-setrect.md)
</dt> <dt>

[<span data-ttu-id="64f8d-135">**EM \_ setrectnp**</span><span class="sxs-lookup"><span data-stu-id="64f8d-135">**EM\_SETRECTNP**</span></span>](em-setrectnp.md)
</dt> <dt>

<span data-ttu-id="64f8d-136">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="64f8d-136">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="64f8d-137">[**Rect**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="64f8d-137">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

