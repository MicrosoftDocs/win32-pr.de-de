---
title: CBN_DROPDOWN Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn das Listenfeld eines Kombinations Felds sichtbar gemacht wird. Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: 2ee9bb19-951b-46bb-a90d-1ade92c2d76c
keywords:
- Windows-Steuerelemente für CBN_DROPDOWN Benachrichtigungs
topic_type:
- apiref
api_name:
- CBN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018dac2a17a656c11ac697836390ee64e55875db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339346"
---
# <a name="cbn_dropdown-notification-code"></a><span data-ttu-id="f99dc-105">CBN- \_ Dropdown-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="f99dc-105">CBN\_DROPDOWN notification code</span></span>

<span data-ttu-id="f99dc-106">Wird gesendet, wenn das Listenfeld eines Kombinations Felds sichtbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="f99dc-106">Sent when the list box of a combo box is about to be made visible.</span></span> <span data-ttu-id="f99dc-107">Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="f99dc-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_DROPDOWN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f99dc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f99dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f99dc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f99dc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f99dc-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner des Kombinations Felds.</span><span class="sxs-lookup"><span data-stu-id="f99dc-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="f99dc-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="f99dc-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="f99dc-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f99dc-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f99dc-113">Handle für das Kombinations Feld.</span><span class="sxs-lookup"><span data-stu-id="f99dc-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f99dc-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f99dc-114">Remarks</span></span>

<span data-ttu-id="f99dc-115">Dieser Benachrichtigungs Code wird nur gesendet, wenn das Kombinations Feld den "CBS"- [**\_ Dropdown**](combo-box-styles.md) oder den [**CBS- \_ DropDownList**](combo-box-styles.md) -Stil enthält.</span><span class="sxs-lookup"><span data-stu-id="f99dc-115">This notification code is only sent if the combo box has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="f99dc-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f99dc-116">Requirements</span></span>



| <span data-ttu-id="f99dc-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f99dc-117">Requirement</span></span> | <span data-ttu-id="f99dc-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f99dc-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f99dc-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f99dc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f99dc-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f99dc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f99dc-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f99dc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f99dc-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f99dc-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f99dc-123">Header</span><span class="sxs-lookup"><span data-stu-id="f99dc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f99dc-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="f99dc-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f99dc-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f99dc-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="f99dc-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="f99dc-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f99dc-127">CBN- \_ Schließung</span><span class="sxs-lookup"><span data-stu-id="f99dc-127">CBN\_CLOSEUP</span></span>](cbn-closeup.md)
</dt> <dt>

<span data-ttu-id="f99dc-128">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="f99dc-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="f99dc-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f99dc-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="f99dc-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f99dc-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f99dc-131">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="f99dc-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

