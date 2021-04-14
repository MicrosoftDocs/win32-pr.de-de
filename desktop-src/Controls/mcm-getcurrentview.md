---
title: MCM_GETCURRENTVIEW Meldung (kommstrg. h)
description: Ruft die aktuelle Ansicht des Kalenders ab. Sie können diese Nachricht explizit oder mit dem monthcal \_ getcurrentview-Makro senden.
ms.assetid: 9c42ebf6-611e-4e50-9dcc-cf7fd63b32eb
keywords:
- Windows-Steuerelemente für MCM_GETCURRENTVIEW Meldung
topic_type:
- apiref
api_name:
- MCM_GETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eebbd6a2b33043294b64b8b65308520b52dbe449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478492"
---
# <a name="mcm_getcurrentview-message"></a><span data-ttu-id="256c4-105">MCM \_ getcurrentview-Meldung</span><span class="sxs-lookup"><span data-stu-id="256c4-105">MCM\_GETCURRENTVIEW message</span></span>

<span data-ttu-id="256c4-106">Ruft die aktuelle Ansicht des Kalenders ab.</span><span class="sxs-lookup"><span data-stu-id="256c4-106">Gets the current view of the calendar.</span></span> <span data-ttu-id="256c4-107">Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getcurrentview**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="256c4-107">You can send this message explicitly or by using the [**MonthCal\_GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="256c4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="256c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="256c4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="256c4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="256c4-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="256c4-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="256c4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="256c4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="256c4-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="256c4-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="256c4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="256c4-113">Return value</span></span>

<span data-ttu-id="256c4-114">Aktuelle Ansicht.</span><span class="sxs-lookup"><span data-stu-id="256c4-114">Current view.</span></span> <span data-ttu-id="256c4-115">Einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="256c4-115">One of the following values.</span></span>



| <span data-ttu-id="256c4-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="256c4-116">Return code</span></span>                                                                                  | <span data-ttu-id="256c4-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="256c4-117">Description</span></span>              |
|----------------------------------------------------------------------------------------------|--------------------------|
| <dl> <span data-ttu-id="256c4-118"><dt>**mcmv- \_ Monat**</dt></span><span class="sxs-lookup"><span data-stu-id="256c4-118"><dt>**MCMV\_MONTH**</dt></span></span> </dl>   | <span data-ttu-id="256c4-119">Monatliche Ansicht.</span><span class="sxs-lookup"><span data-stu-id="256c4-119">Monthly view.</span></span><br/> |
| <dl> <span data-ttu-id="256c4-120"><dt>**mcmv- \_ Jahr**</dt></span><span class="sxs-lookup"><span data-stu-id="256c4-120"><dt>**MCMV\_YEAR**</dt></span></span> </dl>    | <span data-ttu-id="256c4-121">Jährliche Ansicht.</span><span class="sxs-lookup"><span data-stu-id="256c4-121">Annual view.</span></span><br/>  |
| <dl> <span data-ttu-id="256c4-122"><dt>**mcmv- \_ Jahrzehnt**</dt></span><span class="sxs-lookup"><span data-stu-id="256c4-122"><dt>**MCMV\_DECADE**</dt></span></span> </dl>  | <span data-ttu-id="256c4-123">Dekade-Ansicht.</span><span class="sxs-lookup"><span data-stu-id="256c4-123">Decade view.</span></span><br/>  |
| <dl> <span data-ttu-id="256c4-124"><dt>**mcmv \_ Jahrhundert**</dt></span><span class="sxs-lookup"><span data-stu-id="256c4-124"><dt>**MCMV\_CENTURY**</dt></span></span> </dl> | <span data-ttu-id="256c4-125">Jahrhundert Ansicht.</span><span class="sxs-lookup"><span data-stu-id="256c4-125">Century view.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="256c4-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="256c4-126">Requirements</span></span>



| <span data-ttu-id="256c4-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="256c4-127">Requirement</span></span> | <span data-ttu-id="256c4-128">Wert</span><span class="sxs-lookup"><span data-stu-id="256c4-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="256c4-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="256c4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="256c4-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="256c4-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="256c4-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="256c4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="256c4-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="256c4-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="256c4-133">Header</span><span class="sxs-lookup"><span data-stu-id="256c4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="256c4-134"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="256c4-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





