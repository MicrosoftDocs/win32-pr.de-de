---
title: PGM_SETSCROLLINFO Meldung (kommstrg. h)
description: Legt die scrollparameter des Pager-Steuer Elements fest, einschließlich des Timeout Werts, der Zeilen pro Timeout und der Pixel pro Zeile. Sie können diese Nachricht explizit oder mithilfe des Pager- \_ Makros setScrollInfo senden.
ms.assetid: e02450b8-f2b5-45b2-9395-d7412119849c
keywords:
- Windows-Steuerelemente für PGM_SETSCROLLINFO Meldung
topic_type:
- apiref
api_name:
- PGM_SETSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8fc230e1a12968d0eb29f8ba512848df42b64b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858821"
---
# <a name="pgm_setscrollinfo-message"></a><span data-ttu-id="52120-105">PGM- \_ setScrollInfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="52120-105">PGM\_SETSCROLLINFO message</span></span>

<span data-ttu-id="52120-106">\[Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="52120-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="52120-107">Diese Meldung wird möglicherweise in zukünftigen Versionen von Windows nicht mehr unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="52120-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="52120-108">Legt die scrollparameter des Pager-Steuer Elements fest, einschließlich des Timeout Werts, der Zeilen pro Timeout und der Pixel pro Zeile.</span><span class="sxs-lookup"><span data-stu-id="52120-108">Sets the scrolling parameters of the pager control, including the timeout value, the lines per timeout, and the pixels per line.</span></span> <span data-ttu-id="52120-109">Sie können diese Nachricht explizit oder mithilfe des [**Pager-Makros \_ setScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) senden.</span><span class="sxs-lookup"><span data-stu-id="52120-109">You can send this message explicitly or by using the [**Pager\_SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="52120-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="52120-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52120-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52120-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52120-112">Ein **uint** , das den Timeout Wert für den Bild Lauf in Millisekunden angibt.</span><span class="sxs-lookup"><span data-stu-id="52120-112">A **UINT** that specifies the timeout value for the scroll, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="52120-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52120-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52120-114">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **uint** , das die Anzahl der Zeilen angibt, die pro Timeout durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="52120-114">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **UINT** that specifies the number of lines to scroll per timeout.</span></span> <span data-ttu-id="52120-115">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist ein **uint** , das die Anzahl der Pixel pro Zeile angibt.</span><span class="sxs-lookup"><span data-stu-id="52120-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **UINT** that specifies the number of pixels per line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52120-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52120-116">Return value</span></span>

<span data-ttu-id="52120-117">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="52120-117">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="52120-118">Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="52120-118">Security Considerations</span></span>

<span data-ttu-id="52120-119">Die Verwendung dieser Nachricht kann die Sicherheit des Programms beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="52120-119">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="52120-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52120-120">Remarks</span></span>

<span data-ttu-id="52120-121">Der *wParam* -Timeout Wert steuert die Rate, mit der das Pager-Steuerelement scrollereignisse generiert, wenn das Steuerelement die Mauseingabe erfasst hat und die linke Maustaste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="52120-121">The *wParam* timeout value controls the rate at which the pager control generates scrolling events when the control has captured the mouse input and the left mouse button is pressed.</span></span> <span data-ttu-id="52120-122">Kleinere Werte führen zu einem schnelleren Bildlauf. größere Werte führen zu einem langsameren Bildlauf.</span><span class="sxs-lookup"><span data-stu-id="52120-122">Smaller values result in faster scrolling; larger values result in slower scrolling.</span></span> <span data-ttu-id="52120-123">Der Standardwert ist ein Achtel der Doppelklick Zeit.</span><span class="sxs-lookup"><span data-stu-id="52120-123">The default value is one-eighth of the double-click time.</span></span> <span data-ttu-id="52120-124">Weitere Informationen finden Sie unter [**getdoubleclicktime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime).</span><span class="sxs-lookup"><span data-stu-id="52120-124">For more information, see [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime).</span></span>

<span data-ttu-id="52120-125">Standardmäßig scrollt das Pager-Steuerelement bei jedem scrollereignis einen Betrag, der der gesamten Breite oder Höhe des Steuer Elements entspricht, je nachdem, ob das Pager-Steuerelement eine horizontale oder vertikale Ausrichtung aufweist.</span><span class="sxs-lookup"><span data-stu-id="52120-125">By default, with each scrolling event the pager control scrolls an amount equal to the entire width or height of the control, depending on whether the pager control has a horizontal or vertical orientation.</span></span> <span data-ttu-id="52120-126">Die Werte in *LPARAM* werden zum Überschreiben der standardmäßigen scrollmenge verwendet.</span><span class="sxs-lookup"><span data-stu-id="52120-126">The values in *lParam* are used to override the default scrolling amount.</span></span> <span data-ttu-id="52120-127">Wenn Werte ungleich NULL angegeben werden, ist der scrollbetrag das Produkt der beiden Werte (LoWord (*LPARAM*) \* HIWORD (*LPARAM*)).</span><span class="sxs-lookup"><span data-stu-id="52120-127">If nonzero values are provided, the scrolling amount is the product of the two values (LOWORD(*lParam*) \* HIWORD(*lParam*)).</span></span>

## <a name="requirements"></a><span data-ttu-id="52120-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52120-128">Requirements</span></span>



| <span data-ttu-id="52120-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52120-129">Requirement</span></span> | <span data-ttu-id="52120-130">Wert</span><span class="sxs-lookup"><span data-stu-id="52120-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52120-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52120-131">Minimum supported client</span></span><br/> | <span data-ttu-id="52120-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52120-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52120-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52120-133">Minimum supported server</span></span><br/> | <span data-ttu-id="52120-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52120-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52120-135">Header</span><span class="sxs-lookup"><span data-stu-id="52120-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="52120-136"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="52120-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52120-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52120-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52120-138">**Pager \_ setScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="52120-138">**Pager\_SetScrollInfo**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)
</dt> </dl>

 

