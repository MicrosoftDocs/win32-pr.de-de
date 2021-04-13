---
title: CBN_SETFOCUS Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn ein Kombinations Feld den Tastaturfokus erhält. Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: 8072edc6-aedc-4daf-80df-d3acd82fcffa
keywords:
- Windows-Steuerelemente für CBN_SETFOCUS Benachrichtigungs
topic_type:
- apiref
api_name:
- CBN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885bbaebac0a79fc600cbcc2b7864cbdfd19ea93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341378"
---
# <a name="cbn_setfocus-notification-code"></a><span data-ttu-id="d5821-105">CBN- \_ SetFocus-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="d5821-105">CBN\_SETFOCUS notification code</span></span>

<span data-ttu-id="d5821-106">Wird gesendet, wenn ein Kombinations Feld den Tastaturfokus erhält.</span><span class="sxs-lookup"><span data-stu-id="d5821-106">Sent when a combo box receives the keyboard focus.</span></span> <span data-ttu-id="d5821-107">Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="d5821-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d5821-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5821-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5821-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5821-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5821-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner des Kombinations Felds.</span><span class="sxs-lookup"><span data-stu-id="d5821-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="d5821-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="d5821-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d5821-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5821-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5821-113">Handle für das Kombinations Feld.</span><span class="sxs-lookup"><span data-stu-id="d5821-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5821-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5821-114">Requirements</span></span>



| <span data-ttu-id="d5821-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5821-115">Requirement</span></span> | <span data-ttu-id="d5821-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d5821-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5821-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5821-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d5821-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5821-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d5821-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5821-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d5821-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5821-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d5821-121">Header</span><span class="sxs-lookup"><span data-stu-id="d5821-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5821-122"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="d5821-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5821-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5821-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="d5821-124">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d5821-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d5821-125">CBN- \_ killfokus</span><span class="sxs-lookup"><span data-stu-id="d5821-125">CBN\_KILLFOCUS</span></span>](cbn-killfocus.md)
</dt> <dt>

<span data-ttu-id="d5821-126">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="d5821-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d5821-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d5821-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d5821-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d5821-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d5821-129">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="d5821-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

