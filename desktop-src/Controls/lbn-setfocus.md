---
title: LBN_SETFOCUS Benachrichtigungs Code (Winuser. h)
description: Benachrichtigt die Anwendung, dass das Listenfeld den Tastaturfokus erhalten hat. Das übergeordnete Fenster des Listen Felds empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: d9e5e035-98a5-4ece-ba40-6d341c101859
keywords:
- Windows-Steuerelemente für LBN_SETFOCUS Benachrichtigungs
topic_type:
- apiref
api_name:
- LBN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88e56043982cec6606f7c78d3469ab2583951f88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858913"
---
# <a name="lbn_setfocus-notification-code"></a><span data-ttu-id="a30aa-105">LBN- \_ SetFocus-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="a30aa-105">LBN\_SETFOCUS notification code</span></span>

<span data-ttu-id="a30aa-106">Benachrichtigt die Anwendung, dass das Listenfeld den Tastaturfokus erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="a30aa-106">Notifies the application that the list box has received the keyboard focus.</span></span> <span data-ttu-id="a30aa-107">Das übergeordnete Fenster des Listen Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="a30aa-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a30aa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a30aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a30aa-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a30aa-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a30aa-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Listen Felds.</span><span class="sxs-lookup"><span data-stu-id="a30aa-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="a30aa-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="a30aa-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="a30aa-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a30aa-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a30aa-113">Handle für das Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="a30aa-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a30aa-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a30aa-114">Requirements</span></span>



| <span data-ttu-id="a30aa-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a30aa-115">Requirement</span></span> | <span data-ttu-id="a30aa-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a30aa-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a30aa-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a30aa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a30aa-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a30aa-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a30aa-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a30aa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a30aa-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a30aa-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a30aa-121">Header</span><span class="sxs-lookup"><span data-stu-id="a30aa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a30aa-122"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="a30aa-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a30aa-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a30aa-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="a30aa-124">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="a30aa-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a30aa-125">LBN- \_ killfokus</span><span class="sxs-lookup"><span data-stu-id="a30aa-125">LBN\_KILLFOCUS</span></span>](lbn-killfocus.md)
</dt> <dt>

<span data-ttu-id="a30aa-126">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="a30aa-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="a30aa-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a30aa-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="a30aa-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a30aa-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a30aa-129">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="a30aa-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

