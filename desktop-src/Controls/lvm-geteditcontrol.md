---
title: LVM_GETEDITCONTROL Meldung (kommstrg. h)
description: Ruft das Handle für das Bearbeitungs Steuerelement ab, das verwendet wird, um den Text eines Listen Ansichts Elements zu bearbeiten. Sie können diese Nachricht explizit oder mithilfe des ListView \_ geteditcontrol-Makros senden.
ms.assetid: 70450b24-9879-4be8-9bc9-f87008b66415
keywords:
- Windows-Steuerelemente für LVM_GETEDITCONTROL Meldung
topic_type:
- apiref
api_name:
- LVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a8790f86fee17f72078f61899edcd79b331759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040105"
---
# <a name="lvm_geteditcontrol-message"></a><span data-ttu-id="a547e-105">LVM \_ geteditcontrol-Nachricht</span><span class="sxs-lookup"><span data-stu-id="a547e-105">LVM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="a547e-106">Ruft das Handle für das Bearbeitungs Steuerelement ab, das verwendet wird, um den Text eines Listen Ansichts Elements zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="a547e-106">Gets the handle to the edit control being used to edit a list-view item's text.</span></span> <span data-ttu-id="a547e-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ geteditcontrol**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="a547e-107">You can send this message explicitly or by using the [**ListView\_GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a547e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a547e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a547e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a547e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a547e-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a547e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a547e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a547e-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a547e-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a547e-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a547e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a547e-113">Return value</span></span>

<span data-ttu-id="a547e-114">Gibt das Handle für das Bearbeitungs Steuerelement zurück, wenn erfolgreich, andernfalls **null** .</span><span class="sxs-lookup"><span data-stu-id="a547e-114">Returns the handle to the edit control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a547e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a547e-115">Remarks</span></span>

<span data-ttu-id="a547e-116">Wenn die Bezeichnungs Bearbeitung beginnt, wird ein Bearbeitungs Steuerelement erstellt, positioniert und initialisiert.</span><span class="sxs-lookup"><span data-stu-id="a547e-116">When label editing begins, an edit control is created, positioned, and initialized.</span></span> <span data-ttu-id="a547e-117">Bevor es angezeigt wird, sendet das Listenansicht-Steuerelement seinen übergeordneten Fenster einen [LVN \_ beginlabeledit](lvn-beginlabeledit.md) -Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="a547e-117">Before it is displayed, the list-view control sends its parent window an [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) notification code.</span></span>

<span data-ttu-id="a547e-118">Implementieren Sie zum Anpassen der Bezeichnungs Bearbeitung einen Handler für [LVN \_ beginlabeledit](lvn-beginlabeledit.md) , und senden Sie eine **LVM \_ geteditcontrol** -Nachricht an das Listenansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="a547e-118">To customize label editing, implement a handler for [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) and have it send an **LVM\_GETEDITCONTROL** message to the list-view control.</span></span> <span data-ttu-id="a547e-119">Wenn eine Bezeichnung bearbeitet wird, ist der Rückgabewert ein Handle für das Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="a547e-119">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="a547e-120">Verwenden Sie dieses Handle, um das Bearbeitungs Steuerelement anzupassen, indem Sie die üblichen **EM \_ xxx** -Meldungen senden.</span><span class="sxs-lookup"><span data-stu-id="a547e-120">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

<span data-ttu-id="a547e-121">Wenn der Benutzer die Bearbeitung abschließt oder abbricht, wird das Bearbeitungs Steuerelement zerstört und das Handle ist nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="a547e-121">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="a547e-122">Sie können das Bearbeitungs Steuerelement unterteilen, aber Sie sollten es nicht zerstören.</span><span class="sxs-lookup"><span data-stu-id="a547e-122">You can subclass the edit control, but you should not destroy it.</span></span> <span data-ttu-id="a547e-123">Zum Abbrechen der Bearbeitung senden Sie das Listenansicht-Steuerelement an eine [**WM \_ cancelmode**](/windows/desktop/winmsg/wm-cancelmode) -Meldung.</span><span class="sxs-lookup"><span data-stu-id="a547e-123">To cancel editing, send the list-view control a [**WM\_CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) message.</span></span>

<span data-ttu-id="a547e-124">Das zu bearbeitende Listen Ansichts Element ist das aktuell fokussierte Element, d. h. das Element im Fokus Zustand.</span><span class="sxs-lookup"><span data-stu-id="a547e-124">The list-view item being edited is the currently focused item that is, the item in the focused state.</span></span> <span data-ttu-id="a547e-125">Um nach einem Element auf der Grundlage seines Zustands zu suchen, verwenden Sie die [**LVM \_ GetNextItem**](lvm-getnextitem.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a547e-125">To find an item based on its state, use the [**LVM\_GETNEXTITEM**](lvm-getnextitem.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a547e-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a547e-126">Requirements</span></span>



| <span data-ttu-id="a547e-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a547e-127">Requirement</span></span> | <span data-ttu-id="a547e-128">Wert</span><span class="sxs-lookup"><span data-stu-id="a547e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a547e-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a547e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a547e-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a547e-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a547e-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a547e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a547e-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a547e-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a547e-133">Header</span><span class="sxs-lookup"><span data-stu-id="a547e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a547e-134"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a547e-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a547e-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a547e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a547e-136">**ListView \_ geteditcontrol**</span><span class="sxs-lookup"><span data-stu-id="a547e-136">**ListView\_GetEditControl**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol)
</dt> </dl>

 

