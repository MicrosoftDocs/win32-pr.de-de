---
title: LBN_DBLCLK Benachrichtigungs Code (Winuser. h)
description: Benachrichtigt die Anwendung, dass der Benutzer auf ein Element in einem Listenfeld Doppel geklickt hat. Das übergeordnete Fenster des Listen Felds empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: 487282cb-833a-4123-987e-6a417fbd09d4
keywords:
- Windows-Steuerelemente für LBN_DBLCLK Benachrichtigungs
topic_type:
- apiref
api_name:
- LBN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a60623aafb287f2006d9e27da49d0df34c05b05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743009"
---
# <a name="lbn_dblclk-notification-code"></a><span data-ttu-id="c4e9d-105">LBN- \_ dblclk-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="c4e9d-105">LBN\_DBLCLK notification code</span></span>

<span data-ttu-id="c4e9d-106">Benachrichtigt die Anwendung, dass der Benutzer auf ein Element in einem Listenfeld Doppel geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="c4e9d-106">Notifies the application that the user has double-clicked an item in a list box.</span></span> <span data-ttu-id="c4e9d-107">Das übergeordnete Fenster des Listen Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="c4e9d-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c4e9d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4e9d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4e9d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4e9d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4e9d-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Listen Felds.</span><span class="sxs-lookup"><span data-stu-id="c4e9d-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="c4e9d-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="c4e9d-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="c4e9d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4e9d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4e9d-113">Handle für das Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="c4e9d-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4e9d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4e9d-114">Remarks</span></span>

<span data-ttu-id="c4e9d-115">Dieser Benachrichtigungs Code wird nur von einem Listenfeld gesendet, das den L-[**b- \_ Benachrichtigungs**](button-styles.md) Stil enthält.</span><span class="sxs-lookup"><span data-stu-id="c4e9d-115">This notification code is sent only by a list box that has the L [**BS\_NOTIFY**](button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4e9d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4e9d-116">Requirements</span></span>



| <span data-ttu-id="c4e9d-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4e9d-117">Requirement</span></span> | <span data-ttu-id="c4e9d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c4e9d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4e9d-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4e9d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c4e9d-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4e9d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c4e9d-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4e9d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c4e9d-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4e9d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c4e9d-123">Header</span><span class="sxs-lookup"><span data-stu-id="c4e9d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4e9d-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c4e9d-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4e9d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4e9d-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="c4e9d-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c4e9d-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c4e9d-127">LBN \_ selChange</span><span class="sxs-lookup"><span data-stu-id="c4e9d-127">LBN\_SELCHANGE</span></span>](lbn-selchange.md)
</dt> <dt>

<span data-ttu-id="c4e9d-128">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="c4e9d-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="c4e9d-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c4e9d-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="c4e9d-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c4e9d-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c4e9d-131">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="c4e9d-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

