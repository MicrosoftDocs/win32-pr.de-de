---
title: MCM_SETCURRENTVIEW Meldung (kommstrg. h)
description: Legt die aktuelle Ansicht des Kalenders fest. Sie können diese Nachricht explizit oder mit dem monthcal \_ SetCurrentView-Makro senden.
ms.assetid: 26ccbb80-0dba-4241-a2eb-b79000fc3618
keywords:
- Windows-Steuerelemente für MCM_SETCURRENTVIEW Meldung
topic_type:
- apiref
api_name:
- MCM_SETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d383c984932c19805f452cb39841c2edf36809b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957104"
---
# <a name="mcm_setcurrentview-message"></a><span data-ttu-id="ec75d-105">MCM \_ SetCurrentView-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ec75d-105">MCM\_SETCURRENTVIEW message</span></span>

<span data-ttu-id="ec75d-106">Legt die aktuelle Ansicht des Kalenders fest.</span><span class="sxs-lookup"><span data-stu-id="ec75d-106">Sets the current view of the calendar.</span></span> <span data-ttu-id="ec75d-107">Sie können diese Nachricht explizit oder mit dem [**monthcal \_ SetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="ec75d-107">You can send this message explicitly or by using the [**MonthCal\_SetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ec75d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec75d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec75d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec75d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec75d-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ec75d-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ec75d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec75d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec75d-112">Neue Ansicht.</span><span class="sxs-lookup"><span data-stu-id="ec75d-112">New view.</span></span> <span data-ttu-id="ec75d-113">Eine der folgenden Konstanten.</span><span class="sxs-lookup"><span data-stu-id="ec75d-113">One of the following constants.</span></span>



| <span data-ttu-id="ec75d-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ec75d-114">Value</span></span>                                                                                                                                                      | <span data-ttu-id="ec75d-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ec75d-115">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="MCMV_MONTH"></span><span id="mcmv_month"></span><dl> <span data-ttu-id="ec75d-116"><dt>**mcmv- \_ Monat**</dt></span><span class="sxs-lookup"><span data-stu-id="ec75d-116"><dt>**MCMV\_MONTH**</dt></span></span> </dl>       | <span data-ttu-id="ec75d-117">Monatliche Ansicht.</span><span class="sxs-lookup"><span data-stu-id="ec75d-117">Monthly view.</span></span><br/> |
| <span id="MCMV_YEAR"></span><span id="mcmv_year"></span><dl> <span data-ttu-id="ec75d-118"><dt>**mcmv- \_ Jahr**</dt></span><span class="sxs-lookup"><span data-stu-id="ec75d-118"><dt>**MCMV\_YEAR**</dt></span></span> </dl>          | <span data-ttu-id="ec75d-119">Jährliche Ansicht.</span><span class="sxs-lookup"><span data-stu-id="ec75d-119">Annual view.</span></span><br/>  |
| <span id="MCMV_DECADE"></span><span id="mcmv_decade"></span><dl> <span data-ttu-id="ec75d-120"><dt>**mcmv- \_ Jahrzehnt**</dt></span><span class="sxs-lookup"><span data-stu-id="ec75d-120"><dt>**MCMV\_DECADE**</dt></span></span> </dl>    | <span data-ttu-id="ec75d-121">Dekade-Ansicht.</span><span class="sxs-lookup"><span data-stu-id="ec75d-121">Decade view.</span></span><br/>  |
| <span id="MCMV_CENTURY"></span><span id="mcmv_century"></span><dl> <span data-ttu-id="ec75d-122"><dt>**mcmv \_ Jahrhundert**</dt></span><span class="sxs-lookup"><span data-stu-id="ec75d-122"><dt>**MCMV\_CENTURY**</dt></span></span> </dl> | <span data-ttu-id="ec75d-123">Jahrhundert Ansicht.</span><span class="sxs-lookup"><span data-stu-id="ec75d-123">Century view.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec75d-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec75d-124">Return value</span></span>

<span data-ttu-id="ec75d-125">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="ec75d-125">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec75d-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec75d-126">Requirements</span></span>



| <span data-ttu-id="ec75d-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec75d-127">Requirement</span></span> | <span data-ttu-id="ec75d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ec75d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec75d-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ec75d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ec75d-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec75d-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec75d-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ec75d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ec75d-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec75d-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec75d-133">Header</span><span class="sxs-lookup"><span data-stu-id="ec75d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec75d-134"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec75d-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





