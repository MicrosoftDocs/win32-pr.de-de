---
title: BN_PUSHED Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der pushzustand einer Schaltfläche auf Push festgelegt ist.
ms.assetid: 34000def-189c-4a37-bcef-4ca09a67df00
keywords:
- Windows-Steuerelemente für BN_PUSHED Benachrichtigungs
topic_type:
- apiref
api_name:
- BN_PUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18a27599c770eb55d889a21956312512ca804cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340507"
---
# <a name="bn_pushed-notification-code"></a><span data-ttu-id="b6ae2-104">Milliarde- \_ Pushbenachrichtigung-Code</span><span class="sxs-lookup"><span data-stu-id="b6ae2-104">BN\_PUSHED notification code</span></span>

<span data-ttu-id="b6ae2-105">Wird gesendet, wenn der pushzustand einer Schaltfläche auf Push festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-105">Sent when the push state of a button is set to pushed.</span></span>

> [!Note]  
> <span data-ttu-id="b6ae2-106">Dieser Benachrichtigungs Code wird nur für die Kompatibilität mit 16-Bit-Versionen von Windows vor Version 3,0 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="b6ae2-107">Anwendungen sollten für diese [**Aufgabe \_ den Schrift**](button-styles.md) Schnitt-Stil und die [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur des s verwenden.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="b6ae2-108">Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_PUSHED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b6ae2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6ae2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6ae2-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6ae2-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6ae2-111">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="b6ae2-112">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="b6ae2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6ae2-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6ae2-114">Ein Handle für die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="b6ae2-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6ae2-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6ae2-115">Remarks</span></span>

<span data-ttu-id="b6ae2-116">Der Wert für die Übertragung von BN \_ ist mit dem [Milliarden- \_ Hilite](bn-hilite.md) -Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="b6ae2-116">BN\_PUSHED is the same as the [BN\_HILITE](bn-hilite.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6ae2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6ae2-117">Requirements</span></span>



| <span data-ttu-id="b6ae2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6ae2-118">Requirement</span></span> | <span data-ttu-id="b6ae2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b6ae2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ae2-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6ae2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b6ae2-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6ae2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b6ae2-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6ae2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b6ae2-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6ae2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b6ae2-124">Header</span><span class="sxs-lookup"><span data-stu-id="b6ae2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6ae2-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="b6ae2-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6ae2-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6ae2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ae2-127">**Milliarde \_ nicht per pushübertragung**</span><span class="sxs-lookup"><span data-stu-id="b6ae2-127">**BN\_UNPUSHED**</span></span>](bn-unpushed.md)
</dt> </dl>

 

