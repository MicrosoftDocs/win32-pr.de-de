---
description: In diesem Thema werden die Kalender Bezeichner (Datentyp-Calid) definiert, die zur Angabe unterschiedlicher Kalender verwendet werden.
ms.assetid: ba2e841e-e24e-476a-851e-a29b3af4f04d
title: Kalender Bezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9b931aea4a186af0849dfe8f6642c53744d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751153"
---
# <a name="calendar-identifiers"></a><span data-ttu-id="f1300-103">Kalender Bezeichner</span><span class="sxs-lookup"><span data-stu-id="f1300-103">Calendar Identifiers</span></span>

<span data-ttu-id="f1300-104">In diesem Thema werden die Kalender Bezeichner (Datentyp-Calid) definiert, die zur Angabe unterschiedlicher Kalender verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1300-104">This topic defines the calendar identifiers (data type CALID) that are used to specify different calendars.</span></span> <span data-ttu-id="f1300-105">Ihre Anwendungen können diese Bezeichner verwenden, wenn Sie die folgenden nls-Funktionen und-Rückruf Funktionen verwenden, die über Parameter verfügen, die den Datentyp "Calid" akzeptieren:</span><span class="sxs-lookup"><span data-stu-id="f1300-105">Your applications can use these identifiers when using the following NLS functions and callback functions, which have parameters that take the CALID data type:</span></span>

