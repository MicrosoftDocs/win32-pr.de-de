---
title: BN_KILLFOCUS Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn eine Schaltfläche den Tastaturfokus verliert. Die Schaltfläche muss den Typ "b Benachrichtigen" aufweisen \_ , um diesen Benachrichtigungs Code zu senden. Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: 740154ba-47fd-4084-8b86-6166f1e1b39f
keywords:
- Windows-Steuerelemente für BN_KILLFOCUS Benachrichtigungs
topic_type:
- apiref
api_name:
- BN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3fb6737d88ccddedbba6db58ffd0f713da7a8a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475753"
---
# <a name="bn_killfocus-notification-code"></a><span data-ttu-id="bae64-106">BN- \_ killfokus-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="bae64-106">BN\_KILLFOCUS notification code</span></span>

<span data-ttu-id="bae64-107">Wird gesendet, wenn eine Schaltfläche den Tastaturfokus verliert.</span><span class="sxs-lookup"><span data-stu-id="bae64-107">Sent when a button loses the keyboard focus.</span></span> <span data-ttu-id="bae64-108">Die Schaltfläche muss den Typ " [**b \_ Benachrichtigen**](button-styles.md) " aufweisen, um diesen Benachrichtigungs Code zu senden.</span><span class="sxs-lookup"><span data-stu-id="bae64-108">The button must have the [**BS\_NOTIFY**](button-styles.md) style to send this notification code.</span></span>

<span data-ttu-id="bae64-109">Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="bae64-109">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="bae64-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bae64-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bae64-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bae64-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bae64-112">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="bae64-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="bae64-113">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="bae64-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="bae64-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bae64-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bae64-115">Ein Handle für die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="bae64-115">A handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bae64-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bae64-116">Requirements</span></span>



| <span data-ttu-id="bae64-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bae64-117">Requirement</span></span> | <span data-ttu-id="bae64-118">Wert</span><span class="sxs-lookup"><span data-stu-id="bae64-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bae64-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bae64-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bae64-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bae64-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bae64-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bae64-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bae64-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bae64-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bae64-123">Header</span><span class="sxs-lookup"><span data-stu-id="bae64-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bae64-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="bae64-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bae64-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bae64-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bae64-126">BN- \_ SetFocus</span><span class="sxs-lookup"><span data-stu-id="bae64-126">BN\_SETFOCUS</span></span>](bn-setfocus.md)
</dt> </dl>

 

