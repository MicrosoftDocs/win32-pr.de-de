---
title: CBN_EDITCHANGE Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, nachdem der Benutzer eine Aktion ausgeführt hat, die möglicherweise den Text im Bearbeitungs Steuerelement-Teil eines Kombinations Felds geändert hat.
ms.assetid: 2c5de5cd-24d3-4198-906e-b520369e0f61
keywords:
- Windows-Steuerelemente für CBN_EDITCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- CBN_EDITCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a661d647d0879b93675563777d77bba2dfe8c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346536"
---
# <a name="cbn_editchange-notification-code"></a><span data-ttu-id="9f6a8-104">CBN- \_ EditChange-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="9f6a8-104">CBN\_EDITCHANGE notification code</span></span>

<span data-ttu-id="9f6a8-105">Wird gesendet, nachdem der Benutzer eine Aktion ausgeführt hat, die möglicherweise den Text im Bearbeitungs Steuerelement-Teil eines Kombinations Felds geändert hat.</span><span class="sxs-lookup"><span data-stu-id="9f6a8-105">Sent after the user has taken an action that may have altered the text in the edit control portion of a combo box.</span></span> <span data-ttu-id="9f6a8-106">Im Gegensatz zum [CBN- \_ editupdate](cbn-editupdate.md) -Benachrichtigungs Code wird dieser Benachrichtigungs Code gesendet, nachdem das System den Bildschirm aktualisiert hat.</span><span class="sxs-lookup"><span data-stu-id="9f6a8-106">Unlike the [CBN\_EDITUPDATE](cbn-editupdate.md) notification code, this notification code is sent after the system updates the screen.</span></span> <span data-ttu-id="9f6a8-107">Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="9f6a8-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_EDITCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9f6a8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f6a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f6a8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f6a8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f6a8-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner des Kombinations Felds.</span><span class="sxs-lookup"><span data-stu-id="9f6a8-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="9f6a8-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="9f6a8-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="9f6a8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f6a8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f6a8-113">Handle für das Kombinations Feld.</span><span class="sxs-lookup"><span data-stu-id="9f6a8-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f6a8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f6a8-114">Remarks</span></span>

<span data-ttu-id="9f6a8-115">Wenn das Kombinations Feld den " [**CBS \_ DropDownList**](combo-box-styles.md) "-Stil hat, wird dieser Benachrichtigungs Code nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="9f6a8-115">If the combo box has the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, this notification code is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f6a8-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f6a8-116">Requirements</span></span>



| <span data-ttu-id="9f6a8-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f6a8-117">Requirement</span></span> | <span data-ttu-id="9f6a8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9f6a8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f6a8-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f6a8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9f6a8-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f6a8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9f6a8-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f6a8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9f6a8-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f6a8-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9f6a8-123">Header</span><span class="sxs-lookup"><span data-stu-id="9f6a8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f6a8-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="9f6a8-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f6a8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f6a8-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="9f6a8-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9f6a8-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9f6a8-127">CBN- \_ editupdate</span><span class="sxs-lookup"><span data-stu-id="9f6a8-127">CBN\_EDITUPDATE</span></span>](cbn-editupdate.md)
</dt> <dt>

<span data-ttu-id="9f6a8-128">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="9f6a8-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="9f6a8-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9f6a8-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="9f6a8-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9f6a8-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9f6a8-131">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="9f6a8-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

