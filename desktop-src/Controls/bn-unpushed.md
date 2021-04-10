---
title: BN_UNPUSHED Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der pushzustand einer Schaltfläche auf nicht per Push übertragen festgelegt ist.
ms.assetid: 1ae7311d-f067-41fe-a117-e0c70d239e9d
keywords:
- Windows-Steuerelemente für BN_UNPUSHED Benachrichtigungs
topic_type:
- apiref
api_name:
- BN_UNPUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eb8c16d8860274c070c31910254311a897c0f1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103127"
---
# <a name="bn_unpushed-notification-code"></a><span data-ttu-id="95e29-104">BN- \_ Benachrichtigungs Code ohne pushübertragung</span><span class="sxs-lookup"><span data-stu-id="95e29-104">BN\_UNPUSHED notification code</span></span>

<span data-ttu-id="95e29-105">Wird gesendet, wenn der pushzustand einer Schaltfläche auf nicht per Push übertragen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="95e29-105">Sent when the push state of a button is set to unpushed.</span></span>

> [!Note]  
> <span data-ttu-id="95e29-106">Dieser Benachrichtigungs Code wird nur für die Kompatibilität mit 16-Bit-Versionen von Windows vor Version 3,0 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="95e29-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="95e29-107">Anwendungen sollten für diese [**Aufgabe \_ den Schrift**](button-styles.md) Schnitt-Stil und die [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur des s verwenden.</span><span class="sxs-lookup"><span data-stu-id="95e29-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="95e29-108">Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="95e29-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_UNPUSHED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="95e29-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="95e29-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95e29-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95e29-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95e29-111">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="95e29-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="95e29-112">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="95e29-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="95e29-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95e29-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95e29-114">Ein Handle für die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="95e29-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95e29-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95e29-115">Remarks</span></span>

<span data-ttu-id="95e29-116">Der Wert von ' BN ' \_ ist mit dem [Milliarden- \_ unhilite](bn-unhilite.md) -Benachrichtigungs Code identisch.</span><span class="sxs-lookup"><span data-stu-id="95e29-116">BN\_UNPUSHED is the same as the [BN\_UNHILITE](bn-unhilite.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="95e29-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95e29-117">Requirements</span></span>



| <span data-ttu-id="95e29-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95e29-118">Requirement</span></span> | <span data-ttu-id="95e29-119">Wert</span><span class="sxs-lookup"><span data-stu-id="95e29-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95e29-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95e29-120">Minimum supported client</span></span><br/> | <span data-ttu-id="95e29-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95e29-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="95e29-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95e29-122">Minimum supported server</span></span><br/> | <span data-ttu-id="95e29-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95e29-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="95e29-124">Header</span><span class="sxs-lookup"><span data-stu-id="95e29-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="95e29-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="95e29-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95e29-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95e29-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95e29-127">BN per \_ pushübertragung</span><span class="sxs-lookup"><span data-stu-id="95e29-127">BN\_PUSHED</span></span>](bn-pushed.md)
</dt> </dl>

 

