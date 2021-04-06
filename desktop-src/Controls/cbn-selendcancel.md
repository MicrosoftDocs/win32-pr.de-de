---
title: CBN_SELENDCANCEL Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer ein Element auswählt, aber ein anderes Steuerelement auswählt oder das Dialogfeld schließt. Gibt an, dass die anfängliche Auswahl des Benutzers ignoriert werden soll. Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: ac8d6d9f-4455-42d6-b0f1-5aaa55b8ee42
keywords:
- Windows-Steuerelemente für CBN_SELENDCANCEL Benachrichtigungs
topic_type:
- apiref
api_name:
- CBN_SELENDCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5b588fbd55af9dfa66a03c7912d4918821168b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743048"
---
# <a name="cbn_selendcancel-notification-code"></a><span data-ttu-id="d4963-106">CBN \_ selendcancel-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="d4963-106">CBN\_SELENDCANCEL notification code</span></span>

<span data-ttu-id="d4963-107">Wird gesendet, wenn der Benutzer ein Element auswählt, aber ein anderes Steuerelement auswählt oder das Dialogfeld schließt.</span><span class="sxs-lookup"><span data-stu-id="d4963-107">Sent when the user selects an item, but then selects another control or closes the dialog box.</span></span> <span data-ttu-id="d4963-108">Gibt an, dass die anfängliche Auswahl des Benutzers ignoriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4963-108">It indicates the user's initial selection is to be ignored.</span></span> <span data-ttu-id="d4963-109">Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="d4963-109">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELENDCANCEL

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d4963-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4963-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4963-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d4963-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4963-112">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner des Kombinations Felds.</span><span class="sxs-lookup"><span data-stu-id="d4963-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="d4963-113">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="d4963-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d4963-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d4963-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4963-115">Handle für das Kombinations Feld.</span><span class="sxs-lookup"><span data-stu-id="d4963-115">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4963-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4963-116">Remarks</span></span>

<span data-ttu-id="d4963-117">In einem Kombinations Feld mit dem [**\_ einfachen CBS**](combo-box-styles.md) -Stil wird der CBN- \_ Benachrichtigungs Code "selendcancel" nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="d4963-117">In a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style, the CBN\_SELENDCANCEL notification code is not sent.</span></span> <span data-ttu-id="d4963-118">Der [CBN- \_ selendok](cbn-selendok.md) -Benachrichtigungs Code wird unmittelbar vor jedem [CBN- \_ selChange](cbn-selchange.md) -Benachrichtigungs Code gesendet.</span><span class="sxs-lookup"><span data-stu-id="d4963-118">The [CBN\_SELENDOK](cbn-selendok.md) notification code is sent immediately before every [CBN\_SELCHANGE](cbn-selchange.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4963-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4963-119">Requirements</span></span>



| <span data-ttu-id="d4963-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4963-120">Requirement</span></span> | <span data-ttu-id="d4963-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d4963-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4963-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4963-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d4963-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4963-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d4963-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4963-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d4963-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4963-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d4963-126">Header</span><span class="sxs-lookup"><span data-stu-id="d4963-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4963-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="d4963-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4963-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4963-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="d4963-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d4963-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d4963-130">CBN \_ selChange</span><span class="sxs-lookup"><span data-stu-id="d4963-130">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

[<span data-ttu-id="d4963-131">CBN- \_ selendok</span><span class="sxs-lookup"><span data-stu-id="d4963-131">CBN\_SELENDOK</span></span>](cbn-selendok.md)
</dt> <dt>

<span data-ttu-id="d4963-132">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="d4963-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d4963-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d4963-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d4963-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d4963-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d4963-135">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="d4963-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

