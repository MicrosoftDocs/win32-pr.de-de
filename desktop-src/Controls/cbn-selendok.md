---
title: CBN_SELENDOK Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer ein Listenelement auswählt oder ein Element auswählt und dann die Liste schließt. Gibt an, dass die Auswahl des Benutzers verarbeitet werden soll. Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: ef0ac46f-2db9-40d6-ba82-7e90d71fdd37
keywords:
- Windows-Steuerelemente für CBN_SELENDOK Benachrichtigungs
topic_type:
- apiref
api_name:
- CBN_SELENDOK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0b04fcce0ec2b3f6a2bf5b5e04fa4110ad6ceb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337331"
---
# <a name="cbn_selendok-notification-code"></a><span data-ttu-id="16645-106">CBN- \_ selendok-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="16645-106">CBN\_SELENDOK notification code</span></span>

<span data-ttu-id="16645-107">Wird gesendet, wenn der Benutzer ein Listenelement auswählt oder ein Element auswählt und dann die Liste schließt.</span><span class="sxs-lookup"><span data-stu-id="16645-107">Sent when the user selects a list item, or selects an item and then closes the list.</span></span> <span data-ttu-id="16645-108">Gibt an, dass die Auswahl des Benutzers verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="16645-108">It indicates that the user's selection is to be processed.</span></span> <span data-ttu-id="16645-109">Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="16645-109">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELENDOK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="16645-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="16645-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16645-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="16645-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16645-112">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner des Kombinations Felds.</span><span class="sxs-lookup"><span data-stu-id="16645-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="16645-113">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="16645-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="16645-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="16645-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16645-115">Handle für das Kombinations Feld.</span><span class="sxs-lookup"><span data-stu-id="16645-115">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16645-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16645-116">Remarks</span></span>

<span data-ttu-id="16645-117">In einem Kombinations Feld mit dem [**\_ einfachen CBS**](combo-box-styles.md) -Stil wird der CBN- \_ selendok-Benachrichtigungs Code unmittelbar vor jedem [CBN- \_ selChange](cbn-selchange.md) -Benachrichtigungs Code gesendet.</span><span class="sxs-lookup"><span data-stu-id="16645-117">In a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style, the CBN\_SELENDOK notification code is sent immediately before every [CBN\_SELCHANGE](cbn-selchange.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="16645-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16645-118">Requirements</span></span>



| <span data-ttu-id="16645-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16645-119">Requirement</span></span> | <span data-ttu-id="16645-120">Wert</span><span class="sxs-lookup"><span data-stu-id="16645-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16645-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16645-121">Minimum supported client</span></span><br/> | <span data-ttu-id="16645-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16645-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="16645-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16645-123">Minimum supported server</span></span><br/> | <span data-ttu-id="16645-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16645-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="16645-125">Header</span><span class="sxs-lookup"><span data-stu-id="16645-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="16645-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="16645-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16645-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16645-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="16645-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="16645-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="16645-129">CBN \_ selChange</span><span class="sxs-lookup"><span data-stu-id="16645-129">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

[<span data-ttu-id="16645-130">CBN \_ selendcancel</span><span class="sxs-lookup"><span data-stu-id="16645-130">CBN\_SELENDCANCEL</span></span>](cbn-selendcancel.md)
</dt> <dt>

<span data-ttu-id="16645-131">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="16645-131">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="16645-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="16645-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="16645-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="16645-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="16645-134">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="16645-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

