---
title: BN_SETFOCUS Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn eine Schaltfläche den Tastaturfokus erhält. Die Schaltfläche muss den Typ "b Benachrichtigen" aufweisen \_ , um diesen Benachrichtigungs Code zu senden. Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: 6b8d9bde-67f9-454f-ba2c-e5c8d9ff2709
keywords:
- Windows-Steuerelemente für BN_SETFOCUS Benachrichtigungs
topic_type:
- apiref
api_name:
- BN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eb9204f5b23b62b6cee9fb2652a16d546f6ef62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339944"
---
# <a name="bn_setfocus-notification-code"></a><span data-ttu-id="d3afd-106">BN- \_ SetFocus-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="d3afd-106">BN\_SETFOCUS notification code</span></span>

<span data-ttu-id="d3afd-107">Wird gesendet, wenn eine Schaltfläche den Tastaturfokus erhält.</span><span class="sxs-lookup"><span data-stu-id="d3afd-107">Sent when a button receives the keyboard focus.</span></span> <span data-ttu-id="d3afd-108">Die Schaltfläche muss den Typ " [**b \_ Benachrichtigen**](button-styles.md) " aufweisen, um diesen Benachrichtigungs Code zu senden.</span><span class="sxs-lookup"><span data-stu-id="d3afd-108">The button must have the [**BS\_NOTIFY**](button-styles.md) style to send this notification code.</span></span>

<span data-ttu-id="d3afd-109">Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="d3afd-109">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d3afd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3afd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3afd-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3afd-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3afd-112">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="d3afd-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="d3afd-113">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="d3afd-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d3afd-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3afd-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3afd-115">Ein Handle für die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="d3afd-115">A handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3afd-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3afd-116">Requirements</span></span>



| <span data-ttu-id="d3afd-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3afd-117">Requirement</span></span> | <span data-ttu-id="d3afd-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d3afd-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3afd-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3afd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d3afd-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3afd-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d3afd-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3afd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d3afd-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3afd-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d3afd-123">Header</span><span class="sxs-lookup"><span data-stu-id="d3afd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3afd-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="d3afd-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3afd-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3afd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3afd-126">BN- \_ killfokus</span><span class="sxs-lookup"><span data-stu-id="d3afd-126">BN\_KILLFOCUS</span></span>](bn-killfocus.md)
</dt> </dl>

 

