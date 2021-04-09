---
title: LBN_SELCANCEL Benachrichtigungs Code (Winuser. h)
description: Benachrichtigt die Anwendung, dass der Benutzer die Auswahl in einem Listenfeld abgebrochen hat. Das übergeordnete Fenster des Listen Felds empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: 82e39f22-090e-4dda-8ddc-6a1fe4704fc7
keywords:
- Windows-Steuerelemente für LBN_SELCANCEL Benachrichtigungs
topic_type:
- apiref
api_name:
- LBN_SELCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c192fbdfdb7a351d51993bee89b9b6ec3dab387
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956995"
---
# <a name="lbn_selcancel-notification-code"></a><span data-ttu-id="78cc1-105">LBN \_ selcancel-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="78cc1-105">LBN\_SELCANCEL notification code</span></span>

<span data-ttu-id="78cc1-106">Benachrichtigt die Anwendung, dass der Benutzer die Auswahl in einem Listenfeld abgebrochen hat.</span><span class="sxs-lookup"><span data-stu-id="78cc1-106">Notifies the application that the user has canceled the selection in a list box.</span></span> <span data-ttu-id="78cc1-107">Das übergeordnete Fenster des Listen Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="78cc1-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_SELCANCEL

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="78cc1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="78cc1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78cc1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78cc1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78cc1-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Listen Felds.</span><span class="sxs-lookup"><span data-stu-id="78cc1-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="78cc1-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="78cc1-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="78cc1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78cc1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78cc1-113">Handle für das Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="78cc1-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78cc1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78cc1-114">Remarks</span></span>

<span data-ttu-id="78cc1-115">Dieser Benachrichtigungs Code wird nur von einem Listenfeld gesendet, das den L-[**b- \_ Benachrichtigungs**](button-styles.md) Stil enthält.</span><span class="sxs-lookup"><span data-stu-id="78cc1-115">This notification code is sent only by a list box that has the L [**BS\_NOTIFY**](button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="78cc1-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78cc1-116">Requirements</span></span>



| <span data-ttu-id="78cc1-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78cc1-117">Requirement</span></span> | <span data-ttu-id="78cc1-118">Wert</span><span class="sxs-lookup"><span data-stu-id="78cc1-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78cc1-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78cc1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="78cc1-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78cc1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="78cc1-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78cc1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="78cc1-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78cc1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="78cc1-123">Header</span><span class="sxs-lookup"><span data-stu-id="78cc1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="78cc1-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="78cc1-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78cc1-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78cc1-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="78cc1-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="78cc1-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="78cc1-127">**LB- \_ setcurrsel**</span><span class="sxs-lookup"><span data-stu-id="78cc1-127">**LB\_SETCURSEL**</span></span>](lb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="78cc1-128">LBN- \_ dblclk</span><span class="sxs-lookup"><span data-stu-id="78cc1-128">LBN\_DBLCLK</span></span>](lbn-dblclk.md)
</dt> <dt>

[<span data-ttu-id="78cc1-129">LBN \_ selChange</span><span class="sxs-lookup"><span data-stu-id="78cc1-129">LBN\_SELCHANGE</span></span>](lbn-selchange.md)
</dt> <dt>

<span data-ttu-id="78cc1-130">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="78cc1-130">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="78cc1-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="78cc1-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="78cc1-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="78cc1-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="78cc1-133">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="78cc1-133">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

