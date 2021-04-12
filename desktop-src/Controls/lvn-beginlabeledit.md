---
title: LVN_BEGINLABELEDIT Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements über den Anfang der Bezeichnungs Bearbeitung für ein Element. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: c13a9e95-22a9-476e-aeee-4928b8b096b0
keywords:
- Windows-Steuerelemente für LVN_BEGINLABELEDIT Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_BEGINLABELEDIT
- LVN_BEGINLABELEDITA
- LVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f77550b474534cee096b610a0805bce547d9b429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949460"
---
# <a name="lvn_beginlabeledit-notification-code"></a><span data-ttu-id="78ac6-105">LVN \_ beginlabeledit-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="78ac6-105">LVN\_BEGINLABELEDIT notification code</span></span>

<span data-ttu-id="78ac6-106">Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements über den Anfang der Bezeichnungs Bearbeitung für ein Element.</span><span class="sxs-lookup"><span data-stu-id="78ac6-106">Notifies a list-view control's parent window about the start of label editing for an item.</span></span> <span data-ttu-id="78ac6-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="78ac6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="78ac6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="78ac6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78ac6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78ac6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78ac6-110">Zeiger auf eine [**nmlvdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="78ac6-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="78ac6-111">Das **Element Element** dieser Struktur ist eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur, deren **iItem** -Member das Element identifiziert, das bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="78ac6-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure whose **iItem** member identifies the item being edited.</span></span> <span data-ttu-id="78ac6-112">Beachten Sie, dass unter Elemente nicht bearbeitet werden können. der **iSubItem** -Member ist immer auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="78ac6-112">Note that subitems cannot be edited; the **iSubItem** member is always set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78ac6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78ac6-113">Return value</span></span>

<span data-ttu-id="78ac6-114">Um dem Benutzer die Bearbeitung der Bezeichnung zu ermöglichen, geben Sie **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="78ac6-114">To allow the user to edit the label, return **FALSE**.</span></span>

<span data-ttu-id="78ac6-115">Um zu verhindern, dass der Benutzer die Bezeichnung bearbeitet, geben Sie " **true**" zurück.</span><span class="sxs-lookup"><span data-stu-id="78ac6-115">To prevent the user from editing the label, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="78ac6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78ac6-116">Remarks</span></span>

<span data-ttu-id="78ac6-117">Wenn die Bezeichnungs Bearbeitung beginnt, wird ein Bearbeitungs Steuerelement erstellt, positioniert und initialisiert.</span><span class="sxs-lookup"><span data-stu-id="78ac6-117">When label editing begins, an edit control is created, positioned, and initialized.</span></span> <span data-ttu-id="78ac6-118">Bevor es angezeigt wird, sendet das Listenansicht-Steuerelement seinen übergeordneten Fenster einen LVN \_ beginlabeledit-Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="78ac6-118">Before it is displayed, the list-view control sends its parent window an LVN\_BEGINLABELEDIT notification code.</span></span>

<span data-ttu-id="78ac6-119">Implementieren Sie zum Anpassen der Bezeichnungs Bearbeitung einen Handler für LVN \_ beginlabeledit, und senden Sie eine [**LVM \_ geteditcontrol**](lvm-geteditcontrol.md) -Nachricht an das Listenansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="78ac6-119">To customize label editing, implement a handler for LVN\_BEGINLABELEDIT and have it send an [**LVM\_GETEDITCONTROL**](lvm-geteditcontrol.md) message to the list-view control.</span></span> <span data-ttu-id="78ac6-120">Wenn eine Bezeichnung bearbeitet wird, ist der Rückgabewert ein Handle für das Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="78ac6-120">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="78ac6-121">Verwenden Sie dieses Handle, um das Bearbeitungs Steuerelement anzupassen, indem Sie die üblichen **EM \_ xxx** -Meldungen senden.</span><span class="sxs-lookup"><span data-stu-id="78ac6-121">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

<span data-ttu-id="78ac6-122">Wenn der Benutzer die Bearbeitung abbricht oder abschließt, empfängt das übergeordnete Fenster einen [LVN \_ endlabeledit](lvn-endlabeledit.md) -Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="78ac6-122">When the user cancels or completes the editing, the parent window receives an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="78ac6-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78ac6-123">Requirements</span></span>



| <span data-ttu-id="78ac6-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78ac6-124">Requirement</span></span> | <span data-ttu-id="78ac6-125">Wert</span><span class="sxs-lookup"><span data-stu-id="78ac6-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78ac6-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78ac6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="78ac6-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78ac6-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="78ac6-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78ac6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="78ac6-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78ac6-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="78ac6-130">Header</span><span class="sxs-lookup"><span data-stu-id="78ac6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="78ac6-131"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="78ac6-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="78ac6-132">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="78ac6-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="78ac6-133">**LVN \_ Beginlabeleditw** (Unicode) und **LVN \_ beginlabeledita** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="78ac6-133">**LVN\_BEGINLABELEDITW** (Unicode) and **LVN\_BEGINLABELEDITA** (ANSI)</span></span><br/>     |



 

 





