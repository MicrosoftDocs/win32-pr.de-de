---
title: CBN_SELCHANGE Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer die aktuelle Auswahl im Listenfeld eines Kombinations Felds ändert.
ms.assetid: 2d0d711c-dfc4-485b-97bb-9ccfa7c5864b
keywords:
- Windows-Steuerelemente für CBN_SELCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- CBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e921b7856780763923a448e42de072476cc02f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957190"
---
# <a name="cbn_selchange-notification-code"></a><span data-ttu-id="61add-104">CBN- \_ selChange-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="61add-104">CBN\_SELCHANGE notification code</span></span>

<span data-ttu-id="61add-105">Wird gesendet, wenn der Benutzer die aktuelle Auswahl im Listenfeld eines Kombinations Felds ändert.</span><span class="sxs-lookup"><span data-stu-id="61add-105">Sent when the user changes the current selection in the list box of a combo box.</span></span> <span data-ttu-id="61add-106">Der Benutzer kann die Auswahl ändern, indem er im Listenfeld oder mithilfe der Pfeiltasten klickt.</span><span class="sxs-lookup"><span data-stu-id="61add-106">The user can change the selection by clicking in the list box or by using the arrow keys.</span></span> <span data-ttu-id="61add-107">Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code in Form einer [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="61add-107">The parent window of the combo box receives this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="61add-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="61add-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61add-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="61add-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61add-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner des Kombinations Felds.</span><span class="sxs-lookup"><span data-stu-id="61add-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="61add-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="61add-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="61add-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61add-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61add-113">Handle für das Kombinations Feld.</span><span class="sxs-lookup"><span data-stu-id="61add-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61add-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61add-114">Remarks</span></span>

<span data-ttu-id="61add-115">Um den Index der aktuellen Auswahl zu erhalten, senden Sie die [**CB \_ getcurrsel**](cb-getcursel.md) -Nachricht an das-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="61add-115">To get the index of the current selection, send the [**CB\_GETCURSEL**](cb-getcursel.md) message to the control.</span></span>

<span data-ttu-id="61add-116">Der CBN \_ selChange-Benachrichtigungs Code wird nicht gesendet, wenn die aktuelle Auswahl mithilfe der [**CB- \_ setcurrsel**](cb-setcursel.md) -Nachricht festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="61add-116">The CBN\_SELCHANGE notification code is not sent when the current selection is set using the [**CB\_SETCURSEL**](cb-setcursel.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="61add-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61add-117">Requirements</span></span>



| <span data-ttu-id="61add-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61add-118">Requirement</span></span> | <span data-ttu-id="61add-119">Wert</span><span class="sxs-lookup"><span data-stu-id="61add-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61add-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61add-120">Minimum supported client</span></span><br/> | <span data-ttu-id="61add-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61add-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="61add-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61add-122">Minimum supported server</span></span><br/> | <span data-ttu-id="61add-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61add-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="61add-124">Header</span><span class="sxs-lookup"><span data-stu-id="61add-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="61add-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="61add-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61add-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61add-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="61add-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="61add-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="61add-128">CBN- \_ Schließung</span><span class="sxs-lookup"><span data-stu-id="61add-128">CBN\_CLOSEUP</span></span>](cbn-closeup.md)
</dt> <dt>

[<span data-ttu-id="61add-129">CBN- \_ dblclk</span><span class="sxs-lookup"><span data-stu-id="61add-129">CBN\_DBLCLK</span></span>](cbn-dblclk.md)
</dt> <dt>

[<span data-ttu-id="61add-130">**CB \_ getcurrsel**</span><span class="sxs-lookup"><span data-stu-id="61add-130">**CB\_GETCURSEL**</span></span>](cb-getcursel.md)
</dt> <dt>

[<span data-ttu-id="61add-131">**CB \_ setcurrsel**</span><span class="sxs-lookup"><span data-stu-id="61add-131">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> <dt>

<span data-ttu-id="61add-132">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="61add-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="61add-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="61add-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="61add-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="61add-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="61add-135">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="61add-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

