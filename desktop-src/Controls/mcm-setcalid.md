---
title: MCM_SETCALID Meldung (kommstrg. h)
description: Legt die Kalender-ID für das angegebene Kalender Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des "monthcal \_ setcalid"-Makros senden.
ms.assetid: 4b9d06f5-0784-4a17-b401-982206d4be67
keywords:
- Windows-Steuerelemente für MCM_SETCALID Meldung
topic_type:
- apiref
api_name:
- MCM_SETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a661a685062fe737a1927c3a6ab455e8499c6ca9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040241"
---
# <a name="mcm_setcalid-message"></a><span data-ttu-id="8ca91-105">MCM \_ -setcalid-Meldung</span><span class="sxs-lookup"><span data-stu-id="8ca91-105">MCM\_SETCALID message</span></span>

<span data-ttu-id="8ca91-106">Legt die Kalender-ID für das angegebene Kalender Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="8ca91-106">Sets the calendar ID for the given calendar control.</span></span> <span data-ttu-id="8ca91-107">Sie können diese Nachricht explizit oder mithilfe des " [**monthcal \_ setcalid"-**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) Makros senden.</span><span class="sxs-lookup"><span data-stu-id="8ca91-107">You can send this message explicitly or by using the [**MonthCal\_SetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8ca91-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ca91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ca91-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8ca91-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ca91-110">Die Kalender-ID.</span><span class="sxs-lookup"><span data-stu-id="8ca91-110">The calendar ID.</span></span> <span data-ttu-id="8ca91-111">Eine der-Konstanten des [Kalender Bezeichner](/windows/desktop/Intl/calendar-identifiers) .</span><span class="sxs-lookup"><span data-stu-id="8ca91-111">One of the [Calendar Identifiers](/windows/desktop/Intl/calendar-identifiers) constants.</span></span>

</dd> <dt>

<span data-ttu-id="8ca91-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ca91-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ca91-113">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="8ca91-113">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ca91-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ca91-114">Return value</span></span>

<span data-ttu-id="8ca91-115">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ca91-115">Unused.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ca91-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ca91-116">Requirements</span></span>



| <span data-ttu-id="8ca91-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ca91-117">Requirement</span></span> | <span data-ttu-id="8ca91-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8ca91-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca91-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8ca91-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8ca91-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ca91-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8ca91-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8ca91-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8ca91-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ca91-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8ca91-123">Header</span><span class="sxs-lookup"><span data-stu-id="8ca91-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ca91-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ca91-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

