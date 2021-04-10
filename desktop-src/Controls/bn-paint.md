---
title: BN_PAINT Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn eine Schaltfläche gezeichnet werden soll.
ms.assetid: 1c742272-60bb-42f1-a9b3-974e9a8540cd
keywords:
- Windows-Steuerelemente für BN_PAINT Benachrichtigungs
topic_type:
- apiref
api_name:
- BN_PAINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f142c0c502d92933bf7bbc9cb01e3062c8bba96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040114"
---
# <a name="bn_paint-notification-code"></a><span data-ttu-id="54062-104">Milliarden- \_ Paint-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="54062-104">BN\_PAINT notification code</span></span>

<span data-ttu-id="54062-105">Wird gesendet, wenn eine Schaltfläche gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="54062-105">Sent when a button should be painted.</span></span>

> [!Note]  
> <span data-ttu-id="54062-106">Dieser Benachrichtigungs Code wird nur für die Kompatibilität mit 16-Bit-Versionen von Windows vor Version 3,0 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="54062-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="54062-107">Anwendungen sollten für diese [**Aufgabe \_ den Schrift**](button-styles.md) Schnitt-Stil und die [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur des s verwenden.</span><span class="sxs-lookup"><span data-stu-id="54062-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="54062-108">Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="54062-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_PAINT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="54062-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="54062-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54062-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54062-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54062-111">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="54062-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="54062-112">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="54062-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="54062-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54062-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54062-114">Ein Handle für die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="54062-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="54062-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54062-115">Requirements</span></span>



| <span data-ttu-id="54062-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54062-116">Requirement</span></span> | <span data-ttu-id="54062-117">Wert</span><span class="sxs-lookup"><span data-stu-id="54062-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54062-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54062-118">Minimum supported client</span></span><br/> | <span data-ttu-id="54062-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54062-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="54062-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54062-120">Minimum supported server</span></span><br/> | <span data-ttu-id="54062-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54062-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="54062-122">Header</span><span class="sxs-lookup"><span data-stu-id="54062-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="54062-123"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="54062-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

