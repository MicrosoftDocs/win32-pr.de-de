---
title: LBN_SELCHANGE Benachrichtigungs Code (Winuser. h)
description: Benachrichtigt die Anwendung, dass sich die Auswahl in einem Listenfeld aufgrund von Benutzereingaben geändert hat. Das übergeordnete Fenster des Listen Felds empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: 126d2c47-816e-4179-a870-f5c5a34c5513
keywords:
- Windows-Steuerelemente für LBN_SELCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- LBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e029d1753a0fa74f39a59a459d6ede45811a40fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741569"
---
# <a name="lbn_selchange-notification-code"></a><span data-ttu-id="8ce87-105">LBN \_ selChange-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="8ce87-105">LBN\_SELCHANGE notification code</span></span>

<span data-ttu-id="8ce87-106">Benachrichtigt die Anwendung, dass sich die Auswahl in einem Listenfeld aufgrund von Benutzereingaben geändert hat.</span><span class="sxs-lookup"><span data-stu-id="8ce87-106">Notifies the application that the selection in a list box has changed as a result of user input.</span></span> <span data-ttu-id="8ce87-107">Das übergeordnete Fenster des Listen Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="8ce87-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8ce87-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ce87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ce87-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8ce87-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ce87-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Listen Felds.</span><span class="sxs-lookup"><span data-stu-id="8ce87-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="8ce87-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="8ce87-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="8ce87-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ce87-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ce87-113">Handle für das Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="8ce87-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ce87-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ce87-114">Remarks</span></span>

<span data-ttu-id="8ce87-115">Dieser Benachrichtigungs Code wird nur von einem Listenfeld gesendet, das über den [**lbs- \_ Benachrichtigungs**](list-box-styles.md) Stil verfügt.</span><span class="sxs-lookup"><span data-stu-id="8ce87-115">This notification code is sent only by a list box that has the [**LBS\_NOTIFY**](list-box-styles.md) style.</span></span>

<span data-ttu-id="8ce87-116">Dieser Benachrichtigungs Code wird nicht gesendet, wenn die Auswahl durch die Nachricht [**lb \_ SetSel**](lb-setsel.md), [**lb \_ setcurrsel**](lb-setcursel.md), [**lb \_ SelectString**](lb-selectstring.md), [**lb \_ selitemrange**](lb-selitemrange.md) oder [**lb \_ selitemrangeex**](lb-selitemrangeex.md) geändert wird.</span><span class="sxs-lookup"><span data-stu-id="8ce87-116">This notification code is not sent if the [**LB\_SETSEL**](lb-setsel.md), [**LB\_SETCURSEL**](lb-setcursel.md), [**LB\_SELECTSTRING**](lb-selectstring.md), [**LB\_SELITEMRANGE**](lb-selitemrange.md) or [**LB\_SELITEMRANGEEX**](lb-selitemrangeex.md) message changes the selection.</span></span>

<span data-ttu-id="8ce87-117">Bei einem Listenfeld mit Mehrfachauswahl wird der LBN \_ selChange-Benachrichtigungs Code immer dann gesendet, wenn der Benutzer eine Pfeiltaste drückt, auch wenn sich die Auswahl nicht ändert.</span><span class="sxs-lookup"><span data-stu-id="8ce87-117">For a multiple-selection list box, the LBN\_SELCHANGE notification code is sent whenever the user presses an arrow key, even if the selection does not change.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ce87-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ce87-118">Requirements</span></span>



| <span data-ttu-id="8ce87-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ce87-119">Requirement</span></span> | <span data-ttu-id="8ce87-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8ce87-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ce87-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8ce87-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8ce87-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ce87-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8ce87-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8ce87-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8ce87-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ce87-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8ce87-125">Header</span><span class="sxs-lookup"><span data-stu-id="8ce87-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ce87-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="8ce87-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ce87-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ce87-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="8ce87-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="8ce87-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8ce87-129">**LB- \_ setcurrsel**</span><span class="sxs-lookup"><span data-stu-id="8ce87-129">**LB\_SETCURSEL**</span></span>](lb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="8ce87-130">LBN- \_ dblclk</span><span class="sxs-lookup"><span data-stu-id="8ce87-130">LBN\_DBLCLK</span></span>](lbn-dblclk.md)
</dt> <dt>

[<span data-ttu-id="8ce87-131">LBN \_ selcancel</span><span class="sxs-lookup"><span data-stu-id="8ce87-131">LBN\_SELCANCEL</span></span>](lbn-selcancel.md)
</dt> <dt>

<span data-ttu-id="8ce87-132">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="8ce87-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="8ce87-133">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="8ce87-133">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

