---
title: CBN_EDITUPDATE Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Bearbeitungs Steuerungs Bereich eines Kombinations Felds im Begriff ist, geänderten Text anzuzeigen.
ms.assetid: cae9cbf5-d420-4dfb-a46f-8c1a77de6ecf
keywords:
- Windows-Steuerelemente für CBN_EDITUPDATE Benachrichtigungs
topic_type:
- apiref
api_name:
- CBN_EDITUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ef56b97bf8f4c4aebb4a11383be1b5a1941167b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106286"
---
# <a name="cbn_editupdate-notification-code"></a><span data-ttu-id="e2660-104">CBN- \_ editupdate-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="e2660-104">CBN\_EDITUPDATE notification code</span></span>

<span data-ttu-id="e2660-105">Wird gesendet, wenn der Bearbeitungs Steuerungs Bereich eines Kombinations Felds im Begriff ist, geänderten Text anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e2660-105">Sent when the edit control portion of a combo box is about to display altered text.</span></span> <span data-ttu-id="e2660-106">Dieser Benachrichtigungs Code wird gesendet, nachdem das Steuerelement den Text formatiert hat, aber bevor der Text angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e2660-106">This notification code is sent after the control has formatted the text, but before it displays the text.</span></span> <span data-ttu-id="e2660-107">Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="e2660-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_EDITUPDATE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e2660-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2660-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2660-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2660-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2660-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner des Kombinations Felds.</span><span class="sxs-lookup"><span data-stu-id="e2660-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="e2660-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="e2660-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="e2660-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2660-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2660-113">Handle für das Kombinations Feld.</span><span class="sxs-lookup"><span data-stu-id="e2660-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2660-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2660-114">Remarks</span></span>

<span data-ttu-id="e2660-115">Wenn das Kombinations Feld den " [**CBS \_ DropDownList**](combo-box-styles.md) "-Stil hat, wird dieser Benachrichtigungs Code nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="e2660-115">If the combo box has the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, this notification code is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2660-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2660-116">Requirements</span></span>



| <span data-ttu-id="e2660-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2660-117">Requirement</span></span> | <span data-ttu-id="e2660-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e2660-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2660-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2660-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e2660-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2660-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e2660-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2660-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e2660-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2660-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e2660-123">Header</span><span class="sxs-lookup"><span data-stu-id="e2660-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2660-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="e2660-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2660-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2660-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="e2660-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="e2660-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e2660-127">CBN- \_ EditChange</span><span class="sxs-lookup"><span data-stu-id="e2660-127">CBN\_EDITCHANGE</span></span>](cbn-editchange.md)
</dt> <dt>

<span data-ttu-id="e2660-128">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="e2660-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="e2660-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e2660-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="e2660-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e2660-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e2660-131">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="e2660-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

