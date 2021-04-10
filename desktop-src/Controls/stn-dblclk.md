---
title: STN_DBLCLK Benachrichtigungs Code (Winuser. h)
description: Der STN \_ dblclk-Benachrichtigungs Code wird gesendet, wenn der Benutzer auf ein statisches Steuerelement mit dem SS-Benachrichtigungs Stil doppelklickt \_ . Das übergeordnete Fenster des Steuer Elements empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: e3203309-87ea-46f4-9269-7e68c6fa0e4a
keywords:
- Windows-Steuerelemente für STN_DBLCLK Benachrichtigungs
topic_type:
- apiref
api_name:
- STN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 853ed5142de99dc85b729b4c4ea208273d4ace1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040309"
---
# <a name="stn_dblclk-notification-code"></a><span data-ttu-id="c38fc-105">STN \_ dblclk-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="c38fc-105">STN\_DBLCLK notification code</span></span>

<span data-ttu-id="c38fc-106">Der STN \_ dblclk-Benachrichtigungs Code wird gesendet, wenn der Benutzer auf ein statisches Steuerelement mit dem [**SS \_**](static-control-styles.md) -Benachrichtigungs Stil doppelklickt.</span><span class="sxs-lookup"><span data-stu-id="c38fc-106">The STN\_DBLCLK notification code is sent when the user double-clicks a static control that has the [**SS\_NOTIFY**](static-control-styles.md) style.</span></span> <span data-ttu-id="c38fc-107">Das übergeordnete Fenster des Steuer Elements empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="c38fc-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c38fc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c38fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c38fc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c38fc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c38fc-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des statischen Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="c38fc-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="c38fc-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="c38fc-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="c38fc-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c38fc-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c38fc-113">Handle für das statische Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c38fc-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c38fc-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c38fc-114">Requirements</span></span>



| <span data-ttu-id="c38fc-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c38fc-115">Requirement</span></span> | <span data-ttu-id="c38fc-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c38fc-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c38fc-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c38fc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c38fc-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c38fc-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c38fc-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c38fc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c38fc-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c38fc-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c38fc-121">Header</span><span class="sxs-lookup"><span data-stu-id="c38fc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c38fc-122"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c38fc-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c38fc-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c38fc-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="c38fc-124">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c38fc-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c38fc-125">\_angeklickte STN</span><span class="sxs-lookup"><span data-stu-id="c38fc-125">STN\_CLICKED</span></span>](stn-clicked.md)
</dt> <dt>

<span data-ttu-id="c38fc-126">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c38fc-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c38fc-127">Statische Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="c38fc-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="c38fc-128">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="c38fc-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="c38fc-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c38fc-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="c38fc-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c38fc-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c38fc-131">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="c38fc-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

