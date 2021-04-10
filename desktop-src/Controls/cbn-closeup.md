---
title: CBN_CLOSEUP Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn das Listenfeld eines Kombinations Felds geschlossen wurde. Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: 79b2108e-1ef3-433d-a0b0-ac9ad1a93905
keywords:
- Windows-Steuerelemente für CBN_CLOSEUP Benachrichtigungs
topic_type:
- apiref
api_name:
- CBN_CLOSEUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec67cf68109d32d6e1ad714f91a97987f9a3734d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106443"
---
# <a name="cbn_closeup-notification-code"></a><span data-ttu-id="e9ace-105">CBN- \_ closeup-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="e9ace-105">CBN\_CLOSEUP notification code</span></span>

<span data-ttu-id="e9ace-106">Wird gesendet, wenn das Listenfeld eines Kombinations Felds geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="e9ace-106">Sent when the list box of a combo box has been closed.</span></span> <span data-ttu-id="e9ace-107">Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="e9ace-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_CLOSEUP

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e9ace-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9ace-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9ace-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9ace-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9ace-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner des Kombinations Felds.</span><span class="sxs-lookup"><span data-stu-id="e9ace-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="e9ace-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="e9ace-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="e9ace-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9ace-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9ace-113">Handle für das Kombinations Feld.</span><span class="sxs-lookup"><span data-stu-id="e9ace-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9ace-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9ace-114">Remarks</span></span>

<span data-ttu-id="e9ace-115">Wenn der Benutzer die aktuelle Auswahl geändert hat, sendet das Kombinations Feld auch den [CBN \_ selChange](cbn-selchange.md) -Benachrichtigungs Code, wenn die Dropdown Liste geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="e9ace-115">If the user changed the current selection, the combo box also sends the [CBN\_SELCHANGE](cbn-selchange.md) notification code when the drop-down list closes.</span></span> <span data-ttu-id="e9ace-116">Im Allgemeinen können Sie die Reihenfolge, in der die Benachrichtigungs Codes gesendet werden, nicht vorhersagen.</span><span class="sxs-lookup"><span data-stu-id="e9ace-116">In general, you cannot predict the order in which notification codes will be sent.</span></span> <span data-ttu-id="e9ace-117">Insbesondere kann es vorkommen, dass ein CBN-Änderungs \_ Benachrichtigungs Code entweder vor oder nach einem CBN- \_ closeup-Benachrichtigungs Code vorliegt.</span><span class="sxs-lookup"><span data-stu-id="e9ace-117">In particular, a CBN\_SELCHANGE notification code may occur either before or after a CBN\_CLOSEUP notification code.</span></span>

<span data-ttu-id="e9ace-118">Um einen bestimmten Prozess jedes Mal auszuführen, wenn der Benutzer ein Listenelement auswählt, können Sie entweder den Benachrichtigungs Code [CBN \_ selChange](cbn-selchange.md) oder CBN \_ closeup verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e9ace-118">To execute a specific process each time the user selects a list item, you can handle either the [CBN\_SELCHANGE](cbn-selchange.md) or CBN\_CLOSEUP notification code.</span></span> <span data-ttu-id="e9ace-119">In der Regel warten Sie \_ vor dem Verarbeiten einer Änderung in der aktuellen Auswahl den Benachrichtigungs Code für die CBN-Schließung.</span><span class="sxs-lookup"><span data-stu-id="e9ace-119">Typically, you would wait for the CBN\_CLOSEUP notification code before processing a change in the current selection.</span></span> <span data-ttu-id="e9ace-120">Dies kann besonders wichtig sein, wenn eine beträchtliche Menge an Verarbeitung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e9ace-120">This can be particularly important if a significant amount of processing is required.</span></span>

<span data-ttu-id="e9ace-121">Dieser Benachrichtigungs Code wird nicht an ein Kombinations Feld mit dem [**\_ einfachen CBS**](combo-box-styles.md) -Format gesendet.</span><span class="sxs-lookup"><span data-stu-id="e9ace-121">This notification code is not sent to a combo box that has the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9ace-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9ace-122">Requirements</span></span>



| <span data-ttu-id="e9ace-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9ace-123">Requirement</span></span> | <span data-ttu-id="e9ace-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e9ace-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ace-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9ace-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e9ace-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9ace-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e9ace-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9ace-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e9ace-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9ace-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e9ace-129">Header</span><span class="sxs-lookup"><span data-stu-id="e9ace-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9ace-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="e9ace-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9ace-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9ace-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="e9ace-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="e9ace-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e9ace-133">CBN- \_ Dropdown</span><span class="sxs-lookup"><span data-stu-id="e9ace-133">CBN\_DROPDOWN</span></span>](cbn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="e9ace-134">CBN \_ selChange</span><span class="sxs-lookup"><span data-stu-id="e9ace-134">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

<span data-ttu-id="e9ace-135">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="e9ace-135">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="e9ace-136">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9ace-136">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="e9ace-137">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9ace-137">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e9ace-138">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="e9ace-138">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

