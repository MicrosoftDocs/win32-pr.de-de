---
description: In diesem Thema werden die Calendar Type-Informationen (caltype-Datentyp) beschrieben, die in den Funktionen enumcalendarinfo, enumcalendarinfoex, enumcalendarinfoexex, getcalendarinfo und getcalendarinfoex verwendet werden.
ms.assetid: 33361a97-0f27-477a-a0ee-3d4d3aaeaacf
title: Kalendertyp Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a8e334a1b05f372f51c81ab8158294d46eebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867947"
---
# <a name="calendar-type-information"></a><span data-ttu-id="7e8fd-103">Kalendertyp Informationen</span><span class="sxs-lookup"><span data-stu-id="7e8fd-103">Calendar Type Information</span></span>

<span data-ttu-id="7e8fd-104">In diesem Thema werden die Calendar Type-Informationen (caltype-Datentyp) beschrieben, die in den Funktionen [**enumcalendarinfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**enumcalendarinfoex**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**enumcalendarinfoexex**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**getcalendarinfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)und [**getcalendarinfoex**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-104">This topic describes the calendar type information (CALTYPE data type) used in the [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa), and [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) functions.</span></span> <span data-ttu-id="7e8fd-105">Einige dieser Werte werden auch von der [**setcalendarinfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-105">Some of these values are also used by the [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) function.</span></span>

<span data-ttu-id="7e8fd-106">Die folgenden caltype-Konstanten können in Kombination mit allen anderen caltype-Konstanten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-106">The following CALTYPE constants can be used in combination with any other CALTYPE constants.</span></span>



| <span data-ttu-id="7e8fd-107">Konstante</span><span class="sxs-lookup"><span data-stu-id="7e8fd-107">Constant</span></span>                     | <span data-ttu-id="7e8fd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e8fd-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e8fd-109">Cal \_ nouseroverride</span><span class="sxs-lookup"><span data-stu-id="7e8fd-109">CAL\_NOUSEROVERRIDE</span></span>          | <span data-ttu-id="7e8fd-110">**Windows Me/98, Windows 2000:** Verwenden Sie den Standardwert des Systems anstelle der Auswahl des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-110">**Windows Me/98, Windows 2000:** Use the system default instead of the user's choice.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="7e8fd-111">Cal- \_ Rückgabe \_ \_ Namen</span><span class="sxs-lookup"><span data-stu-id="7e8fd-111">CAL\_RETURN\_GENITIVE\_NAMES</span></span> | <span data-ttu-id="7e8fd-112">**Windows 7 und höher:** Rufen Sie das Ergebnis von [**getcalendarinfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) in Form von Namen von Monaten ab, bei denen es sich um die Namen handelt, die verwendet werden, wenn die Monatsnamen mit anderen Elementen kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-112">**Windows 7 and later:** Retrieve the result from [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) in the form of genitive names of months, which are the names used when the month names are combined with other items.</span></span> <span data-ttu-id="7e8fd-113">Beispielsweise wird in Ukrainisch die Entsprechung von Januar in den Namen "" geschrieben, wenn der Monat allein benannt wird.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-113">For example, in Ukrainian the equivalent of January is written "Січень" when the month is named alone.</span></span> <span data-ttu-id="7e8fd-114">Wenn jedoch der Monats Name in Kombination verwendet wird, z. b. in einem Datum wie dem 5. Januar 2003, wird das Format des Namens verwendet.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-114">However, when the month name is used in combination, for example, in a date such as January 5th, 2003, the genitive form of the name is used.</span></span> <span data-ttu-id="7e8fd-115">Im Beispiel "Ukrainisch" wird der Name des "Genitive Month" als "2003 5.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-115">For the Ukrainian example, the genitive month name is displayed as "5 січня 2003".</span></span> <span data-ttu-id="7e8fd-116">Weitere Informationen finden Sie unter [locale \_ Return \_ Genitive \_ Names](locale-return-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7e8fd-116">For more information, see [LOCALE\_RETURN\_GENITIVE\_NAMES](locale-return-constants.md).</span></span> |
| <span data-ttu-id="7e8fd-117">Cal- \_ Rückgabe \_ Nummer</span><span class="sxs-lookup"><span data-stu-id="7e8fd-117">CAL\_RETURN\_NUMBER</span></span>          | <span data-ttu-id="7e8fd-118">**Windows Me/98, Windows 2000:** Rufen Sie das Ergebnis von [**getcalendarinfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) als Zahl anstelle einer Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-118">**Windows Me/98, Windows 2000:** Retrieve the result from [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) as a number instead of a string.</span></span> <span data-ttu-id="7e8fd-119">Dies gilt nur für Werte, die mit Cal \_ I beginnen.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-119">This is only valid for values beginning with CAL\_I.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="7e8fd-120">Cal \_ -Verwendung von \_ CP \_ ACP</span><span class="sxs-lookup"><span data-stu-id="7e8fd-120">CAL\_USE\_CP\_ACP</span></span>            | <span data-ttu-id="7e8fd-121">**Windows Me/98, Windows 2000:** Verwenden Sie die ANSI-Codepage (ACP) des Systems anstelle der Gebiets Schema-Codepage für die Zeichen folgen Übersetzung.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-121">**Windows Me/98, Windows 2000:** Use the system ANSI code page (ACP) instead of the locale code page for string translation.</span></span> <span data-ttu-id="7e8fd-122">Dies ist nur für ANSI-Versionen von Funktionen relevant, z. b. **enumcalendarinfoa**.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-122">This is only relevant for ANSI versions of functions, for example, **EnumCalendarInfoA**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="7e8fd-123">Die folgenden caltype-Konstanten schließen sich gegenseitig aus und können in einem Funktions aufrufnicht in Kombination miteinander verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-123">The following CALTYPE constants are mutually exclusive and cannot be used in combination with each other in a function call.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7e8fd-124">Konstante</span><span class="sxs-lookup"><span data-stu-id="7e8fd-124">Constant</span></span></th>
<th><span data-ttu-id="7e8fd-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e8fd-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e8fd-126">CAL_ICALINTVALUE</span><span class="sxs-lookup"><span data-stu-id="7e8fd-126">CAL_ICALINTVALUE</span></span></td>
<td><span data-ttu-id="7e8fd-127">Ein ganzzahliger Wert, der den Kalendertyp des alternativen Kalenders angibt.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-127">An integer value indicating the calendar type of the alternate calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-128">CAL_ITWODIGITYEARMAX</span><span class="sxs-lookup"><span data-stu-id="7e8fd-128">CAL_ITWODIGITYEARMAX</span></span></td>
<td><span data-ttu-id="7e8fd-129"><strong>Windows Me/98, Windows 2000:</strong> Ein ganzzahliger Wert, der die obere Grenze des zweistelligen Jahres Bereichs angibt.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-129"><strong>Windows Me/98, Windows 2000:</strong> An integer value indicating the upper boundary of the two-digit year range.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-130">CAL_IYEAROFFSETRANGE</span><span class="sxs-lookup"><span data-stu-id="7e8fd-130">CAL_IYEAROFFSETRANGE</span></span></td>
<td><span data-ttu-id="7e8fd-131">Mindestens eine NULL-terminierte Zeichenfolge, die die Jahres Offsets für die einzelnen Zeitraum Bereiche angibt.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-131">One or more null-terminated strings that specify the year offsets for each of the era ranges.</span></span> <span data-ttu-id="7e8fd-132">Die letzte Zeichenfolge weist ein zusätzliches abschließendes NULL-Zeichen auf.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-132">The last string has an extra terminating null character.</span></span> <span data-ttu-id="7e8fd-133">Dieser Wert variiert je nach Typ des optionalen Kalenders im Format.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-133">This value varies in format depending on the type of optional calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-134">CAL_SABBREVDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="7e8fd-134">CAL_SABBREVDAYNAME1</span></span></td>
<td><span data-ttu-id="7e8fd-135">Abgekürzte System eigener Name des ersten Tags der Woche.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-135">Abbreviated native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-136">CAL_SABBREVDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="7e8fd-136">CAL_SABBREVDAYNAME2</span></span></td>
<td><span data-ttu-id="7e8fd-137">Abgekürzte System eigener Name des zweiten Tags der Woche.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-137">Abbreviated native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-138">CAL_SABBREVDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="7e8fd-138">CAL_SABBREVDAYNAME3</span></span></td>
<td><span data-ttu-id="7e8fd-139">Abgekürzte System eigener Name des dritten wochentags.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-139">Abbreviated native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-140">CAL_SABBREVDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="7e8fd-140">CAL_SABBREVDAYNAME4</span></span></td>
<td><span data-ttu-id="7e8fd-141">Abgekürzte Name des vierten Tags der Woche.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-141">Abbreviated native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-142">CAL_SABBREVDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="7e8fd-142">CAL_SABBREVDAYNAME5</span></span></td>
<td><span data-ttu-id="7e8fd-143">Abgekürzte System eigener Name des fünften wochentags.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-143">Abbreviated native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-144">CAL_SABBREVDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="7e8fd-144">CAL_SABBREVDAYNAME6</span></span></td>
<td><span data-ttu-id="7e8fd-145">Abgekürzte System eigener Name des sechsten wochentags.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-145">Abbreviated native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-146">CAL_SABBREVDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="7e8fd-146">CAL_SABBREVDAYNAME7</span></span></td>
<td><span data-ttu-id="7e8fd-147">Abgekürzte System eigener Name des siebten wochentags.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-147">Abbreviated native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-148">CAL_SABBREVERASTRING</span><span class="sxs-lookup"><span data-stu-id="7e8fd-148">CAL_SABBREVERASTRING</span></span></td>
<td><span data-ttu-id="7e8fd-149"><strong>Windows 7 und höher:</strong> Abgekürzte nativer Name eines Zeitraums.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-149"><strong>Windows 7 and later:</strong> Abbreviated native name of an era.</span></span> <span data-ttu-id="7e8fd-150">Der vollständige Zeitraum wird durch die CAL_SERASTRING Konstante dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-150">The full era is represented by the CAL_SERASTRING constant.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-151">CAL_SABBREVMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="7e8fd-151">CAL_SABBREVMONTHNAME1</span></span></td>
<td><span data-ttu-id="7e8fd-152">Der systemeigene Name des ersten Monats des Jahres wurde abgekürzt.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-152">Abbreviated native name of the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-153">CAL_SABBREVMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="7e8fd-153">CAL_SABBREVMONTHNAME2</span></span></td>
<td><span data-ttu-id="7e8fd-154">Abgekürzte System eigener Name des zweiten Monats des Jahres.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-154">Abbreviated native name of the second month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-155">CAL_SABBREVMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="7e8fd-155">CAL_SABBREVMONTHNAME3</span></span></td>
<td><span data-ttu-id="7e8fd-156">Der systemeigene Name des dritten Monats des Jahres wurde abgekürzt.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-156">Abbreviated native name of the third month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-157">CAL_SABBREVMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="7e8fd-157">CAL_SABBREVMONTHNAME4</span></span></td>
<td><span data-ttu-id="7e8fd-158">Abgekürzte nativer Name des vierten Monats des Jahres.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-158">Abbreviated native name of the fourth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-159">CAL_SABBREVMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="7e8fd-159">CAL_SABBREVMONTHNAME5</span></span></td>
<td><span data-ttu-id="7e8fd-160">Abgekürzte nativer Name des fünften Monats des Jahres.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-160">Abbreviated native name of the fifth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-161">CAL_SABBREVMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="7e8fd-161">CAL_SABBREVMONTHNAME6</span></span></td>
<td><span data-ttu-id="7e8fd-162">Der systemeigene Name des sechsten Monats des Jahres wurde abgekürzt.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-162">Abbreviated native name of the sixth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-163">CAL_SABBREVMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="7e8fd-163">CAL_SABBREVMONTHNAME7</span></span></td>
<td><span data-ttu-id="7e8fd-164">Der systemeigene Name des siebten Monats des Jahres wurde abgekürzt.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-164">Abbreviated native name of the seventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-165">CAL_SABBREVMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="7e8fd-165">CAL_SABBREVMONTHNAME8</span></span></td>
<td><span data-ttu-id="7e8fd-166">Abgekürzte nativer Name des achten Monats des Jahres.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-166">Abbreviated native name of the eighth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-167">CAL_SABBREVMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="7e8fd-167">CAL_SABBREVMONTHNAME9</span></span></td>
<td><span data-ttu-id="7e8fd-168">Der systemeigene Name des neunten Monats des Jahres wurde abgekürzt.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-168">Abbreviated native name of the ninth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-169">CAL_SABBREVMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="7e8fd-169">CAL_SABBREVMONTHNAME10</span></span></td>
<td><span data-ttu-id="7e8fd-170">Der systemeigene Name des zehnten Monats des Jahres wurde abgekürzt.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-170">Abbreviated native name of the tenth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-171">CAL_SABBREVMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="7e8fd-171">CAL_SABBREVMONTHNAME11</span></span></td>
<td><span data-ttu-id="7e8fd-172">Der systemeigene Name des elften Monats des Jahres wurde abgekürzt.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-172">Abbreviated native name of the eleventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-173">CAL_SABBREVMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="7e8fd-173">CAL_SABBREVMONTHNAME12</span></span></td>
<td><span data-ttu-id="7e8fd-174">Der systemeigene Name des zwölften Monats des Jahres wurde abgekürzt.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-174">Abbreviated native name of the twelfth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-175">CAL_SABBREVMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="7e8fd-175">CAL_SABBREVMONTHNAME13</span></span></td>
<td><span data-ttu-id="7e8fd-176">Der systemeigene Name des dreizehnten Monats des Jahres, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-176">Abbreviated native name of the thirteenth month of the year, if it exists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-177">CAL_SCALNAME</span><span class="sxs-lookup"><span data-stu-id="7e8fd-177">CAL_SCALNAME</span></span></td>
<td><span data-ttu-id="7e8fd-178">Der Native Name des alternativen Kalenders.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-178">Native name of the alternate calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-179">CAL_SDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="7e8fd-179">CAL_SDAYNAME1</span></span></td>
<td><span data-ttu-id="7e8fd-180">Der Native Name des ersten Tags der Woche.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-180">Native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-181">CAL_SDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="7e8fd-181">CAL_SDAYNAME2</span></span></td>
<td><span data-ttu-id="7e8fd-182">Der Native Name des zweiten Tags der Woche.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-182">Native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-183">CAL_SDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="7e8fd-183">CAL_SDAYNAME3</span></span></td>
<td><span data-ttu-id="7e8fd-184">Der Native Name des dritten wochentags.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-184">Native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-185">CAL_SDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="7e8fd-185">CAL_SDAYNAME4</span></span></td>
<td><span data-ttu-id="7e8fd-186">Der Native Name des vierten Tags der Woche.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-186">Native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-187">CAL_SDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="7e8fd-187">CAL_SDAYNAME5</span></span></td>
<td><span data-ttu-id="7e8fd-188">Der Native Name des fünften wochentags.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-188">Native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-189">CAL_SDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="7e8fd-189">CAL_SDAYNAME6</span></span></td>
<td><span data-ttu-id="7e8fd-190">Der systemeigene Name des sechsten wochentags.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-190">Native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-191">CAL_SDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="7e8fd-191">CAL_SDAYNAME7</span></span></td>
<td><span data-ttu-id="7e8fd-192">Der Native Name des siebten wochentags.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-192">Native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-193">CAL_SERASTRING</span><span class="sxs-lookup"><span data-stu-id="7e8fd-193">CAL_SERASTRING</span></span></td>
<td><span data-ttu-id="7e8fd-194">Mindestens eine NULL-terminierte Zeichenfolge, die jeden der Unicode-Code Punkte angibt, die den mit CAL_IYEAROFFSETRANGE verknüpften Zeitraum angeben.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-194">One or more null-terminated strings that specify each of the Unicode code points specifying the era associated with CAL_IYEAROFFSETRANGE.</span></span> <span data-ttu-id="7e8fd-195">Die letzte Zeichenfolge weist ein zusätzliches abschließendes NULL-Zeichen auf.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-195">The last string has an extra terminating null character.</span></span> <span data-ttu-id="7e8fd-196">Dieser Wert variiert je nach Typ des optionalen Kalenders im Format.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-196">This value varies in format depending on the type of optional calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-197">CAL_SLONGDATE</span><span class="sxs-lookup"><span data-stu-id="7e8fd-197">CAL_SLONGDATE</span></span></td>
<td><span data-ttu-id="7e8fd-198">Lange Datumsformate für den Kalendertyp.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-198">Long date formats for the calendar type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-199">CAL_SMONTHDAY</span><span class="sxs-lookup"><span data-stu-id="7e8fd-199">CAL_SMONTHDAY</span></span></td>
<td><span data-ttu-id="7e8fd-200"><strong>Windows 7 und höher:</strong> Format von Monat und Tag für den Kalendertyp.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-200"><strong>Windows 7 and later:</strong> Format of the month and day for the calendar type.</span></span> <span data-ttu-id="7e8fd-201">Die Formatierung ähnelt der für CAL_SLONGDATE.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-201">The formatting is similar to that for CAL_SLONGDATE.</span></span> <span data-ttu-id="7e8fd-202">Wenn z. b. das Muster Month/Day der vollständige Monats Name ist, gefolgt von der Tagesnummer mit führenden Nullen (z &quot; . b. September 03), &quot; ist das Format &quot; MMMM dd &quot; .</span><span class="sxs-lookup"><span data-stu-id="7e8fd-202">For example, if the Month/Day pattern is the full month name followed by the day number with leading zeros, for example, &quot;September 03&quot;, the format is &quot;MMMM dd&quot;.</span></span> <span data-ttu-id="7e8fd-203">Einfache Anführungszeichen können verwendet werden, um nicht formatierte Zeichen (z. b. "de") in Spanisch einzufügen.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-203">Single quotation marks can be used to insert non-format characters, for example, 'de' in Spanish.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7e8fd-204">Dieser Kalendertyp unterstützt nur ein Format.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-204">This calendar type supports only one format.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-205">CAL_SMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="7e8fd-205">CAL_SMONTHNAME1</span></span></td>
<td><span data-ttu-id="7e8fd-206">Der Native Name des ersten Monats des Jahres.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-206">Native name of the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-207">CAL_SMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="7e8fd-207">CAL_SMONTHNAME2</span></span></td>
<td><span data-ttu-id="7e8fd-208">Der Native Name des zweiten Monats des Jahres.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-208">Native name of the second month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-209">CAL_SMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="7e8fd-209">CAL_SMONTHNAME3</span></span></td>
<td><span data-ttu-id="7e8fd-210">Der Native Name des dritten Monats des Jahres.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-210">Native name of the third month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-211">CAL_SMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="7e8fd-211">CAL_SMONTHNAME4</span></span></td>
<td><span data-ttu-id="7e8fd-212">Der Native Name des vierten Monats des Jahres.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-212">Native name of the fourth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-213">CAL_SMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="7e8fd-213">CAL_SMONTHNAME5</span></span></td>
<td><span data-ttu-id="7e8fd-214">Der Native Name des fünften Monats des Jahres.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-214">Native name of the fifth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-215">CAL_SMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="7e8fd-215">CAL_SMONTHNAME6</span></span></td>
<td><span data-ttu-id="7e8fd-216">Der Native Name des sechsten Monats des Jahres.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-216">Native name of the sixth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-217">CAL_SMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="7e8fd-217">CAL_SMONTHNAME7</span></span></td>
<td><span data-ttu-id="7e8fd-218">Der Native Name des siebten Monats des Jahres.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-218">Native name of the seventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-219">CAL_SMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="7e8fd-219">CAL_SMONTHNAME8</span></span></td>
<td><span data-ttu-id="7e8fd-220">Der Native Name des achten Monats des Jahres.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-220">Native name of the eighth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-221">CAL_SMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="7e8fd-221">CAL_SMONTHNAME9</span></span></td>
<td><span data-ttu-id="7e8fd-222">Der Native Name des neunten Monats des Jahres.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-222">Native name of the ninth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-223">CAL_SMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="7e8fd-223">CAL_SMONTHNAME10</span></span></td>
<td><span data-ttu-id="7e8fd-224">Der Native Name des zehnten Monats des Jahres.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-224">Native name of the tenth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-225">CAL_SMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="7e8fd-225">CAL_SMONTHNAME11</span></span></td>
<td><span data-ttu-id="7e8fd-226">Der Native Name des elften Monats des Jahres.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-226">Native name of the eleventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-227">CAL_SMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="7e8fd-227">CAL_SMONTHNAME12</span></span></td>
<td><span data-ttu-id="7e8fd-228">Der Native Name des zwölften Monats des Jahres.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-228">Native name of the twelfth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-229">CAL_SMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="7e8fd-229">CAL_SMONTHNAME13</span></span></td>
<td><span data-ttu-id="7e8fd-230">Der Native Name des dreizehnten Monats des Jahres, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-230">Native name of the thirteenth month of the year, if it exists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-231">CAL_SSHORTDATE</span><span class="sxs-lookup"><span data-stu-id="7e8fd-231">CAL_SSHORTDATE</span></span></td>
<td><span data-ttu-id="7e8fd-232">Kurze Datumsformate für den Kalendertyp.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-232">Short date formats for the calendar type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-233">CAL_SSHORTESTDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="7e8fd-233">CAL_SSHORTESTDAYNAME1</span></span></td>
<td><span data-ttu-id="7e8fd-234"><strong>Windows Vista und höher:</strong> Kurzer nativer Name des ersten Tags der Woche.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-234"><strong>Windows Vista and later:</strong> Short native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-235">CAL_SSHORTESTDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="7e8fd-235">CAL_SSHORTESTDAYNAME2</span></span></td>
<td><span data-ttu-id="7e8fd-236"><strong>Windows Vista und höher:</strong> Kurzer nativer Name des zweiten Tags der Woche.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-236"><strong>Windows Vista and later:</strong> Short native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-237">CAL_SSHORTESTDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="7e8fd-237">CAL_SSHORTESTDAYNAME3</span></span></td>
<td><span data-ttu-id="7e8fd-238"><strong>Windows Vista und höher:</strong> Kurzer nativer Name des dritten wochentags.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-238"><strong>Windows Vista and later:</strong> Short native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-239">CAL_SSHORTESTDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="7e8fd-239">CAL_SSHORTESTDAYNAME4</span></span></td>
<td><span data-ttu-id="7e8fd-240"><strong>Windows Vista und höher:</strong> Kurzer nativer Name des vierten Tags der Woche.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-240"><strong>Windows Vista and later:</strong> Short native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-241">CAL_SSHORTESTDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="7e8fd-241">CAL_SSHORTESTDAYNAME5</span></span></td>
<td><span data-ttu-id="7e8fd-242"><strong>Windows Vista und höher:</strong> Kurzer nativer Name des fünften wochentags.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-242"><strong>Windows Vista and later:</strong> Short native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-243">CAL_SSHORTESTDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="7e8fd-243">CAL_SSHORTESTDAYNAME6</span></span></td>
<td><span data-ttu-id="7e8fd-244"><strong>Windows Vista und höher:</strong> Kurzer nativer Name des sechsten wochentags.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-244"><strong>Windows Vista and later:</strong> Short native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8fd-245">CAL_SSHORTESTDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="7e8fd-245">CAL_SSHORTESTDAYNAME7</span></span></td>
<td><span data-ttu-id="7e8fd-246"><strong>Windows Vista und höher:</strong> Kurzer nativer Name des siebten wochentags.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-246"><strong>Windows Vista and later:</strong> Short native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8fd-247">CAL_SYEARMONTH</span><span class="sxs-lookup"><span data-stu-id="7e8fd-247">CAL_SYEARMONTH</span></span></td>
<td><span data-ttu-id="7e8fd-248"><strong>Windows Me/98, Windows 2000:</strong> Das Jahr/Monat-Format für die angegebenen Kalender.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-248"><strong>Windows Me/98, Windows 2000:</strong> The year/month formats for the specified calendars.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="7e8fd-249">Wenn der Native Name des Wochentags oder eines Monats eine leere Zeichenfolge ist, ist dieser Name mit dem in den entsprechenden Gebiets Schema Informationen angegebenen Namen identisch und wird daher hier nicht dupliziert.</span><span class="sxs-lookup"><span data-stu-id="7e8fd-249">If the native name for the day of the week or for a month is an empty string, that name is identical to the name specified in the corresponding locale information and therefore is not duplicated here.</span></span>

 

 

 




