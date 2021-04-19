---
title: MCM_GETMONTHRANGE Meldung (kommstrg. h)
description: Ruft Datumsinformationen (mithilfe von SYSTEMTIME-Strukturen) ab, die die hohen und unteren Grenzen der Anzeige eines Monatskalender-Steuer Elements darstellen. Sie können diese Nachricht explizit oder mit dem monthcal \_ getmonthrange-Makro senden.
ms.assetid: f50ac4b7-1f58-4639-8c78-341bb33db3c3
keywords:
- Windows-Steuerelemente für MCM_GETMONTHRANGE Meldung
topic_type:
- apiref
api_name:
- MCM_GETMONTHRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022ca7e05cc0c69cd32f6ad92531420cdaed7c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343895"
---
# <a name="mcm_getmonthrange-message"></a><span data-ttu-id="2ccd5-105">MCM \_ getmonthrange-Meldung</span><span class="sxs-lookup"><span data-stu-id="2ccd5-105">MCM\_GETMONTHRANGE message</span></span>

<span data-ttu-id="2ccd5-106">Ruft Datumsinformationen (mithilfe von [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Strukturen) ab, die die hohen und unteren Grenzen der Anzeige eines Monatskalender-Steuer Elements darstellen.</span><span class="sxs-lookup"><span data-stu-id="2ccd5-106">Retrieves date information (using [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures) that represents the high and low limits of a month calendar control's display.</span></span> <span data-ttu-id="2ccd5-107">Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getmonthrange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="2ccd5-107">You can send this message explicitly or by using the [**MonthCal\_GetMonthRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ccd5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ccd5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ccd5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ccd5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ccd5-110">-Wert, der den Gültigkeitsbereich der abzurufenden Bereichs Begrenzungen angibt.</span><span class="sxs-lookup"><span data-stu-id="2ccd5-110">Value specifying the scope of the range limits to be retrieved.</span></span> <span data-ttu-id="2ccd5-111">Dieser Wert muss einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="2ccd5-111">This value must be one of the following:</span></span>



| <span data-ttu-id="2ccd5-112">Wert</span><span class="sxs-lookup"><span data-stu-id="2ccd5-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="2ccd5-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2ccd5-113">Meaning</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="GMR_DAYSTATE"></span><span id="gmr_daystate"></span><dl> <span data-ttu-id="2ccd5-114"><dt>**GMR \_ daystate**</dt></span><span class="sxs-lookup"><span data-stu-id="2ccd5-114"><dt>**GMR\_DAYSTATE**</dt></span></span> </dl> | <span data-ttu-id="2ccd5-115">Schließt vorangestellte und nachfolgende Monate des sichtbaren Bereichs ein, die nur teilweise angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2ccd5-115">Include preceding and trailing months of visible range that are only partially displayed.</span></span> <br/> |
| <span id="GMR_VISIBLE"></span><span id="gmr_visible"></span><dl> <span data-ttu-id="2ccd5-116"><dt>**GMR \_ sichtbar**</dt></span><span class="sxs-lookup"><span data-stu-id="2ccd5-116"><dt>**GMR\_VISIBLE**</dt></span></span> </dl>    | <span data-ttu-id="2ccd5-117">Schließen Sie nur die Monate ein, die vollständig angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2ccd5-117">Include only those months that are entirely displayed.</span></span> <br/>                                    |



 

</dd> <dt>

<span data-ttu-id="2ccd5-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ccd5-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ccd5-119">Ein Zeiger auf ein zwei-Element-Array von [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Strukturen, das die unteren und oberen Begrenzungen des durch *wParam* angegebenen Bereichs empfängt.</span><span class="sxs-lookup"><span data-stu-id="2ccd5-119">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the lower and upper limits of the scope specified by *wParam*.</span></span> <span data-ttu-id="2ccd5-120">Die unteren und oberen Grenzwerte werden in *lprgsystimearray* \[ 0 \] bzw. *lprgsystimearray* \[ 1 platziert \] .</span><span class="sxs-lookup"><span data-stu-id="2ccd5-120">The lower and upper limits are placed in *lprgSysTimeArray*\[0\] and *lprgSysTimeArray*\[1\], respectively.</span></span> <span data-ttu-id="2ccd5-121">Dieser Parameter muss eine gültige Adresse sein und darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="2ccd5-121">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ccd5-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ccd5-122">Return value</span></span>

<span data-ttu-id="2ccd5-123">Gibt einen int-Wert zurück, der den Bereich in Monaten darstellt, über den die beiden bei *LPARAM* zurückgegebenen Grenzwerte liegen.</span><span class="sxs-lookup"><span data-stu-id="2ccd5-123">Returns an INT value that represents the range, in months, spanned by the two limits returned at *lParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ccd5-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ccd5-124">Requirements</span></span>



| <span data-ttu-id="2ccd5-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ccd5-125">Requirement</span></span> | <span data-ttu-id="2ccd5-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2ccd5-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ccd5-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ccd5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2ccd5-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ccd5-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2ccd5-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ccd5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2ccd5-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ccd5-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ccd5-131">Header</span><span class="sxs-lookup"><span data-stu-id="2ccd5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ccd5-132"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ccd5-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ccd5-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ccd5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ccd5-134">Uhrzeiten im Monatskalender-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="2ccd5-134">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

