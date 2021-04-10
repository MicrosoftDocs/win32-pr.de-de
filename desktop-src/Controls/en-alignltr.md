---
title: EN_ALIGNLTR Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass die Absatz Richtung von links nach rechts geändert wurde. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM- \_ Befehls Meldung.
ms.assetid: 754ac2b5-bcec-487b-a1ab-b653f673830a
keywords:
- Windows-Steuerelemente für EN_ALIGNLTR Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_ALIGNLTR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55c20a9ae4efb3ba5758ed0740b20b8b57f3877
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040446"
---
# <a name="en_alignltr-notification-code"></a><span data-ttu-id="78956-105">EN \_ alignltr-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="78956-105">EN\_ALIGNLTR notification code</span></span>

<span data-ttu-id="78956-106">Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass die Absatz Richtung von links nach rechts geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="78956-106">Notifies a rich edit control's parent window that the paragraph direction has changed to left-to-right.</span></span> <span data-ttu-id="78956-107">Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="78956-107">A rich edit control sends this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ALIGNLTR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="78956-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="78956-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78956-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78956-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78956-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Rich Edit-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="78956-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the rich edit control.</span></span> <span data-ttu-id="78956-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="78956-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="78956-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78956-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78956-113">Handle für das Rich Edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="78956-113">Handle to the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78956-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78956-114">Return value</span></span>

<span data-ttu-id="78956-115">Dieser Benachrichtigungs Code gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="78956-115">This notification code does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="78956-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78956-116">Requirements</span></span>



| <span data-ttu-id="78956-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78956-117">Requirement</span></span> | <span data-ttu-id="78956-118">Wert</span><span class="sxs-lookup"><span data-stu-id="78956-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78956-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78956-119">Minimum supported client</span></span><br/> | <span data-ttu-id="78956-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78956-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="78956-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78956-121">Minimum supported server</span></span><br/> | <span data-ttu-id="78956-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78956-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="78956-123">Header</span><span class="sxs-lookup"><span data-stu-id="78956-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="78956-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="78956-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78956-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78956-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="78956-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="78956-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="78956-127">**de \_ alignrtl**</span><span class="sxs-lookup"><span data-stu-id="78956-127">**EN\_ALIGNRTL**</span></span>](en-alignrtl.md)
</dt> <dt>

<span data-ttu-id="78956-128">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="78956-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="78956-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="78956-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="78956-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="78956-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="78956-131">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="78956-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

