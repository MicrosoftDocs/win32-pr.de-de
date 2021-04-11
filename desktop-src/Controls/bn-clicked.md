---
title: BN_CLICKED Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer auf eine Schaltfläche klickt. Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: 74847549-b92f-4981-a979-d0b2a8a5539a
keywords:
- Windows-Steuerelemente für BN_CLICKED Benachrichtigungs
topic_type:
- apiref
api_name:
- BN_CLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 894837c9a930c6a5f6d124b6b9e983465ef3beac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103234"
---
# <a name="bn_clicked-notification-code"></a><span data-ttu-id="2f621-105">In der Milliarde \_ angeklickte Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="2f621-105">BN\_CLICKED notification code</span></span>

<span data-ttu-id="2f621-106">Wird gesendet, wenn der Benutzer auf eine Schaltfläche klickt.</span><span class="sxs-lookup"><span data-stu-id="2f621-106">Sent when the user clicks a button.</span></span>

<span data-ttu-id="2f621-107">Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="2f621-107">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_CLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="2f621-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f621-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f621-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f621-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f621-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="2f621-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="2f621-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="2f621-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="2f621-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f621-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f621-113">Ein Handle für die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="2f621-113">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f621-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f621-114">Remarks</span></span>

<span data-ttu-id="2f621-115">Eine deaktivierte Schaltfläche sendet keinen \_ an das übergeordneten Fenster angeklickten Wert für die Anzeige von BN</span><span class="sxs-lookup"><span data-stu-id="2f621-115">A disabled button does not send a BN\_CLICKED notification code to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f621-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f621-116">Requirements</span></span>



| <span data-ttu-id="2f621-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f621-117">Requirement</span></span> | <span data-ttu-id="2f621-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2f621-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f621-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f621-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2f621-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f621-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2f621-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f621-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2f621-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f621-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2f621-123">Header</span><span class="sxs-lookup"><span data-stu-id="2f621-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f621-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="2f621-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f621-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f621-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="2f621-126">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="2f621-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="2f621-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2f621-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="2f621-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2f621-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2f621-129">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="2f621-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

