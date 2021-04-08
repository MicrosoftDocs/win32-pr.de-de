---
title: LVM_EDITLABEL Meldung (kommstrg. h)
description: Beginnt die direkte Bearbeitung des angegebenen Texts des Listen Ansichts Elements. In der Meldung wird das angegebene Element implizit ausgewählt und fokussiert. Sie können diese Nachricht explizit oder mithilfe des ListView \_ EditLabel-Makros senden.
ms.assetid: b63f13f1-6e66-4770-af84-30bcdb241727
keywords:
- Windows-Steuerelemente für LVM_EDITLABEL Meldung
topic_type:
- apiref
api_name:
- LVM_EDITLABEL
- LVM_EDITLABELA
- LVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25cb4e119731c41130e1c19fdea2f74882796435
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739968"
---
# <a name="lvm_editlabel-message"></a><span data-ttu-id="ca10d-106">LVM- \_ EditLabel-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ca10d-106">LVM\_EDITLABEL message</span></span>

<span data-ttu-id="ca10d-107">Beginnt die direkte Bearbeitung des angegebenen Texts des Listen Ansichts Elements.</span><span class="sxs-lookup"><span data-stu-id="ca10d-107">Begins in-place editing of the specified list-view item's text.</span></span> <span data-ttu-id="ca10d-108">In der Meldung wird das angegebene Element implizit ausgewählt und fokussiert.</span><span class="sxs-lookup"><span data-stu-id="ca10d-108">The message implicitly selects and focuses the specified item.</span></span> <span data-ttu-id="ca10d-109">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="ca10d-109">You can send this message explicitly or by using the [**ListView\_EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ca10d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca10d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca10d-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ca10d-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca10d-112">Der Index des Listen Ansichts Elements.</span><span class="sxs-lookup"><span data-stu-id="ca10d-112">The index of the list-view item.</span></span> <span data-ttu-id="ca10d-113">Um die Bearbeitung abzubrechen, legen Sie den Index auf-1 fest.</span><span class="sxs-lookup"><span data-stu-id="ca10d-113">To cancel editing, set the index to -1.</span></span>

</dd> <dt>

<span data-ttu-id="ca10d-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ca10d-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ca10d-115">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ca10d-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca10d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca10d-116">Return value</span></span>

<span data-ttu-id="ca10d-117">Gibt das Handle für das Bearbeitungs Steuerelement zurück, mit dem der Element Text bei erfolgreicher Bearbeitung bearbeitet wird, andernfalls **null** .</span><span class="sxs-lookup"><span data-stu-id="ca10d-117">Returns the handle to the edit control that is used to edit the item text if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca10d-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca10d-118">Remarks</span></span>

<span data-ttu-id="ca10d-119">Wenn der Benutzer die Bearbeitung abschließt oder abbricht, wird das Bearbeitungs Steuerelement zerstört und das Handle ist nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="ca10d-119">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="ca10d-120">Sie können das Bearbeitungs Steuerelement unterteilen, aber Sie sollten es nicht zerstören.</span><span class="sxs-lookup"><span data-stu-id="ca10d-120">You can subclass the edit control, but you should not destroy it.</span></span>

<span data-ttu-id="ca10d-121">Vor dem Senden dieser Nachricht an das-Steuerelement muss das-Steuerelement den Fokus haben.</span><span class="sxs-lookup"><span data-stu-id="ca10d-121">The control must have the focus before you send this message to the control.</span></span> <span data-ttu-id="ca10d-122">Der Fokus kann mithilfe der [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) -Funktion festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ca10d-122">Focus can be set using the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function.</span></span>

<span data-ttu-id="ca10d-123">Wenn *wParam* den Wert-1 hat, wird ein [LVN \_ endlabeledit](lvn-endlabeledit.md) -Benachrichtigungs Code gesendet.</span><span class="sxs-lookup"><span data-stu-id="ca10d-123">If *wParam* is -1, an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification code is sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca10d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca10d-124">Requirements</span></span>



| <span data-ttu-id="ca10d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca10d-125">Requirement</span></span> | <span data-ttu-id="ca10d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="ca10d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca10d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ca10d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ca10d-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca10d-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ca10d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ca10d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ca10d-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca10d-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca10d-131">Header</span><span class="sxs-lookup"><span data-stu-id="ca10d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca10d-132"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca10d-132"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ca10d-133">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="ca10d-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ca10d-134">**LVM \_ Editlabelw** (Unicode) und **LVM \_ editlabela** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ca10d-134">**LVM\_EDITLABELW** (Unicode) and **LVM\_EDITLABELA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="ca10d-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca10d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca10d-136">**WM- \_ cancelmode**</span><span class="sxs-lookup"><span data-stu-id="ca10d-136">**WM\_CANCELMODE**</span></span>](/windows/desktop/winmsg/wm-cancelmode)
</dt> </dl>

 

