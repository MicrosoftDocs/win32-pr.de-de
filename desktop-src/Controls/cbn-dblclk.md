---
title: CBN_DBLCLK Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer auf eine Zeichenfolge im Listenfeld eines Kombinations Felds doppelklickt. Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: 79ca3fd3-4a71-4bd5-be68-efc867a4ad22
keywords:
- Windows-Steuerelemente für CBN_DBLCLK Benachrichtigungs
topic_type:
- apiref
api_name:
- CBN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 841c68079572e1740f074034c1a8097ba6a86253
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346543"
---
# <a name="cbn_dblclk-notification-code"></a><span data-ttu-id="d65f5-105">CBN- \_ dblclk-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="d65f5-105">CBN\_DBLCLK notification code</span></span>

<span data-ttu-id="d65f5-106">Wird gesendet, wenn der Benutzer auf eine Zeichenfolge im Listenfeld eines Kombinations Felds doppelklickt.</span><span class="sxs-lookup"><span data-stu-id="d65f5-106">Sent when the user double-clicks a string in the list box of a combo box.</span></span> <span data-ttu-id="d65f5-107">Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="d65f5-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d65f5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d65f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d65f5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d65f5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d65f5-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner des Kombinations Felds.</span><span class="sxs-lookup"><span data-stu-id="d65f5-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="d65f5-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="d65f5-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d65f5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d65f5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d65f5-113">Handle für das Kombinations Feld.</span><span class="sxs-lookup"><span data-stu-id="d65f5-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d65f5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d65f5-114">Remarks</span></span>

<span data-ttu-id="d65f5-115">Dieser Benachrichtigungs Code tritt nur für ein Kombinations Feld mit [**\_ einfachem CBS**](combo-box-styles.md) -Stil auf.</span><span class="sxs-lookup"><span data-stu-id="d65f5-115">This notification code occurs only for a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="d65f5-116">In einem Kombinations Feld mit dem Format " [**CBS \_ Dropdown**](combo-box-styles.md) " oder " [**CBS \_ DropDownList**](combo-box-styles.md) " kann kein Doppelklick auftreten, weil ein einzelner Klick das Listenfeld schließt.</span><span class="sxs-lookup"><span data-stu-id="d65f5-116">In a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, a double-click cannot occur because a single click closes the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="d65f5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d65f5-117">Requirements</span></span>



| <span data-ttu-id="d65f5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d65f5-118">Requirement</span></span> | <span data-ttu-id="d65f5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d65f5-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d65f5-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d65f5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d65f5-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d65f5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d65f5-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d65f5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d65f5-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d65f5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d65f5-124">Header</span><span class="sxs-lookup"><span data-stu-id="d65f5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d65f5-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="d65f5-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d65f5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d65f5-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="d65f5-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d65f5-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d65f5-128">CBN \_ selChange</span><span class="sxs-lookup"><span data-stu-id="d65f5-128">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

<span data-ttu-id="d65f5-129">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="d65f5-129">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d65f5-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d65f5-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d65f5-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d65f5-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d65f5-132">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="d65f5-132">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

