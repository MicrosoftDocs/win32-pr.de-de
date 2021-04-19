---
title: Monatskalender-Steuerelement Stile (kommctrl. h)
description: Die folgenden Stil Konstanten werden verwendet, wenn Sie Monatskalender-Steuerelemente erstellen.
ms.assetid: 8d9b2239-fd13-4579-81a2-0385fd318e83
topic_type:
- apiref
api_name:
- MCS_DAYSTATE
- MCS_MULTISELECT
- MCS_WEEKNUMBERS
- MCS_NOTODAYCIRCLE
- MCS_NOTODAY
- MCS_NOTRAILINGDATES
- MCS_SHORTDAYSOFWEEK
- MCS_NOSELCHANGEONNAV
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45ccef4a3cc8e16851c0676b8b0dce8c53cfdd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360401"
---
# <a name="month-calendar-control-styles"></a><span data-ttu-id="ec7ce-103">Monatskalender-Steuerelement Stile</span><span class="sxs-lookup"><span data-stu-id="ec7ce-103">Month Calendar Control Styles</span></span>

<span data-ttu-id="ec7ce-104">Die folgenden Stil Konstanten werden verwendet, wenn Sie Monatskalender-Steuerelemente erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec7ce-104">The following style constants are used when creating month calendar controls.</span></span>



