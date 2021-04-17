---
title: MCM_GETMINREQRECT Meldung (kommstrg. h)
description: Ruft die Mindestgröße ab, die erforderlich ist, um einen vollen Monat in einem Monatskalender-Steuerelement anzuzeigen. Sie können diese Nachricht explizit oder mit dem monthcal \_ getminreqrect-Makro senden.
ms.assetid: f0378338-4809-48e9-9387-ed8b79356f95
keywords:
- Windows-Steuerelemente für MCM_GETMINREQRECT Meldung
topic_type:
- apiref
api_name:
- MCM_GETMINREQRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac6b2e2b16a70841836a277ffe55e030a6d6a241
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476071"
---
# <a name="mcm_getminreqrect-message"></a><span data-ttu-id="300cc-105">MCM \_ getminreqrect-Meldung</span><span class="sxs-lookup"><span data-stu-id="300cc-105">MCM\_GETMINREQRECT message</span></span>

<span data-ttu-id="300cc-106">Ruft die Mindestgröße ab, die erforderlich ist, um einen vollen Monat in einem Monatskalender-Steuerelement anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="300cc-106">Retrieves the minimum size required to display a full month in a month calendar control.</span></span> <span data-ttu-id="300cc-107">Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getminreqrect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="300cc-107">You can send this message explicitly or by using the [**MonthCal\_GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="300cc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="300cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="300cc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="300cc-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="300cc-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="300cc-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="300cc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="300cc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="300cc-112">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die Informationen zu umschließenden Rechtecks empfängt.</span><span class="sxs-lookup"><span data-stu-id="300cc-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive bounding rectangle information.</span></span> <span data-ttu-id="300cc-113">Dieser Parameter muss eine gültige Adresse sein und darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="300cc-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="300cc-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="300cc-114">Return value</span></span>

<span data-ttu-id="300cc-115">Gibt einen Wert ungleich 0 (null) zurück, und *LPARAM* empfängt bei erfolgreicher Ausführung die entsprechenden umgebenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="300cc-115">Returns nonzero and *lParam* receives the applicable bounding information if successful.</span></span> <span data-ttu-id="300cc-116">Andernfalls gibt die Meldung 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="300cc-116">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="300cc-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="300cc-117">Remarks</span></span>

<span data-ttu-id="300cc-118">Die mindestens erforderliche Fenstergröße für ein Monatskalender-Steuerelement hängt von der aktuell ausgewählten Schriftart, den Steuerelement Stilen, den Systemmetriken und den regionalen Einstellungen ab.</span><span class="sxs-lookup"><span data-stu-id="300cc-118">The minimum required window size for a month calendar control depends on the currently selected font, control styles, system metrics, and regional settings.</span></span> <span data-ttu-id="300cc-119">Wenn eine Anwendung etwas ändert, das sich auf die minimale Fenstergröße auswirkt, oder eine [**WM- \_ settingchange**](/windows/desktop/winmsg/wm-settingchange) -Nachricht verarbeitet, sollte Sie **MCM \_ getminreqrect** senden, um die neue Mindestgröße zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="300cc-119">When an application changes anything that affects the minimum window size, or processes a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message, it should send **MCM\_GETMINREQRECT** to determine the new minimum size.</span></span>

> [!Note]  
> <span data-ttu-id="300cc-120">Das von **MCM \_ getminreqrect** zurückgegebene Rechteck enthält nicht die Breite der "Today"-Zeichenfolge, wenn es vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="300cc-120">The rectangle returned by **MCM\_GETMINREQRECT** does not include the width of the "Today" string, if it is present.</span></span> <span data-ttu-id="300cc-121">Wenn der [**MCS- \_ notoday**](month-calendar-control-styles.md) -Stil nicht festgelegt ist, sollte Ihre Anwendung auch das Rechteck abrufen, das die Zeichen folgen Breite "Today" definiert, indem eine [**MCM \_ getmaxchanwidth**](mcm-getmaxtodaywidth.md) -Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="300cc-121">If the [**MCS\_NOTODAY**](month-calendar-control-styles.md) style is not set, your application should also retrieve the rectangle that defines the "Today" string width by sending a [**MCM\_GETMAXTODAYWIDTH**](mcm-getmaxtodaywidth.md) message.</span></span> <span data-ttu-id="300cc-122">Verwenden Sie die größere der beiden Rechtecke, um sicherzustellen, dass die "Today"-Zeichenfolge nicht abgeschnitten wird.</span><span class="sxs-lookup"><span data-stu-id="300cc-122">Use the larger of the two rectangles to ensure that the "Today" string is not clipped.</span></span>

 

<span data-ttu-id="300cc-123">Die **oberen** und **linken** Member der Struktur, auf die von *LPARAM* verwiesen wird, sind immer 0 (null).</span><span class="sxs-lookup"><span data-stu-id="300cc-123">The **top** and **left** members of the structure pointed to by *lParam* will always be zero.</span></span> <span data-ttu-id="300cc-124">Die **Rechte** und **untersten** Elemente stellen den minimalen *CX* -und *CY* -Member dar, der für das Steuerelement erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="300cc-124">The **right** and **bottom** members represent the minimum *cx* and *cy* required for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="300cc-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="300cc-125">Requirements</span></span>



| <span data-ttu-id="300cc-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="300cc-126">Requirement</span></span> | <span data-ttu-id="300cc-127">Wert</span><span class="sxs-lookup"><span data-stu-id="300cc-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="300cc-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="300cc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="300cc-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="300cc-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="300cc-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="300cc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="300cc-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="300cc-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="300cc-132">Header</span><span class="sxs-lookup"><span data-stu-id="300cc-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="300cc-133"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="300cc-133"><dt>Commctrl.h</dt></span></span> </dl> |



 

