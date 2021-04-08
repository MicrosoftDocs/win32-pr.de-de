---
title: BN_UNHILITE Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn die Hervorhebung aus einer Schaltfläche entfernt werden soll.
ms.assetid: 9839a55b-9e9c-4c9c-8e92-347007ea27be
keywords:
- Windows-Steuerelemente für BN_UNHILITE Benachrichtigungs
topic_type:
- apiref
api_name:
- BN_UNHILITE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395901548103a7a678b4873e1fde52e259297ebb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949549"
---
# <a name="bn_unhilite-notification-code"></a><span data-ttu-id="5ce5a-104">Milliarden- \_ unhilite-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="5ce5a-104">BN\_UNHILITE notification code</span></span>

<span data-ttu-id="5ce5a-105">Wird gesendet, wenn die Hervorhebung aus einer Schaltfläche entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ce5a-105">Sent when the highlight should be removed from a button.</span></span>

> [!Note]  
> <span data-ttu-id="5ce5a-106">Dieser Benachrichtigungs Code wird nur für die Kompatibilität mit 16-Bit-Versionen von Windows vor Version 3,0 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5ce5a-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="5ce5a-107">Anwendungen sollten für diese [**Aufgabe \_ den Schrift**](button-styles.md) Schnitt-Stil und die [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur des s verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ce5a-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="5ce5a-108">Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="5ce5a-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_UNHILITE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5ce5a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ce5a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ce5a-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5ce5a-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ce5a-111">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="5ce5a-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="5ce5a-112">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="5ce5a-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="5ce5a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ce5a-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ce5a-114">Ein Handle für die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="5ce5a-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ce5a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ce5a-115">Remarks</span></span>

<span data-ttu-id="5ce5a-116">Der BN- \_ unhilite-Wert ist identisch mit dem [nicht per \_ pushcode verwalteten](bn-unpushed.md) Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="5ce5a-116">BN\_UNHILITE is the same as the [BN\_UNPUSHED](bn-unpushed.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ce5a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ce5a-117">Requirements</span></span>



| <span data-ttu-id="5ce5a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ce5a-118">Requirement</span></span> | <span data-ttu-id="5ce5a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5ce5a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ce5a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ce5a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5ce5a-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ce5a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5ce5a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ce5a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5ce5a-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ce5a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5ce5a-124">Header</span><span class="sxs-lookup"><span data-stu-id="5ce5a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ce5a-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="5ce5a-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

