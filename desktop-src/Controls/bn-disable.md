---
title: BN_DISABLE Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn eine Schaltfläche deaktiviert ist.
ms.assetid: 5e2bb434-f20d-42f1-a9e9-46c4d10b8c7e
keywords:
- Windows-Steuerelemente für BN_DISABLE Benachrichtigungs
topic_type:
- apiref
api_name:
- BN_DISABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faaba622c056366fe0c49683adc2c020a6302929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949600"
---
# <a name="bn_disable-notification-code"></a><span data-ttu-id="e144d-104">BN \_ Deaktivieren des Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="e144d-104">BN\_DISABLE notification code</span></span>

<span data-ttu-id="e144d-105">Wird gesendet, wenn eine Schaltfläche deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e144d-105">Sent when a button is disabled.</span></span>

> [!Note]  
> <span data-ttu-id="e144d-106">Dieser Benachrichtigungs Code wird nur für die Kompatibilität mit 16-Bit-Versionen von Windows vor Version 3,0 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e144d-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="e144d-107">Anwendungen sollten für diese [**Aufgabe \_ den Schrift**](button-styles.md) Schnitt-Stil und die [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur des s verwenden.</span><span class="sxs-lookup"><span data-stu-id="e144d-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="e144d-108">Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="e144d-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DISABLE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="e144d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e144d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e144d-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e144d-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e144d-111">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="e144d-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="e144d-112">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="e144d-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="e144d-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e144d-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e144d-114">Handle für die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="e144d-114">Handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e144d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e144d-115">Requirements</span></span>



| <span data-ttu-id="e144d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e144d-116">Requirement</span></span> | <span data-ttu-id="e144d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e144d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e144d-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e144d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e144d-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e144d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e144d-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e144d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e144d-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e144d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e144d-122">Header</span><span class="sxs-lookup"><span data-stu-id="e144d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e144d-123"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="e144d-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

