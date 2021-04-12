---
title: LBN_ERRSPACE Benachrichtigungs Code (Winuser. h)
description: Benachrichtigt die Anwendung, dass das Listenfeld nicht genügend Arbeitsspeicher zuordnen kann, um eine bestimmte Anforderung zu erfüllen. Das übergeordnete Fenster des Listen Felds empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: ff716ad0-cbd8-4ac3-bcaf-d5be81355eaa
keywords:
- Windows-Steuerelemente für LBN_ERRSPACE Benachrichtigungs
topic_type:
- apiref
api_name:
- LBN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d324b17a83e38a9b3592be71720486910e88689d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213731"
---
# <a name="lbn_errspace-notification-code"></a><span data-ttu-id="656d1-105">LBN- \_ errspace-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="656d1-105">LBN\_ERRSPACE notification code</span></span>

<span data-ttu-id="656d1-106">Benachrichtigt die Anwendung, dass das Listenfeld nicht genügend Arbeitsspeicher zuordnen kann, um eine bestimmte Anforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="656d1-106">Notifies the application that the list box cannot allocate enough memory to meet a specific request.</span></span> <span data-ttu-id="656d1-107">Das übergeordnete Fenster des Listen Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="656d1-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="656d1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="656d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="656d1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="656d1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="656d1-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Listen Felds.</span><span class="sxs-lookup"><span data-stu-id="656d1-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="656d1-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="656d1-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="656d1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="656d1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="656d1-113">Handle für das Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="656d1-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="656d1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="656d1-114">Requirements</span></span>



| <span data-ttu-id="656d1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="656d1-115">Requirement</span></span> | <span data-ttu-id="656d1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="656d1-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="656d1-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="656d1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="656d1-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="656d1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="656d1-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="656d1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="656d1-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="656d1-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="656d1-121">Header</span><span class="sxs-lookup"><span data-stu-id="656d1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="656d1-122"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="656d1-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="656d1-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="656d1-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="656d1-124">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="656d1-124">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="656d1-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="656d1-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="656d1-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="656d1-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="656d1-127">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="656d1-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

