---
title: LBN_KILLFOCUS Benachrichtigungs Code (Winuser. h)
description: Benachrichtigt die Anwendung, dass das Listenfeld den Tastaturfokus verloren hat. Das übergeordnete Fenster des Listen Felds empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: ef927b56-3c46-4ae7-87df-13295cf175a8
keywords:
- Windows-Steuerelemente für LBN_KILLFOCUS Benachrichtigungs
topic_type:
- apiref
api_name:
- LBN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba424efc2518d359c3d031561aeafee8c0348b65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105518"
---
# <a name="lbn_killfocus-notification-code"></a><span data-ttu-id="059f2-105">LBN- \_ killfocus-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="059f2-105">LBN\_KILLFOCUS notification code</span></span>

<span data-ttu-id="059f2-106">Benachrichtigt die Anwendung, dass das Listenfeld den Tastaturfokus verloren hat.</span><span class="sxs-lookup"><span data-stu-id="059f2-106">Notifies the application that the list box has lost the keyboard focus.</span></span> <span data-ttu-id="059f2-107">Das übergeordnete Fenster des Listen Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="059f2-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="059f2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="059f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="059f2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="059f2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="059f2-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Listen Felds.</span><span class="sxs-lookup"><span data-stu-id="059f2-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="059f2-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="059f2-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="059f2-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="059f2-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="059f2-113">Handle für das Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="059f2-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="059f2-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="059f2-114">Requirements</span></span>



| <span data-ttu-id="059f2-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="059f2-115">Requirement</span></span> | <span data-ttu-id="059f2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="059f2-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="059f2-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="059f2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="059f2-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="059f2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="059f2-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="059f2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="059f2-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="059f2-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="059f2-121">Header</span><span class="sxs-lookup"><span data-stu-id="059f2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="059f2-122"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="059f2-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="059f2-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="059f2-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="059f2-124">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="059f2-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="059f2-125">LBN- \_ SetFocus</span><span class="sxs-lookup"><span data-stu-id="059f2-125">LBN\_SETFOCUS</span></span>](lbn-setfocus.md)
</dt> <dt>

<span data-ttu-id="059f2-126">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="059f2-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="059f2-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="059f2-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="059f2-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="059f2-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="059f2-129">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="059f2-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

