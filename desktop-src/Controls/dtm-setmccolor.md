---
title: DTM_SETMCCOLOR Meldung (kommstrg. h)
description: Legt die Farbe für einen bestimmten Teil des Monats Kalenders innerhalb eines DTP-Steuer Elements fest. Sie können diese Nachricht explizit senden oder das DateTime- \_ setmonthcalcolor-Makro verwenden.
ms.assetid: cee72c1d-58da-4ee5-850e-a615ec6ad079
keywords:
- Windows-Steuerelemente für DTM_SETMCCOLOR Meldung
topic_type:
- apiref
api_name:
- DTM_SETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e496abb4dd28b040dd4a8035073ffa32a3f3847
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742561"
---
# <a name="dtm_setmccolor-message"></a><span data-ttu-id="43b47-105">DTM- \_ Nachricht "Abmeldung"</span><span class="sxs-lookup"><span data-stu-id="43b47-105">DTM\_SETMCCOLOR message</span></span>

<span data-ttu-id="43b47-106">Legt die Farbe für einen bestimmten Teil des Monats Kalenders innerhalb eines DTP-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="43b47-106">Sets the color for a given portion of the month calendar within a date and time picker (DTP) control.</span></span> <span data-ttu-id="43b47-107">Sie können diese Nachricht explizit senden oder das [**DateTime- \_ setmonthcalcolor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="43b47-107">You can send this message explicitly or use the [**DateTime\_SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="43b47-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="43b47-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43b47-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43b47-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43b47-110">Ein Wert vom Typ **int** , der angibt, welche Monatskalender Farbe festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="43b47-110">A value of type **int** specifying which month calendar color to set.</span></span> <span data-ttu-id="43b47-111">Die folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="43b47-111">This value can be one of the following:</span></span>



| <span data-ttu-id="43b47-112">Wert</span><span class="sxs-lookup"><span data-stu-id="43b47-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="43b47-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="43b47-113">Meaning</span></span>                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="43b47-114"><dt>**MCSC- \_ Hintergrund**</dt></span><span class="sxs-lookup"><span data-stu-id="43b47-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="43b47-115">Legen Sie die zwischen den Monaten angezeigte Hintergrundfarbe fest.</span><span class="sxs-lookup"><span data-stu-id="43b47-115">Set the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="43b47-116"><dt>**MCSC \_ monthbk**</dt></span><span class="sxs-lookup"><span data-stu-id="43b47-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="43b47-117">Legen Sie die im Monat angezeigte Hintergrundfarbe fest.</span><span class="sxs-lookup"><span data-stu-id="43b47-117">Set the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="43b47-118"><dt>**MCSC- \_ Text**</dt></span><span class="sxs-lookup"><span data-stu-id="43b47-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="43b47-119">Legen Sie die Farbe fest, mit der Text innerhalb eines Monats angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="43b47-119">Set the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="43b47-120"><dt>**MCSC \_ titlebk**</dt></span><span class="sxs-lookup"><span data-stu-id="43b47-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="43b47-121">Legen Sie die im Titel des Kalenders angezeigte Hintergrundfarbe fest.</span><span class="sxs-lookup"><span data-stu-id="43b47-121">Set the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="43b47-122"><dt>**MCSC \_ TitleText**</dt></span><span class="sxs-lookup"><span data-stu-id="43b47-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="43b47-123">Legen Sie die Farbe fest, die verwendet wird, um Text innerhalb des Kalender Titels anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="43b47-123">Set the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="43b47-124"><dt>**MCSC- \_ trailingtext**</dt></span><span class="sxs-lookup"><span data-stu-id="43b47-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="43b47-125">Legen Sie die Farbe fest, die verwendet wird, um den Header Tag und den nachfolgenden Tag</span><span class="sxs-lookup"><span data-stu-id="43b47-125">Set the color used to display header day and trailing day text.</span></span> <span data-ttu-id="43b47-126">Header und nachfolgende Tage sind die Tage aus den vorherigen und den nächsten Monaten, die im Kalender des aktuellen Monats angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="43b47-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="43b47-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43b47-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43b47-128">Ein **COLORREF** -Wert, der die Farbe darstellt, die für den angegebenen Bereich des Monats Kalenders festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="43b47-128">A **COLORREF** value representing the color that will be set for the specified area of the month calendar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43b47-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43b47-129">Return value</span></span>

<span data-ttu-id="43b47-130">Gibt einen **COLORREF** -Wert zurück, der die vorherige Farbeinstellung für den angegebenen Teil des Monatskalender-Steuer Elements darstellt, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="43b47-130">Returns a **COLORREF** value that represents the previous color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="43b47-131">Andernfalls gibt die Meldung-1 zurück.</span><span class="sxs-lookup"><span data-stu-id="43b47-131">Otherwise, the message returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="43b47-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43b47-132">Remarks</span></span>

<span data-ttu-id="43b47-133">Wenn visuelle Stile aktiviert sind, hat diese Meldung keine Auswirkung, es sei denn, *wParam* ist ein MCSC- \_ Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="43b47-133">When visual styles are enabled, this message has no effect except when *wParam* is MCSC\_BACKGROUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="43b47-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43b47-134">Requirements</span></span>



| <span data-ttu-id="43b47-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43b47-135">Requirement</span></span> | <span data-ttu-id="43b47-136">Wert</span><span class="sxs-lookup"><span data-stu-id="43b47-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43b47-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43b47-137">Minimum supported client</span></span><br/> | <span data-ttu-id="43b47-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43b47-138">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43b47-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43b47-139">Minimum supported server</span></span><br/> | <span data-ttu-id="43b47-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43b47-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43b47-141">Header</span><span class="sxs-lookup"><span data-stu-id="43b47-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="43b47-142"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="43b47-142"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





