---
title: EN_ALIGNRTL Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass die Absatz Richtung von rechts nach links geändert wurde. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM- \_ Befehls Meldung.
ms.assetid: 2db5fd49-9ecd-49d7-8199-1706648255ca
keywords:
- Windows-Steuerelemente für EN_ALIGNRTL Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_ALIGNRTL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac2adaa629d00ef940f02f1ed69eb778cdc7813
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476095"
---
# <a name="en_alignrtl-notification-code"></a><span data-ttu-id="21774-105">EN \_ alignrtl-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="21774-105">EN\_ALIGNRTL notification code</span></span>

<span data-ttu-id="21774-106">Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass die Absatz Richtung von rechts nach links geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="21774-106">Notifies a rich edit control's parent window that the paragraph direction changed to right-to-left.</span></span> <span data-ttu-id="21774-107">Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="21774-107">A rich edit control sends this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ALIGNRTL

    WPARAM wParam
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="21774-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="21774-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21774-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="21774-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21774-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Rich Edit-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="21774-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the rich edit control.</span></span> <span data-ttu-id="21774-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="21774-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="21774-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="21774-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21774-113">Handle für das Rich Edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="21774-113">Handle to the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21774-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21774-114">Return value</span></span>

<span data-ttu-id="21774-115">Dieser Benachrichtigungs Code gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="21774-115">This notification code does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="21774-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21774-116">Requirements</span></span>



| <span data-ttu-id="21774-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21774-117">Requirement</span></span> | <span data-ttu-id="21774-118">Wert</span><span class="sxs-lookup"><span data-stu-id="21774-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21774-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21774-119">Minimum supported client</span></span><br/> | <span data-ttu-id="21774-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21774-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="21774-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21774-121">Minimum supported server</span></span><br/> | <span data-ttu-id="21774-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21774-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="21774-123">Header</span><span class="sxs-lookup"><span data-stu-id="21774-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="21774-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="21774-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21774-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21774-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="21774-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="21774-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="21774-127">**EN \_ alignltr**</span><span class="sxs-lookup"><span data-stu-id="21774-127">**EN\_ALIGNLTR**</span></span>](en-alignltr.md)
</dt> <dt>

<span data-ttu-id="21774-128">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="21774-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="21774-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="21774-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="21774-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="21774-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="21774-131">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="21774-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

