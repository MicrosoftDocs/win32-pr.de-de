---
title: MCM_GETCALENDARCOUNT Meldung (kommstrg. h)
description: Ruft die Anzahl der Kalender ab, die momentan im Kalender Steuerelement angezeigt werden. Sie können diese Nachricht explizit oder mit dem monthcal \_ getcalendarcount-Makro senden.
ms.assetid: b9463f02-d37b-49b0-8387-0938020c23ee
keywords:
- Windows-Steuerelemente für MCM_GETCALENDARCOUNT Meldung
topic_type:
- apiref
api_name:
- MCM_GETCALENDARCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a3be9e9bcc5db8c1aab32cacbcc2ded82727af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104805"
---
# <a name="mcm_getcalendarcount-message"></a><span data-ttu-id="1f28f-105">MCM \_ getcalendarcount-Meldung</span><span class="sxs-lookup"><span data-stu-id="1f28f-105">MCM\_GETCALENDARCOUNT message</span></span>

<span data-ttu-id="1f28f-106">Ruft die Anzahl der Kalender ab, die momentan im Kalender Steuerelement angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1f28f-106">Gets the number of calendars currently displayed in the calendar control.</span></span> <span data-ttu-id="1f28f-107">Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getcalendarcount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="1f28f-107">You can send this message explicitly or by using the [**MonthCal\_GetCalendarCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f28f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f28f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f28f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1f28f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f28f-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="1f28f-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1f28f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f28f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f28f-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="1f28f-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f28f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f28f-113">Return value</span></span>

<span data-ttu-id="1f28f-114">Anzahl der derzeit im Kalender Steuerelement angezeigten Kalender.</span><span class="sxs-lookup"><span data-stu-id="1f28f-114">Number of calendars currently displayed in the calendar control.</span></span> <span data-ttu-id="1f28f-115">Die maximal zulässige Anzahl zulässiger Kalender ist 12.</span><span class="sxs-lookup"><span data-stu-id="1f28f-115">The maximum number of allowed calendars is 12.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f28f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f28f-116">Requirements</span></span>



| <span data-ttu-id="1f28f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f28f-117">Requirement</span></span> | <span data-ttu-id="1f28f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1f28f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f28f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f28f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1f28f-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f28f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1f28f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f28f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1f28f-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f28f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f28f-123">Header</span><span class="sxs-lookup"><span data-stu-id="1f28f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f28f-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f28f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