-   [<span data-ttu-id="f1300-106">**Convertsystemtimeumcaldatetime**</span><span class="sxs-lookup"><span data-stu-id="f1300-106">**ConvertSystemTimeToCalDateTime**</span></span>](convertsystemtimetocaldatetime.md)
-   [<span data-ttu-id="f1300-107">**Enumcalendarinfo**</span><span class="sxs-lookup"><span data-stu-id="f1300-107">**EnumCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa)
-   [<span data-ttu-id="f1300-108">**Enumcalendarinfoex**</span><span class="sxs-lookup"><span data-stu-id="f1300-108">**EnumCalendarInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa)
-   [<span data-ttu-id="f1300-109">**Enumcalendarinfoexex**</span><span class="sxs-lookup"><span data-stu-id="f1300-109">**EnumCalendarInfoExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)
-   <span data-ttu-id="f1300-110">[**Enumcalendarinfoprocex**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1300-110">[**EnumCalendarInfoProcEx**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))</span></span>
-   <span data-ttu-id="f1300-111">[**Enumdateformatsprocex**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1300-111">[**EnumDateFormatsProcEx**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))</span></span>
-   [<span data-ttu-id="f1300-112">**Getcalendarinfo**</span><span class="sxs-lookup"><span data-stu-id="f1300-112">**GetCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)
-   [<span data-ttu-id="f1300-113">**Getcalendarinfoex**</span><span class="sxs-lookup"><span data-stu-id="f1300-113">**GetCalendarInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)
-   [<span data-ttu-id="f1300-114">**Getcalendarsupporteddaterange**</span><span class="sxs-lookup"><span data-stu-id="f1300-114">**GetCalendarSupportedDateRange**</span></span>](getcalendarsupporteddaterange.md)
-   [<span data-ttu-id="f1300-115">**Iscalendarleapyear**</span><span class="sxs-lookup"><span data-stu-id="f1300-115">**IsCalendarLeapYear**</span></span>](iscalendarleapyear.md)
-   [<span data-ttu-id="f1300-116">**Setcalendarinfo**</span><span class="sxs-lookup"><span data-stu-id="f1300-116">**SetCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa)

<span data-ttu-id="f1300-117">Die folgenden Werte sind definiert.</span><span class="sxs-lookup"><span data-stu-id="f1300-117">The following values are defined.</span></span> <span data-ttu-id="f1300-118">Alle anderen Werte sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="f1300-118">All other values are reserved.</span></span> <span data-ttu-id="f1300-119">Diese Werte können nicht miteinander kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="f1300-119">These values cannot be combined with one another.</span></span>



<span data-ttu-id="f1300-120">Kalender-ID</span><span class="sxs-lookup"><span data-stu-id="f1300-120">Calendar identifier</span></span>

<span data-ttu-id="f1300-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f1300-121">Meaning</span></span>

<span data-ttu-id="f1300-122">1</span><span class="sxs-lookup"><span data-stu-id="f1300-122">1</span></span>

<span data-ttu-id="f1300-123">Cal \_ Gregorianisch</span><span class="sxs-lookup"><span data-stu-id="f1300-123">CAL\_GREGORIAN</span></span>

<span data-ttu-id="f1300-124">Gregorianisch (lokalisiert)</span><span class="sxs-lookup"><span data-stu-id="f1300-124">Gregorian (localized)</span></span>

<span data-ttu-id="f1300-125">2</span><span class="sxs-lookup"><span data-stu-id="f1300-125">2</span></span>

<span data-ttu-id="f1300-126">Cal- \_ Gregorianisch \_</span><span class="sxs-lookup"><span data-stu-id="f1300-126">CAL\_GREGORIAN\_US</span></span>

<span data-ttu-id="f1300-127">Gregorianisch (englische Zeichen folgen immer)</span><span class="sxs-lookup"><span data-stu-id="f1300-127">Gregorian (English strings always)</span></span>

<span data-ttu-id="f1300-128">3</span><span class="sxs-lookup"><span data-stu-id="f1300-128">3</span></span>

<span data-ttu-id="f1300-129">Cal \_ Japan</span><span class="sxs-lookup"><span data-stu-id="f1300-129">CAL\_JAPAN</span></span>

<span data-ttu-id="f1300-130">Japanischer Kaiser ERA</span><span class="sxs-lookup"><span data-stu-id="f1300-130">Japanese Emperor Era</span></span>

<span data-ttu-id="f1300-131">4</span><span class="sxs-lookup"><span data-stu-id="f1300-131">4</span></span>

<span data-ttu-id="f1300-132">Cal- \_ Taiwan</span><span class="sxs-lookup"><span data-stu-id="f1300-132">CAL\_TAIWAN</span></span>

<span data-ttu-id="f1300-133">Taiwan-Kalender</span><span class="sxs-lookup"><span data-stu-id="f1300-133">Taiwan calendar</span></span>

<span data-ttu-id="f1300-134">5</span><span class="sxs-lookup"><span data-stu-id="f1300-134">5</span></span>

<span data-ttu-id="f1300-135">Cal \_ Korea</span><span class="sxs-lookup"><span data-stu-id="f1300-135">CAL\_KOREA</span></span>

<span data-ttu-id="f1300-136">Koreanischer Tangun-Zeitraum</span><span class="sxs-lookup"><span data-stu-id="f1300-136">Korean Tangun Era</span></span>

<span data-ttu-id="f1300-137">6</span><span class="sxs-lookup"><span data-stu-id="f1300-137">6</span></span>

<span data-ttu-id="f1300-138">Cal- \_ Hijri</span><span class="sxs-lookup"><span data-stu-id="f1300-138">CAL\_HIJRI</span></span>

<span data-ttu-id="f1300-139">Hijri (Arabisch, Mond)</span><span class="sxs-lookup"><span data-stu-id="f1300-139">Hijri (Arabic Lunar)</span></span>

<span data-ttu-id="f1300-140">7</span><span class="sxs-lookup"><span data-stu-id="f1300-140">7</span></span>

<span data-ttu-id="f1300-141">Cal- \_ Thai</span><span class="sxs-lookup"><span data-stu-id="f1300-141">CAL\_THAI</span></span>

<span data-ttu-id="f1300-142">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="f1300-142">Thai</span></span>

<span data-ttu-id="f1300-143">8</span><span class="sxs-lookup"><span data-stu-id="f1300-143">8</span></span>

<span data-ttu-id="f1300-144">Cal- \_ Hebräisch</span><span class="sxs-lookup"><span data-stu-id="f1300-144">CAL\_HEBREW</span></span>

<span data-ttu-id="f1300-145">Hebräisch (Mond)</span><span class="sxs-lookup"><span data-stu-id="f1300-145">Hebrew (Lunar)</span></span>

<span data-ttu-id="f1300-146">9</span><span class="sxs-lookup"><span data-stu-id="f1300-146">9</span></span>

<span data-ttu-id="f1300-147">Cal \_ Gregorianisch ( \_ \_ Französisch)</span><span class="sxs-lookup"><span data-stu-id="f1300-147">CAL\_GREGORIAN\_ME\_FRENCH</span></span>

<span data-ttu-id="f1300-148">Gregorian Middle East French</span><span class="sxs-lookup"><span data-stu-id="f1300-148">Gregorian Middle East French</span></span>

<span data-ttu-id="f1300-149">10</span><span class="sxs-lookup"><span data-stu-id="f1300-149">10</span></span>

<span data-ttu-id="f1300-150">Cal \_ Gregorianisch, \_ Arabisch</span><span class="sxs-lookup"><span data-stu-id="f1300-150">CAL\_GREGORIAN\_ARABIC</span></span>

<span data-ttu-id="f1300-151">Gregorian Arabic</span><span class="sxs-lookup"><span data-stu-id="f1300-151">Gregorian Arabic</span></span>

<span data-ttu-id="f1300-152">11</span><span class="sxs-lookup"><span data-stu-id="f1300-152">11</span></span>

<span data-ttu-id="f1300-153">Cal \_ Gregorianisch (in \_ \_ englischer Sprache)</span><span class="sxs-lookup"><span data-stu-id="f1300-153">CAL\_GREGORIAN\_XLIT\_ENGLISH</span></span>

<span data-ttu-id="f1300-154">Gregorianisch, transliterierte Englisch</span><span class="sxs-lookup"><span data-stu-id="f1300-154">Gregorian transliterated English</span></span>

<span data-ttu-id="f1300-155">12</span><span class="sxs-lookup"><span data-stu-id="f1300-155">12</span></span>

<span data-ttu-id="f1300-156">Cal \_ Gregorianischen \_ xlit \_ Französisch</span><span class="sxs-lookup"><span data-stu-id="f1300-156">CAL\_GREGORIAN\_XLIT\_FRENCH</span></span>

<span data-ttu-id="f1300-157">Gregorianisches transliterierte Französisch</span><span class="sxs-lookup"><span data-stu-id="f1300-157">Gregorian transliterated French</span></span>

<span data-ttu-id="f1300-158">23</span><span class="sxs-lookup"><span data-stu-id="f1300-158">23</span></span>

<span data-ttu-id="f1300-159">Cal-über- \_ Qura</span><span class="sxs-lookup"><span data-stu-id="f1300-159">CAL\_UMALQURA</span></span>

<span data-ttu-id="f1300-160">**Windows Vista und höher:** Um Al Qura-Kalender (Arabisch Mond)</span><span class="sxs-lookup"><span data-stu-id="f1300-160">**Windows Vista and later:** Um Al Qura (Arabic lunar) calendar</span></span>



 

> [!Note]  
> <span data-ttu-id="f1300-161">Die Lücke bei der Nummerierung zwischen den Bezeichner Cal \_ Gregorianisch \_ xlit \_ Französisch und Cal-über- \_ Qura ist beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="f1300-161">The gap in numbering between the identifiers CAL\_GREGORIAN\_XLIT\_FRENCH and CAL\_UMALQURA is intentional.</span></span> <span data-ttu-id="f1300-162">Der Kenn Zeichner für Cal--über- \_ Qura ist 23, nicht 13.</span><span class="sxs-lookup"><span data-stu-id="f1300-162">The designator for CAL\_UMALQURA is 23, not 13.</span></span>

 

<span data-ttu-id="f1300-163">Außerdem erlauben [**enumcalendarinfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) und [**enumcalendarinfoex**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) die Verwendung des Werts \_ \_ Enumeration all Kalenders, um eine Enumeration aller anwendbaren Kalender anzufordern.</span><span class="sxs-lookup"><span data-stu-id="f1300-163">In addition, [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) and [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) allow the use of the value ENUM\_ALL\_CALENDARS to request an enumeration of all applicable calendars.</span></span>

<span data-ttu-id="f1300-164">Wert</span><span class="sxs-lookup"><span data-stu-id="f1300-164">Value</span></span>

<span data-ttu-id="f1300-165">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f1300-165">Meaning</span></span>

<span data-ttu-id="f1300-166">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="f1300-166">0xffffffff</span></span>

<span data-ttu-id="f1300-167">\_alle Kalender aufzählen \_</span><span class="sxs-lookup"><span data-stu-id="f1300-167">ENUM\_ALL\_CALENDARS</span></span>

<span data-ttu-id="f1300-168">Alle anwendbaren Kalender für das angegebene Gebiets Schema</span><span class="sxs-lookup"><span data-stu-id="f1300-168">All applicable calendars for the specified locale</span></span>



 

 

 
