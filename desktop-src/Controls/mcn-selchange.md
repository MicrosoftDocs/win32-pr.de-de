---
title: MCN_SELCHANGE Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Monatskalender-Steuerelement gesendet, wenn das aktuell ausgewählte Datum oder der Datumsbereich geändert wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 8923524f-d257-409d-bd3e-021684b88856
keywords:
- Windows-Steuerelemente für MCN_SELCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- MCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffa328ca0173afd3a577f6cf14e0204cd5c0f7d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040240"
---
# <a name="mcn_selchange-notification-code"></a><span data-ttu-id="383be-105">MCN \_ selChange-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="383be-105">MCN\_SELCHANGE notification code</span></span>

<span data-ttu-id="383be-106">Wird von einem Monatskalender-Steuerelement gesendet, wenn das aktuell ausgewählte Datum oder der Datumsbereich geändert wird.</span><span class="sxs-lookup"><span data-stu-id="383be-106">Sent by a month calendar control when the currently selected date or range of dates changes.</span></span> <span data-ttu-id="383be-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="383be-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_SELCHANGE

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="383be-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="383be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="383be-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="383be-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="383be-110">Ein Zeiger auf eine [**nmselchange**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) -Struktur, die Informationen über den aktuell ausgewählten Datumsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="383be-110">Pointer to an [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) structure that contains information about the currently selected date range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="383be-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="383be-111">Return value</span></span>

<span data-ttu-id="383be-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="383be-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="383be-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="383be-113">Remarks</span></span>

<span data-ttu-id="383be-114">Beispielsweise sendet das Steuerelement MCN \_ selChange, wenn der Benutzer die Auswahl innerhalb des aktuellen Monats explizit ändert oder wenn die Auswahl in Reaktion auf die nächste/vorherige Monats Navigation implizit geändert wird.</span><span class="sxs-lookup"><span data-stu-id="383be-114">For example, the control sends MCN\_SELCHANGE when the user explicitly changes the selection within the current month or when the selection is implicitly changed in response to next/previous month navigation.</span></span> <span data-ttu-id="383be-115">Dieser Benachrichtigungs Code wird auch in regelmäßigen Abständen vom System gesendet, sodass das Steuerelement auf Datumsänderungen reagieren kann.</span><span class="sxs-lookup"><span data-stu-id="383be-115">This notification code is also sent by the system at regular intervals so that the control can respond to date changes.</span></span>

<span data-ttu-id="383be-116">Dieser Benachrichtigungs Code ähnelt [MCN \_ Select](mcn-select.md), aber er wird als Reaktion auf eine beliebige Auswahl Änderung gesendet.</span><span class="sxs-lookup"><span data-stu-id="383be-116">This notification code is similar to [MCN\_SELECT](mcn-select.md), but it is sent in response to any selection change.</span></span> <span data-ttu-id="383be-117">\_Die Auswahl von MCN wird nur für eine explizite Datumsauswahl gesendet.</span><span class="sxs-lookup"><span data-stu-id="383be-117">MCN\_SELECT is sent only for an explicit date selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="383be-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="383be-118">Requirements</span></span>



| <span data-ttu-id="383be-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="383be-119">Requirement</span></span> | <span data-ttu-id="383be-120">Wert</span><span class="sxs-lookup"><span data-stu-id="383be-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="383be-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="383be-121">Minimum supported client</span></span><br/> | <span data-ttu-id="383be-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="383be-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="383be-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="383be-123">Minimum supported server</span></span><br/> | <span data-ttu-id="383be-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="383be-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="383be-125">Header</span><span class="sxs-lookup"><span data-stu-id="383be-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="383be-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="383be-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