| <span data-ttu-id="ec7ce-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="ec7ce-105">Constant</span></span>                                                                                                                                                                           | <span data-ttu-id="ec7ce-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec7ce-106">Description</span></span>                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_DAYSTATE"></span><span id="mcs_daystate"></span><dl> <span data-ttu-id="ec7ce-107"><dt>**MCS \_ daystate**</dt></span><span class="sxs-lookup"><span data-stu-id="ec7ce-107"><dt>**MCS\_DAYSTATE**</dt></span></span> </dl>                         | <span data-ttu-id="ec7ce-108">[Version 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="ec7ce-108">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="ec7ce-109">Der Monatskalender sendet [MCN \_ getdaystate](mcn-getdaystate.md) -Benachrichtigungen, um Informationen darüber anzufordern, welche Tage fett angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ec7ce-109">The month calendar sends [MCN\_GETDAYSTATE](mcn-getdaystate.md) notifications to request information about which days should be displayed in bold.</span></span><br/>                                                                                                          |
| <span id="MCS_MULTISELECT"></span><span id="mcs_multiselect"></span><dl> <span data-ttu-id="ec7ce-110"><dt>**MCS- \_ Mehrfachauswahl**</dt></span><span class="sxs-lookup"><span data-stu-id="ec7ce-110"><dt>**MCS\_MULTISELECT**</dt></span></span> </dl>                | <span data-ttu-id="ec7ce-111">[Version 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="ec7ce-111">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="ec7ce-112">Der Monatskalender ermöglicht dem Benutzer die Auswahl eines Datums Bereichs innerhalb des-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="ec7ce-112">The month calendar enables the user to select a range of dates within the control.</span></span> <span data-ttu-id="ec7ce-113">Standardmäßig beträgt der maximale Bereich eine Woche.</span><span class="sxs-lookup"><span data-stu-id="ec7ce-113">By default, the maximum range is one week.</span></span> <span data-ttu-id="ec7ce-114">Sie können den maximalen Bereich, der ausgewählt werden kann, mithilfe der [**MCM \_ setmaxselcount**](mcm-setmaxselcount.md) -Nachricht ändern.</span><span class="sxs-lookup"><span data-stu-id="ec7ce-114">You can change the maximum range that can be selected by using the [**MCM\_SETMAXSELCOUNT**](mcm-setmaxselcount.md) message.</span></span> <br/> |
| <span id="MCS_WEEKNUMBERS"></span><span id="mcs_weeknumbers"></span><dl> <span data-ttu-id="ec7ce-115"><dt>**MCS- \_ Wochen Nummern**</dt></span><span class="sxs-lookup"><span data-stu-id="ec7ce-115"><dt>**MCS\_WEEKNUMBERS**</dt></span></span> </dl>                | <span data-ttu-id="ec7ce-116">[Version 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="ec7ce-116">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="ec7ce-117">Das Monatskalender-Steuerelement zeigt die Wochen Nummern (1-52) links neben den Zeilen der Tage an.</span><span class="sxs-lookup"><span data-stu-id="ec7ce-117">The month calendar control displays week numbers (1-52) to the left of each row of days.</span></span> <span data-ttu-id="ec7ce-118">Woche 1 wird als erste Woche definiert, die mindestens vier Tage umfasst.</span><span class="sxs-lookup"><span data-stu-id="ec7ce-118">Week 1 is defined as the first week that contains at least four days.</span></span> <br/>                                                                                              |
| <span id="MCS_NOTODAYCIRCLE"></span><span id="mcs_notodaycircle"></span><dl> <span data-ttu-id="ec7ce-119"><dt>**MCS \_ noumdaycircle**</dt></span><span class="sxs-lookup"><span data-stu-id="ec7ce-119"><dt>**MCS\_NOTODAYCIRCLE**</dt></span></span> </dl>          | <span data-ttu-id="ec7ce-120">[Version 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="ec7ce-120">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="ec7ce-121">Das Month Calendar-Steuerelement Zirkel nicht das heutige Datum.</span><span class="sxs-lookup"><span data-stu-id="ec7ce-121">The month calendar control does not circle the "today" date.</span></span> <br/>                                                                                                                                                                                                |
| <span id="MCS_NOTODAY"></span><span id="mcs_notoday"></span><dl> <span data-ttu-id="ec7ce-122"><dt>**MCS \_ notoday**</dt></span><span class="sxs-lookup"><span data-stu-id="ec7ce-122"><dt>**MCS\_NOTODAY**</dt></span></span> </dl>                            | <span data-ttu-id="ec7ce-123">[Version 4,70](common-control-versions.md). Im Monatskalender-Steuerelement wird nicht das heutige Datum am unteren Rand des Steuer Elements angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ec7ce-123">[Version 4.70](common-control-versions.md).The month calendar control does not display the "today" date at the bottom of the control.</span></span> <br/>                                                                                                                                                                   |
| <span id="MCS_NOTRAILINGDATES"></span><span id="mcs_notrailingdates"></span><dl> <span data-ttu-id="ec7ce-124"><dt>**MCS \_ notrailingdates**</dt></span><span class="sxs-lookup"><span data-stu-id="ec7ce-124"><dt>**MCS\_NOTRAILINGDATES**</dt></span></span> </dl>    | <span data-ttu-id="ec7ce-125">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="ec7ce-125">**Windows Vista.**</span></span> <span data-ttu-id="ec7ce-126">Datumsangaben aus dem vorherigen und den nächsten Monaten werden im Kalender des aktuellen Monats nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ec7ce-126">Dates from the previous and next months are not displayed in the current month's calendar.</span></span><br/>                                                                                                                                                                                              |
| <span id="MCS_SHORTDAYSOFWEEK"></span><span id="mcs_shortdaysofweek"></span><dl> <span data-ttu-id="ec7ce-127"><dt>**MCS \_ shortdaysofweek**</dt></span><span class="sxs-lookup"><span data-stu-id="ec7ce-127"><dt>**MCS\_SHORTDAYSOFWEEK**</dt></span></span> </dl>    | <span data-ttu-id="ec7ce-128">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="ec7ce-128">**Windows Vista.**</span></span> <span data-ttu-id="ec7ce-129">Kurztagnamen werden in der Kopfzeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ec7ce-129">Short day names are displayed in the header.</span></span><br/>                                                                                                                                                                                                                                            |
| <span id="MCS_NOSELCHANGEONNAV"></span><span id="mcs_noselchangeonnav"></span><dl> <span data-ttu-id="ec7ce-130"><dt>**MCS \_ noselchangeonnav**</dt></span><span class="sxs-lookup"><span data-stu-id="ec7ce-130"><dt>**MCS\_NOSELCHANGEONNAV**</dt></span></span> </dl> | <span data-ttu-id="ec7ce-131">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="ec7ce-131">**Windows Vista.**</span></span> <span data-ttu-id="ec7ce-132">Die Auswahl wird nicht geändert, wenn der Benutzer im Kalender auf "Next" oder "Previous" navigiert.</span><span class="sxs-lookup"><span data-stu-id="ec7ce-132">The selection is not changed when the user navigates next or previous in the calendar.</span></span> <span data-ttu-id="ec7ce-133">Dadurch kann der Benutzer einen Bereich auswählen, der größer als sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="ec7ce-133">This allows the user to select a range larger than is visible.</span></span><br/>                                                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="ec7ce-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec7ce-134">Requirements</span></span>



| <span data-ttu-id="ec7ce-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec7ce-135">Requirement</span></span> | <span data-ttu-id="ec7ce-136">Wert</span><span class="sxs-lookup"><span data-stu-id="ec7ce-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec7ce-137">Header</span><span class="sxs-lookup"><span data-stu-id="ec7ce-137">Header</span></span><br/> | <dl> <span data-ttu-id="ec7ce-138"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec7ce-138"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





