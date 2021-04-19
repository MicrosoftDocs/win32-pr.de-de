---
title: CBN_KILLFOCUS Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn ein Kombinations Feld den Tastaturfokus verliert. Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: 0118a2ff-9811-4bf1-b3f6-1d00ca5c8dbe
keywords:
- Windows-Steuerelemente für CBN_KILLFOCUS Benachrichtigungs
topic_type:
- apiref
api_name:
- CBN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e266824bf8bcdac1fb901d40ca2b15406fc79660
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346535"
---
# <a name="cbn_killfocus-notification-code"></a><span data-ttu-id="ee075-105">CBN- \_ killfocus-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="ee075-105">CBN\_KILLFOCUS notification code</span></span>

<span data-ttu-id="ee075-106">Wird gesendet, wenn ein Kombinations Feld den Tastaturfokus verliert.</span><span class="sxs-lookup"><span data-stu-id="ee075-106">Sent when a combo box loses the keyboard focus.</span></span> <span data-ttu-id="ee075-107">Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="ee075-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ee075-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee075-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee075-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ee075-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee075-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner des Kombinations Felds.</span><span class="sxs-lookup"><span data-stu-id="ee075-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="ee075-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="ee075-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="ee075-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ee075-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee075-113">Handle für das Kombinations Feld.</span><span class="sxs-lookup"><span data-stu-id="ee075-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee075-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee075-114">Requirements</span></span>



| <span data-ttu-id="ee075-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee075-115">Requirement</span></span> | <span data-ttu-id="ee075-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ee075-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee075-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee075-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ee075-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee075-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ee075-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee075-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ee075-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee075-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ee075-121">Header</span><span class="sxs-lookup"><span data-stu-id="ee075-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee075-122"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="ee075-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee075-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee075-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="ee075-124">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="ee075-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ee075-125">CBN- \_ SetFocus</span><span class="sxs-lookup"><span data-stu-id="ee075-125">CBN\_SETFOCUS</span></span>](cbn-setfocus.md)
</dt> <dt>

<span data-ttu-id="ee075-126">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="ee075-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="ee075-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ee075-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="ee075-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ee075-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ee075-129">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="ee075-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

