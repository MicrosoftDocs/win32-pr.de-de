---
title: MCM_SETMONTHDELTA Meldung (kommstrg. h)
description: Legt die Bild Lauf Rate für ein Monatskalender-Steuerelement fest. Die Scrollrate entspricht der Anzahl von Monaten, die das Steuerelement seine Anzeige verschiebt, wenn der Benutzer auf eine Bild Lauf Schaltfläche klickt. Sie können diese Nachricht explizit oder mit dem monthcal- \_ setmonthdelta-Makro senden.
ms.assetid: 2d01b95f-3be8-4548-80b5-ac01d3e49e9f
keywords:
- Windows-Steuerelemente für MCM_SETMONTHDELTA Meldung
topic_type:
- apiref
api_name:
- MCM_SETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 123eddb55a7ee8ddf8e3f6d8136e9ee57dfc8681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340006"
---
# <a name="mcm_setmonthdelta-message"></a><span data-ttu-id="91646-106">MCM- \_ setmonthdelta-Meldung</span><span class="sxs-lookup"><span data-stu-id="91646-106">MCM\_SETMONTHDELTA message</span></span>

<span data-ttu-id="91646-107">Legt die Bild Lauf Rate für ein Monatskalender-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="91646-107">Sets the scroll rate for a month calendar control.</span></span> <span data-ttu-id="91646-108">Die Scrollrate entspricht der Anzahl von Monaten, die das Steuerelement seine Anzeige verschiebt, wenn der Benutzer auf eine Bild Lauf Schaltfläche klickt.</span><span class="sxs-lookup"><span data-stu-id="91646-108">The scroll rate is the number of months that the control moves its display when the user clicks a scroll button.</span></span> <span data-ttu-id="91646-109">Sie können diese Nachricht explizit oder mit dem [**monthcal- \_ setmonthdelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="91646-109">You can send this message explicitly or by using the [**MonthCal\_SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="91646-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="91646-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91646-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91646-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91646-112">Ein Wert, der die Anzahl der Monate darstellt, die als Schiebe Rate des Steuer Elements festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="91646-112">Value representing the number of months to be set as the control's scroll rate.</span></span> <span data-ttu-id="91646-113">Wenn dieser Wert 0 (null) ist, wird der Monat Delta auf den Standardwert zurückgesetzt. Dies ist die Anzahl der Monate, die im Steuerelement angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="91646-113">If this value is zero, the month delta is reset to the default, which is the number of months displayed in the control.</span></span>

</dd> <dt>

<span data-ttu-id="91646-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91646-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="91646-115">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="91646-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91646-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91646-116">Return value</span></span>

<span data-ttu-id="91646-117">Gibt einen int-Wert zurück, der die vorherige Scrollrate darstellt.</span><span class="sxs-lookup"><span data-stu-id="91646-117">Returns an INT value that represents the previous scroll rate.</span></span> <span data-ttu-id="91646-118">Wenn die Scrollrate zuvor nicht festgelegt wurde, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="91646-118">If the scroll rate was not previously set, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="91646-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91646-119">Remarks</span></span>

<span data-ttu-id="91646-120">Die Bild-auf-und Bild-ab-Taste, VK \_ vor und VK, \_ Ändern Sie den ausgewählten Monat um 1, unabhängig von der Anzahl der angezeigten Monate oder des durch **MCM \_ setmonthdelta** festgelegten Werts.</span><span class="sxs-lookup"><span data-stu-id="91646-120">The PAGE UP and PAGE DOWN keys, VK\_PRIOR and VK\_NEXT, change the selected month by one, regardless of the number of months displayed or the value set by **MCM\_SETMONTHDELTA**.</span></span>

## <a name="requirements"></a><span data-ttu-id="91646-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91646-121">Requirements</span></span>



| <span data-ttu-id="91646-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91646-122">Requirement</span></span> | <span data-ttu-id="91646-123">Wert</span><span class="sxs-lookup"><span data-stu-id="91646-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91646-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91646-124">Minimum supported client</span></span><br/> | <span data-ttu-id="91646-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91646-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91646-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91646-126">Minimum supported server</span></span><br/> | <span data-ttu-id="91646-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91646-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91646-128">Header</span><span class="sxs-lookup"><span data-stu-id="91646-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="91646-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="91646-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





