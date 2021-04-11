---
title: BN_DBLCLK Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer auf eine Schaltfläche doppelklickt.
ms.assetid: 60cc033f-8b84-4aa5-b625-fdee9deb4757
keywords:
- Windows-Steuerelemente für BN_DBLCLK Benachrichtigungs
topic_type:
- apiref
api_name:
- BN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f04c6bf52e213056d85d3a6d038bedb83754a27e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040373"
---
# <a name="bn_dblclk-notification-code"></a><span data-ttu-id="5ce2b-104">Mrd. \_ dblclk-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="5ce2b-104">BN\_DBLCLK notification code</span></span>

<span data-ttu-id="5ce2b-105">Wird gesendet, wenn der Benutzer auf eine Schaltfläche doppelklickt.</span><span class="sxs-lookup"><span data-stu-id="5ce2b-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="5ce2b-106">Dieser Benachrichtigungs Code wird automatisch für die Schaltflächen " [**\_ Benutzer Schaltfläche**](button-styles.md)", " [**SB \_ RadioButton**](button-styles.md)" und " [**b \_**](button-styles.md)</span><span class="sxs-lookup"><span data-stu-id="5ce2b-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="5ce2b-107">Andere Schaltflächen Typen senden \_ nur dann eine Milliarde dblclk, wenn Sie über das Format "Schriftarten [**\_ Benachrichtigen**](button-styles.md) " verfügen</span><span class="sxs-lookup"><span data-stu-id="5ce2b-107">Other button types send BN\_DBLCLK only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="5ce2b-108">Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="5ce2b-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DBLCLK

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="5ce2b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ce2b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ce2b-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5ce2b-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ce2b-111">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="5ce2b-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="5ce2b-112">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="5ce2b-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="5ce2b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ce2b-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ce2b-114">Ein Handle für die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="5ce2b-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ce2b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ce2b-115">Remarks</span></span>

<span data-ttu-id="5ce2b-116">Der BN- \_ dblclk-Wert ist identisch mit dem über die [Milliarde \_ doublegeklickt](bn-doubleclicked.md) -Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="5ce2b-116">BN\_DBLCLK is the same as the [BN\_DOUBLECLICKED](bn-doubleclicked.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ce2b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ce2b-117">Requirements</span></span>



| <span data-ttu-id="5ce2b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ce2b-118">Requirement</span></span> | <span data-ttu-id="5ce2b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5ce2b-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ce2b-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ce2b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5ce2b-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ce2b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5ce2b-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ce2b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5ce2b-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ce2b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5ce2b-124">Header</span><span class="sxs-lookup"><span data-stu-id="5ce2b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ce2b-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="5ce2b-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ce2b-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ce2b-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="5ce2b-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="5ce2b-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5ce2b-128">auf BN \_ geklickt</span><span class="sxs-lookup"><span data-stu-id="5ce2b-128">BN\_CLICKED</span></span>](bn-clicked.md)
</dt> <dt>

[<span data-ttu-id="5ce2b-129">BN- \_ Doppelklick</span><span class="sxs-lookup"><span data-stu-id="5ce2b-129">BN\_DOUBLECLICKED</span></span>](bn-doubleclicked.md)
</dt> <dt>

<span data-ttu-id="5ce2b-130">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="5ce2b-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5ce2b-131">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="5ce2b-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

