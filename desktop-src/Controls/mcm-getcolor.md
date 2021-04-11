---
title: MCM_GETCOLOR Meldung (kommstrg. h)
description: Ruft die Farbe für einen angegebenen Teil eines Monatskalender-Steuer Elements ab. Sie können diese Nachricht explizit oder mit dem monthcal \_ GetColor-Makro senden.
ms.assetid: 6c30ad0d-7584-402a-9c27-3c12c49c87f3
keywords:
- Windows-Steuerelemente für MCM_GETCOLOR Meldung
topic_type:
- apiref
api_name:
- MCM_GETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932b457bd1ddd870fd84facdb540e31188825504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105458"
---
# <a name="mcm_getcolor-message"></a><span data-ttu-id="aa94f-105">MCM- \_ GetColor-Meldung</span><span class="sxs-lookup"><span data-stu-id="aa94f-105">MCM\_GETCOLOR message</span></span>

<span data-ttu-id="aa94f-106">Ruft die Farbe für einen angegebenen Teil eines Monatskalender-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="aa94f-106">Retrieves the color for a given portion of a month calendar control.</span></span> <span data-ttu-id="aa94f-107">Sie können diese Nachricht explizit oder mit dem [**monthcal \_ GetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="aa94f-107">You can send this message explicitly or by using the [**MonthCal\_GetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="aa94f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa94f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa94f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa94f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa94f-110">Ein Wert vom Typ **int** , der angibt, welche Monatskalender Farbe abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa94f-110">Value of type **int** specifying which month calendar color to retrieve.</span></span> <span data-ttu-id="aa94f-111">Die folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="aa94f-111">This value can be one of the following:</span></span>



| <span data-ttu-id="aa94f-112">Wert</span><span class="sxs-lookup"><span data-stu-id="aa94f-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="aa94f-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="aa94f-113">Meaning</span></span>                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="aa94f-114"><dt>**MCSC- \_ Hintergrund**</dt></span><span class="sxs-lookup"><span data-stu-id="aa94f-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="aa94f-115">Rufen Sie die zwischen Monaten angezeigte Hintergrundfarbe ab.</span><span class="sxs-lookup"><span data-stu-id="aa94f-115">Retrieve the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="aa94f-116"><dt>**MCSC \_ monthbk**</dt></span><span class="sxs-lookup"><span data-stu-id="aa94f-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="aa94f-117">Rufen Sie die im Monat angezeigte Hintergrundfarbe ab.</span><span class="sxs-lookup"><span data-stu-id="aa94f-117">Retrieve the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="aa94f-118"><dt>**MCSC- \_ Text**</dt></span><span class="sxs-lookup"><span data-stu-id="aa94f-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="aa94f-119">Ruft die Farbe ab, die zum Anzeigen von Text innerhalb eines Monats verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aa94f-119">Retrieve the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="aa94f-120"><dt>**MCSC \_ titlebk**</dt></span><span class="sxs-lookup"><span data-stu-id="aa94f-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="aa94f-121">Ruft die im Titel des Kalenders angezeigte Hintergrundfarbe ab.</span><span class="sxs-lookup"><span data-stu-id="aa94f-121">Retrieve the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="aa94f-122"><dt>**MCSC \_ TitleText**</dt></span><span class="sxs-lookup"><span data-stu-id="aa94f-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="aa94f-123">Ruft die Farbe ab, die zum Anzeigen von Text innerhalb des Kalender Titels verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aa94f-123">Retrieve the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="aa94f-124"><dt>**MCSC- \_ trailingtext**</dt></span><span class="sxs-lookup"><span data-stu-id="aa94f-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="aa94f-125">Ruft die Farbe ab, die zum Anzeigen des Header Tags und des nachfolgenden Tages Textes verwendet wird</span><span class="sxs-lookup"><span data-stu-id="aa94f-125">Retrieve the color used to display header day and trailing day text.</span></span> <span data-ttu-id="aa94f-126">Header und nachfolgende Tage sind die Tage aus den vorherigen und den nächsten Monaten, die im Kalender des aktuellen Monats angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="aa94f-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="aa94f-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa94f-127">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="aa94f-128">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="aa94f-128">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa94f-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa94f-129">Return value</span></span>

<span data-ttu-id="aa94f-130">Gibt einen **COLORREF** -Wert zurück, der die Farbeinstellung für den angegebenen Teil des Monatskalender-Steuer Elements darstellt, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="aa94f-130">Returns a **COLORREF** value that represents the color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="aa94f-131">Andernfalls gibt diese Meldung-1 zurück.</span><span class="sxs-lookup"><span data-stu-id="aa94f-131">Otherwise, this message returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa94f-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa94f-132">Requirements</span></span>



| <span data-ttu-id="aa94f-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa94f-133">Requirement</span></span> | <span data-ttu-id="aa94f-134">Wert</span><span class="sxs-lookup"><span data-stu-id="aa94f-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa94f-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa94f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="aa94f-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa94f-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aa94f-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa94f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="aa94f-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa94f-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aa94f-139">Header</span><span class="sxs-lookup"><span data-stu-id="aa94f-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa94f-140"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa94f-140"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





