---
title: CBN_ERRSPACE Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn ein Kombinations Feld nicht genügend Arbeitsspeicher zuordnen kann, um eine bestimmte Anforderung zu erfüllen. Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: c1c19c40-fc88-47d0-9676-7a267a48ae98
keywords:
- Windows-Steuerelemente für CBN_ERRSPACE Benachrichtigungs
topic_type:
- apiref
api_name:
- CBN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74e46e4435a03a0233ce6591d3c36cefb4d880a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106281"
---
# <a name="cbn_errspace-notification-code"></a><span data-ttu-id="5e930-105">CBN- \_ errspace-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="5e930-105">CBN\_ERRSPACE notification code</span></span>

<span data-ttu-id="5e930-106">Wird gesendet, wenn ein Kombinations Feld nicht genügend Arbeitsspeicher zuordnen kann, um eine bestimmte Anforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="5e930-106">Sent when a combo box cannot allocate enough memory to meet a specific request.</span></span> <span data-ttu-id="5e930-107">Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="5e930-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5e930-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e930-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e930-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e930-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e930-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner des Kombinations Felds.</span><span class="sxs-lookup"><span data-stu-id="5e930-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="5e930-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="5e930-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="5e930-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e930-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e930-113">Handle für das Kombinations Feld.</span><span class="sxs-lookup"><span data-stu-id="5e930-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5e930-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e930-114">Requirements</span></span>



| <span data-ttu-id="5e930-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e930-115">Requirement</span></span> | <span data-ttu-id="5e930-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5e930-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e930-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e930-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5e930-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e930-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5e930-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e930-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5e930-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e930-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5e930-121">Header</span><span class="sxs-lookup"><span data-stu-id="5e930-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e930-122"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="5e930-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e930-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e930-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="5e930-124">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="5e930-124">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="5e930-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5e930-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="5e930-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5e930-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5e930-127">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="5e930-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

