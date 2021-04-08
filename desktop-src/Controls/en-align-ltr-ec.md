---
title: EN_ALIGN_LTR_EC Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer die Richtung des Bearbeitungs Steuer Elements in von links nach rechts geändert hat. Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine WM- \_ Befehls Meldung.
ms.assetid: 231f9d00-c5a5-445e-9176-201fe1c14a0e
keywords:
- Windows-Steuerelemente für EN_ALIGN_LTR_EC Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_ALIGN_LTR_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4886c68a024005c4b2fddd71e1480b0a3545bdf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740992"
---
# <a name="en_align_ltr_ec-notification-code"></a><span data-ttu-id="bda2f-105">EN \_ Ausrichten des \_ Ltr- \_ EC-Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="bda2f-105">EN\_ALIGN\_LTR\_EC notification code</span></span>

<span data-ttu-id="bda2f-106">Wird gesendet, wenn der Benutzer die Richtung des Bearbeitungs Steuer Elements in von links nach rechts geändert hat.</span><span class="sxs-lookup"><span data-stu-id="bda2f-106">Sent when the user has changed the edit control direction to left-to-right.</span></span> <span data-ttu-id="bda2f-107">Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="bda2f-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ALIGN_LTR_EC

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="bda2f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bda2f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bda2f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bda2f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bda2f-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="bda2f-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="bda2f-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="bda2f-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="bda2f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bda2f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bda2f-113">Ein Handle für das Bearbeitungs Steuerelement, das den Benachrichtigungs Code sendet.</span><span class="sxs-lookup"><span data-stu-id="bda2f-113">A handle to the edit control sending the notification code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bda2f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bda2f-114">Remarks</span></span>

<span data-ttu-id="bda2f-115">Wenn eine bidirektionale Sprache auf dem System installiert ist (z. b. Arabisch oder Hebräisch), können Sie die Bearbeitungs Steuerelement-Richtung mithilfe von STRG + LShift (von links nach rechts) und STRG + rshift (von rechts nach links) ändern.</span><span class="sxs-lookup"><span data-stu-id="bda2f-115">If there is a bidirectional language installed on your system, for example, Arabic or Hebrew, you can change the edit control direction using CTRL+LSHIFT (for left to right) and CTRL+RSHIFT (for right to left).</span></span>

<span data-ttu-id="bda2f-116">Umfassende **Bearbeitung:** Dieser Benachrichtigungs Code wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bda2f-116">**Rich Edit:** This notification code is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="bda2f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bda2f-117">Requirements</span></span>



| <span data-ttu-id="bda2f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bda2f-118">Requirement</span></span> | <span data-ttu-id="bda2f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="bda2f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bda2f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bda2f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bda2f-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bda2f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bda2f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bda2f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bda2f-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bda2f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bda2f-124">Header</span><span class="sxs-lookup"><span data-stu-id="bda2f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bda2f-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="bda2f-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bda2f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bda2f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bda2f-127">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="bda2f-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

