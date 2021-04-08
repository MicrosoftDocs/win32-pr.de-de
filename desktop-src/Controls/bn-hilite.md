---
title: BN_HILITE Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer eine Schaltfläche auswählt.
ms.assetid: f20ba77e-257c-44ec-a2dd-dbf23cd78d07
keywords:
- Windows-Steuerelemente für BN_HILITE Benachrichtigungs
topic_type:
- apiref
api_name:
- BN_HILITE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5567837c9883c52d99f0ca68d450f7b3538f233b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949599"
---
# <a name="bn_hilite-notification-code"></a><span data-ttu-id="0ba6a-104">BN- \_ Hilite-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="0ba6a-104">BN\_HILITE notification code</span></span>

<span data-ttu-id="0ba6a-105">Wird gesendet, wenn der Benutzer eine Schaltfläche auswählt.</span><span class="sxs-lookup"><span data-stu-id="0ba6a-105">Sent when the user selects a button.</span></span>

> [!Note]  
> <span data-ttu-id="0ba6a-106">Dieser Benachrichtigungs Code wird nur für die Kompatibilität mit 16-Bit-Versionen von Windows vor Version 3,0 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="0ba6a-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="0ba6a-107">Anwendungen sollten für diese [**Aufgabe \_ den Schrift**](button-styles.md) Schnitt-Stil und die [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur des s verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ba6a-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="0ba6a-108">Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="0ba6a-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_HILITE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="0ba6a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ba6a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ba6a-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0ba6a-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ba6a-111">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="0ba6a-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="0ba6a-112">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="0ba6a-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="0ba6a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ba6a-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ba6a-114">Handle für die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="0ba6a-114">Handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ba6a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ba6a-115">Remarks</span></span>

<span data-ttu-id="0ba6a-116">Der BN-Hilite-Wert ist identisch mit dem von der Übertragung übertragenen \_ Benachrichtigungs Code [ \_ ](bn-pushed.md)</span><span class="sxs-lookup"><span data-stu-id="0ba6a-116">BN\_HILITE is the same as the [BN\_PUSHED](bn-pushed.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ba6a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ba6a-117">Requirements</span></span>



| <span data-ttu-id="0ba6a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ba6a-118">Requirement</span></span> | <span data-ttu-id="0ba6a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0ba6a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ba6a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ba6a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0ba6a-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ba6a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0ba6a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ba6a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0ba6a-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ba6a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0ba6a-124">Header</span><span class="sxs-lookup"><span data-stu-id="0ba6a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ba6a-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba6a-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

