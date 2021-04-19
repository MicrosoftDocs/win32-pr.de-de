---
title: MCM_SETFIRSTDAYOFWEEK Meldung (kommstrg. h)
description: Legt den ersten Tag der Woche für ein Monatskalender-Steuerelement fest. Sie können diese Nachricht explizit oder mit dem monthcal \_ setfirstdayof Week-Makro senden.
ms.assetid: 6e0dc906-a41e-4c3a-9528-1f5428dceb8d
keywords:
- Windows-Steuerelemente für MCM_SETFIRSTDAYOFWEEK Meldung
topic_type:
- apiref
api_name:
- MCM_SETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32452c9043bbd7c3bbcf96f9dc32e67714eacce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343059"
---
# <a name="mcm_setfirstdayofweek-message"></a><span data-ttu-id="37497-105">MCM \_ setfirstdayof Week-Meldung</span><span class="sxs-lookup"><span data-stu-id="37497-105">MCM\_SETFIRSTDAYOFWEEK message</span></span>

<span data-ttu-id="37497-106">Legt den ersten Tag der Woche für ein Monatskalender-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="37497-106">Sets the first day of the week for a month calendar control.</span></span> <span data-ttu-id="37497-107">Sie können diese Nachricht explizit oder mit dem [**monthcal \_ setfirstdayof Week**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="37497-107">You can send this message explicitly or by using the [**MonthCal\_SetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="37497-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="37497-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37497-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37497-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="37497-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="37497-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="37497-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37497-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37497-112">Ein Wert vom Typ **int** , der angibt, welcher Tag als erster Wochentag festgelegt werden soll, wobei 0 für Montag, 1 für Dienstag usw. steht.</span><span class="sxs-lookup"><span data-stu-id="37497-112">Value of type **int** representing which day is to be set as the first day of the week, where 0 is Monday, 1 is Tuesday, and so on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37497-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37497-113">Return value</span></span>

<span data-ttu-id="37497-114">Gibt einen **DWORD** -Wert zurück, der zwei Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="37497-114">Returns a **DWORD** value that contains two values.</span></span> <span data-ttu-id="37497-115">Das hohe Wort ist ein **boolescher** Wert, der ungleich 0 (null) ist, wenn der vorherige erste Tag der Woche nicht dem Gebiets Schema \_ ifirstdayosweek entspricht, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="37497-115">The high word is a **BOOL** value that is nonzero if the previous first day of the week did not equal LOCALE\_IFIRSTDAYOFWEEK, or zero otherwise.</span></span> <span data-ttu-id="37497-116">Das niedrige Wort ist ein int-Wert, der den vorherigen ersten Tag der Woche darstellt.</span><span class="sxs-lookup"><span data-stu-id="37497-116">The low word is an INT value that represents the previous first day of the week.</span></span>

## <a name="remarks"></a><span data-ttu-id="37497-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37497-117">Remarks</span></span>

<span data-ttu-id="37497-118">Wenn der erste Tag der Woche auf einen anderen Wert als den Standardwert festgelegt ist (Gebiets Schema \_ ifirstdayofweek), aktualisiert das Steuerelement die Änderungen am Wochentag nicht automatisch basierend auf Gebiets Schema Änderungen.</span><span class="sxs-lookup"><span data-stu-id="37497-118">If the first day of the week is set to anything other than the default (LOCALE\_IFIRSTDAYOFWEEK), the control will not automatically update first-day-of-the-week changes based on locale changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="37497-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37497-119">Requirements</span></span>



| <span data-ttu-id="37497-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37497-120">Requirement</span></span> | <span data-ttu-id="37497-121">Wert</span><span class="sxs-lookup"><span data-stu-id="37497-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37497-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37497-122">Minimum supported client</span></span><br/> | <span data-ttu-id="37497-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37497-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37497-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37497-124">Minimum supported server</span></span><br/> | <span data-ttu-id="37497-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37497-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="37497-126">Header</span><span class="sxs-lookup"><span data-stu-id="37497-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="37497-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="37497-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





