---
description: Das-Objekt von "Swap DateTime" ist ein Hilfsobjekt zum Analysieren und Festlegen von Common Information Model (CIM)-DateTime-Werten.
ms.assetid: 3dd34c73-3c2b-4d59-827b-169cf8020213
ms.tgt_platform: multiple
title: Taubemdatetime-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime
- ISWbemDateTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 65f3f9836b52693e3f74bac5cfd94553e02d7bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348061"
---
# <a name="swbemdatetime-object"></a><span data-ttu-id="9628c-103">Taubemdatetime-Objekt</span><span class="sxs-lookup"><span data-stu-id="9628c-103">SWbemDateTime object</span></span>

<span data-ttu-id="9628c-104">Das-Objekt von " **Swap DateTime** " ist ein Hilfsobjekt zum Analysieren und Festlegen von Common Information Model (CIM)- [DateTime](datetime.md) -Werten.</span><span class="sxs-lookup"><span data-stu-id="9628c-104">The **SWbemDateTime** object is a helper object to parse and set Common Information Model (CIM) [datetime](datetime.md) values.</span></span> <span data-ttu-id="9628c-105">Sie spielt eine Rolle ähnlich der von " [**errbemubjectpath**](swbemobjectpath.md)", die Unterstützung für das Formatieren und Interpretieren von Objekt Pfaden bietet.</span><span class="sxs-lookup"><span data-stu-id="9628c-105">It plays a role similar to [**SWbemObjectPath**](swbemobjectpath.md), which provides assistance to format and interpret object paths.</span></span> <span data-ttu-id="9628c-106">Sie können den VBScript-Aufruf von " [comateobject](/previous-versions//xzysf6hc(v=vs.85)) " verwenden, um das Objekt " **Swap DateTime** " zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9628c-106">You can use the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call to create the **SWbemDateTime** object.</span></span>

<span data-ttu-id="9628c-107">Ein " **slibemdatetime** "-Objekt kann mithilfe von Methoden für das-Objekt aus den Werten " **VT \_ Date** " oder " **FILETIME** " initialisiert und formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="9628c-107">An **SWbemDateTime** object can be initialized from and formatted in either **VT\_DATE** or **FILETIME** values using methods on the object.</span></span> <span data-ttu-id="9628c-108">Mithilfe der Eigenschaften des-Objekts kann der Wert in die Komponenten Jahr, Monat, Tag, Stunde, Minuten, Sekunden oder Mikrosekunden analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="9628c-108">Using properties of the object, the value can be parsed into component year, month, day, hour, minutes, seconds, or microseconds.</span></span> <span data-ttu-id="9628c-109">Das Objekt " **taubemdatetime** " kann entweder in lokale oder koordinierte Weltzeit (UTC)-Werte formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="9628c-109">The **SWbemDateTime** object can be formatted into either local or Coordinated Universal Time (UTC) values.</span></span> <span data-ttu-id="9628c-110">Weitere Informationen finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="9628c-110">For more information, see [Date and Time Format](date-and-time-format.md).</span></span>

<span data-ttu-id="9628c-111">' **Swap DateTime** ' ist das einzige Windows-Verwaltungsinstrumentation (WMI)-Skript Objekt, das für die Initialisierung und Skripts, die auf HTML-Seiten in Internet Explorer ausgeführt werden, als sicher gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="9628c-111">**SWbemDateTime** is the only Windows Management Instrumentation (WMI) scripting object that is marked safe for initialization and scripts running on HTML pages in Internet Explorer.</span></span>

## <a name="members"></a><span data-ttu-id="9628c-112">Member</span><span class="sxs-lookup"><span data-stu-id="9628c-112">Members</span></span>

<span data-ttu-id="9628c-113">Das Objekt " **waybemdatetime** " enthält diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9628c-113">The **SWbemDateTime** object has these types of members:</span></span>

-   [<span data-ttu-id="9628c-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="9628c-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="9628c-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9628c-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9628c-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="9628c-116">Methods</span></span>

<span data-ttu-id="9628c-117">Das Objekt " **Swap DateTime** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="9628c-117">The **SWbemDateTime** object has these methods.</span></span>



| <span data-ttu-id="9628c-118">Methode</span><span class="sxs-lookup"><span data-stu-id="9628c-118">Method</span></span>                                           | <span data-ttu-id="9628c-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9628c-119">Description</span></span>                                                                                                          |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9628c-120">**' GetFileTime '**</span><span class="sxs-lookup"><span data-stu-id="9628c-120">**GetFileTime**</span></span>](swbemdatetime-getfiletime.md) | <span data-ttu-id="9628c-121">Konvertiert ein Datum und eine Uhrzeit der **FILETIME** , ausgedrückt als **BSTR**, in ein WMI- [DateTime](datetime.md) -Format.</span><span class="sxs-lookup"><span data-stu-id="9628c-121">Converts a **FILETIME** date and time, expressed as a **BSTR**, to a WMI [DATETIME](datetime.md) format.</span></span><br/> |
| [<span data-ttu-id="9628c-122">**GetVarDate**</span><span class="sxs-lookup"><span data-stu-id="9628c-122">**GetVarDate**</span></span>](swbemdatetime-getvardate.md)   | <span data-ttu-id="9628c-123">Konvertiert einen Datums-und Uhrzeitwert für ein WMI- [DateTime-Format](datetime.md) in ein **VT- \_ Datum**.</span><span class="sxs-lookup"><span data-stu-id="9628c-123">Converts a WMI [DATETIME](datetime.md) formatted date and time value to a **VT\_DATE**.</span></span><br/>                  |
| [<span data-ttu-id="9628c-124">**SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="9628c-124">**SetFileTime**</span></span>](swbemdatetime-setfiletime.md) | <span data-ttu-id="9628c-125">Konvertiert ein WMI- [DateTime](datetime.md) -Format in ein Datum und eine Uhrzeit der **FILETIME** , ausgedrückt als **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="9628c-125">Converts a WMI [DATETIME](datetime.md) format to a **FILETIME** date and time, expressed as a **BSTR**.</span></span><br/>  |
| [<span data-ttu-id="9628c-126">**SetVarDate**</span><span class="sxs-lookup"><span data-stu-id="9628c-126">**SetVarDate**</span></span>](swbemdatetime-setvardate.md)   | <span data-ttu-id="9628c-127">Konvertiert ein Datum und eine Uhrzeit im Format " **VT \_ Date** " in einen WMI- [DateTime](datetime.md)-Wert.</span><span class="sxs-lookup"><span data-stu-id="9628c-127">Converts a **VT\_DATE** formatted date and time to a WMI [DATETIME](datetime.md).</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="9628c-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9628c-128">Properties</span></span>

<span data-ttu-id="9628c-129">Das Objekt " **Swap DateTime** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9628c-129">The **SWbemDateTime** object has these properties.</span></span>



| <span data-ttu-id="9628c-130">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9628c-130">Property</span></span>                                                                        | <span data-ttu-id="9628c-131">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="9628c-131">Access type</span></span>           | <span data-ttu-id="9628c-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9628c-132">Description</span></span>                                                                                                                     |
|:--------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9628c-133">**Tag**</span><span class="sxs-lookup"><span data-stu-id="9628c-133">**Day**</span></span>](swbemdatetime-day.md)<br/>                                     | <span data-ttu-id="9628c-134">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9628c-134">Read/write</span></span><br/> | <span data-ttu-id="9628c-135">Die Tages Komponente eines CIM- [DateTime](datetime.md) -Werts.</span><span class="sxs-lookup"><span data-stu-id="9628c-135">The day component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                           |
| [<span data-ttu-id="9628c-136">**Dayangegeben**</span><span class="sxs-lookup"><span data-stu-id="9628c-136">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)<br/>                   | <span data-ttu-id="9628c-137">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9628c-137">Read/write</span></span><br/> | <span data-ttu-id="9628c-138">Gibt an, ob der Tag angegeben oder als Platzhalter belassen wird.</span><span class="sxs-lookup"><span data-stu-id="9628c-138">Indicates whether the day is specified or left as a wildcard.</span></span><br/>                                                        |
| [<span data-ttu-id="9628c-139">**Stunden**</span><span class="sxs-lookup"><span data-stu-id="9628c-139">**Hours**</span></span>](swbemdatetime-hours.md)<br/>                                 | <span data-ttu-id="9628c-140">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9628c-140">Read/write</span></span><br/> | <span data-ttu-id="9628c-141">Die Stunden der Tages Komponente eines CIM- [DateTime](datetime.md) -Werts.</span><span class="sxs-lookup"><span data-stu-id="9628c-141">The hours of the day component of a CIM [datetime](datetime.md) value.</span></span><br/>                                              |
| [<span data-ttu-id="9628c-142">**Sansangegeben**</span><span class="sxs-lookup"><span data-stu-id="9628c-142">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)<br/>               | <span data-ttu-id="9628c-143">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9628c-143">Read/write</span></span><br/> | <span data-ttu-id="9628c-144">Gibt an, ob die Stunde angegeben oder als Platzhalter belassen wird.</span><span class="sxs-lookup"><span data-stu-id="9628c-144">Indicates whether the hour is specified or left as a wildcard.</span></span><br/>                                                       |
| [<span data-ttu-id="9628c-145">**Isinterval**</span><span class="sxs-lookup"><span data-stu-id="9628c-145">**IsInterval**</span></span>](swbemdatetime-isinterval.md)<br/>                       | <span data-ttu-id="9628c-146">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9628c-146">Read/write</span></span><br/> | <span data-ttu-id="9628c-147">Gibt an, dass mindestens eine Komponente von CIM [DateTime](datetime.md) ein Intervall und kein Datum darstellt.</span><span class="sxs-lookup"><span data-stu-id="9628c-147">Indicates that at least one component of the CIM [datetime](datetime.md) represents an interval rather than a date.</span></span><br/> |
| [<span data-ttu-id="9628c-148">**Mikrosekunden**</span><span class="sxs-lookup"><span data-stu-id="9628c-148">**Microseconds**</span></span>](swbemdatetime-microseconds.md)<br/>                   | <span data-ttu-id="9628c-149">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9628c-149">Read/write</span></span><br/> | <span data-ttu-id="9628c-150">Die Mikrosekunden Komponente eines CIM- [DateTime](datetime.md) -Werts.</span><span class="sxs-lookup"><span data-stu-id="9628c-150">The microseconds component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                  |
| [<span data-ttu-id="9628c-151">**' Mikroseconds' angegeben**</span><span class="sxs-lookup"><span data-stu-id="9628c-151">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)<br/> | <span data-ttu-id="9628c-152">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9628c-152">Read/write</span></span><br/> | <span data-ttu-id="9628c-153">Gibt an, ob die Mikrosekunden Komponente angegeben oder als Platzhalter belassen wird.</span><span class="sxs-lookup"><span data-stu-id="9628c-153">Indicates whether the microseconds component is specified or left as a wildcard.</span></span><br/>                                     |
| [<span data-ttu-id="9628c-154">**Minuten**</span><span class="sxs-lookup"><span data-stu-id="9628c-154">**Minutes**</span></span>](swbemdatetime-minutes.md)<br/>                             | <span data-ttu-id="9628c-155">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9628c-155">Read/write</span></span><br/> | <span data-ttu-id="9628c-156">Die Minuten Komponente eines CIM- [DateTime](datetime.md) -Werts.</span><span class="sxs-lookup"><span data-stu-id="9628c-156">The minutes component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                       |
| [<span data-ttu-id="9628c-157">**Minutesangegeben**</span><span class="sxs-lookup"><span data-stu-id="9628c-157">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)<br/>           | <span data-ttu-id="9628c-158">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9628c-158">Read/write</span></span><br/> | <span data-ttu-id="9628c-159">Gibt an, ob die Minuten Komponente angegeben oder als Platzhalter belassen wird.</span><span class="sxs-lookup"><span data-stu-id="9628c-159">Indicates whether the minutes component is specified or left as a wildcard.</span></span><br/>                                          |
| [<span data-ttu-id="9628c-160">**Ges**</span><span class="sxs-lookup"><span data-stu-id="9628c-160">**Month**</span></span>](swbemdatetime-month.md)<br/>                                 | <span data-ttu-id="9628c-161">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9628c-161">Read/write</span></span><br/> | <span data-ttu-id="9628c-162">Die Monats Komponente eines CIM- [DateTime](datetime.md) -Werts.</span><span class="sxs-lookup"><span data-stu-id="9628c-162">The month component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                         |
| [<span data-ttu-id="9628c-163">**Monthspezifiziert**</span><span class="sxs-lookup"><span data-stu-id="9628c-163">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)<br/>               | <span data-ttu-id="9628c-164">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9628c-164">Read/write</span></span><br/> | <span data-ttu-id="9628c-165">Gibt an, ob der Monat angegeben oder als Platzhalter belassen wird.</span><span class="sxs-lookup"><span data-stu-id="9628c-165">Indicates whether the month is specified or left as a wildcard.</span></span><br/>                                                      |
| [<span data-ttu-id="9628c-166">**Sekunden**</span><span class="sxs-lookup"><span data-stu-id="9628c-166">**Seconds**</span></span>](swbemdatetime-seconds.md)<br/>                             | <span data-ttu-id="9628c-167">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9628c-167">Read/write</span></span><br/> | <span data-ttu-id="9628c-168">Die Sekunden Komponente eines CIM- [DateTime](datetime.md) -Werts.</span><span class="sxs-lookup"><span data-stu-id="9628c-168">The seconds component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                       |
| [<span data-ttu-id="9628c-169">**Secondsspezifiziert**</span><span class="sxs-lookup"><span data-stu-id="9628c-169">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)<br/>           | <span data-ttu-id="9628c-170">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9628c-170">Read/write</span></span><br/> | <span data-ttu-id="9628c-171">Gibt an, ob die Sekunden Komponente angegeben oder als Platzhalter belassen wird.</span><span class="sxs-lookup"><span data-stu-id="9628c-171">Indicates whether the seconds component is specified or left as a wildcard.</span></span><br/>                                          |
| [<span data-ttu-id="9628c-172">**UTC**</span><span class="sxs-lookup"><span data-stu-id="9628c-172">**UTC**</span></span>](swbemdatetime-utc.md)<br/>                                     | <span data-ttu-id="9628c-173">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9628c-173">Read/write</span></span><br/> | <span data-ttu-id="9628c-174">Die UTC-Komponente eines CIM- [DateTime](datetime.md) -Werts.</span><span class="sxs-lookup"><span data-stu-id="9628c-174">The UTC component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                           |
| [<span data-ttu-id="9628c-175">**Utcangegeben**</span><span class="sxs-lookup"><span data-stu-id="9628c-175">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)<br/>                   | <span data-ttu-id="9628c-176">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9628c-176">Read/write</span></span><br/> | <span data-ttu-id="9628c-177">Gibt an, ob die UTC-Komponente angegeben oder als Platzhalter belassen wird.</span><span class="sxs-lookup"><span data-stu-id="9628c-177">Indicates whether the UTC component is specified or left as a wildcard.</span></span><br/>                                              |
| [<span data-ttu-id="9628c-178">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9628c-178">**Value**</span></span>](swbemdatetime-value.md)<br/>                                 | <span data-ttu-id="9628c-179">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9628c-179">Read/write</span></span><br/> | <span data-ttu-id="9628c-180">Der vollständige CIM- [DateTime](datetime.md) -Wert.</span><span class="sxs-lookup"><span data-stu-id="9628c-180">The full CIM [datetime](datetime.md) value.</span></span><br/>                                                                         |
| [<span data-ttu-id="9628c-181">**Jährigen**</span><span class="sxs-lookup"><span data-stu-id="9628c-181">**Year**</span></span>](swbemdatetime-year.md)<br/>                                   | <span data-ttu-id="9628c-182">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9628c-182">Read/write</span></span><br/> | <span data-ttu-id="9628c-183">Die Jahres Komponente eines CIM- [DateTime](datetime.md) -Werts.</span><span class="sxs-lookup"><span data-stu-id="9628c-183">The year component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                          |
| [<span data-ttu-id="9628c-184">**Yearfest gelegt**</span><span class="sxs-lookup"><span data-stu-id="9628c-184">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)<br/>                 | <span data-ttu-id="9628c-185">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9628c-185">Read/write</span></span><br/> | <span data-ttu-id="9628c-186">Gibt an, ob das Jahr angegeben oder als Platzhalter belassen wird.</span><span class="sxs-lookup"><span data-stu-id="9628c-186">Indicates whether or not the year is specified or left as a wildcard.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="9628c-187">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9628c-187">Remarks</span></span>

<span data-ttu-id="9628c-188">WMI zeichnet Zeitstempel im UTC-Format (Universal Time Koordinate) auf.</span><span class="sxs-lookup"><span data-stu-id="9628c-188">WMI records timestamps in universal time coordinate (UTC) format.</span></span> <span data-ttu-id="9628c-189">UTC ist nicht das Format, das von den meisten Entwicklern und IT-Administratoren verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9628c-189">UTC is not the format that most developers and IT administrators use.</span></span> <span data-ttu-id="9628c-190">Daher besteht ein häufiges Problem darin, zu bestimmen, wie UTC in etwas lesbares übersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9628c-190">Therefore, a common issue is determining how to translate UTC into something more readable.</span></span> <span data-ttu-id="9628c-191">Weitere Informationen zum Arbeiten mit UTC finden Sie unter [WMI-Tasks: Datums-und Uhrzeitwerte](wmi-tasks--dates-and-times.md) und [Arbeiten mit Datums-und Uhrzeitwerten mithilfe von WMI](/previous-versions/tn-archive/ee198928(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="9628c-191">For more information on how to work with UTC, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md) and [Working with Dates and Times using WMI](/previous-versions/tn-archive/ee198928(v=technet.10)).</span></span> <span data-ttu-id="9628c-192">Sie können auch die Informationen zu [Zeit (Oh und zu Datumsangaben)](/previous-versions/technet-magazine/cc160973(v=msdn.10)) lesen und [wie kann ich eine angegebene Anzahl von Tagen von einem UTC-Wert subtrahieren?](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) in Blogbeiträgen finden Sie weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="9628c-192">You can also read the [It s About Time (Oh, and About Dates, Too)](/previous-versions/technet-magazine/cc160973(v=msdn.10)) and [How Can I Subtract a Specified Number of Days from a UTC Value?](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) blog posts for additional information.</span></span>

<span data-ttu-id="9628c-193">Alle numerischen Felder können einen Platzhalter Wert aufweisen, wenn die [**isinterval**](swbemdatetime-isinterval.md) -Eigenschaft auf **false** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9628c-193">Any numeric field can have a wildcard value if the [**IsInterval**](swbemdatetime-isinterval.md) property is set to **FALSE**.</span></span> <span data-ttu-id="9628c-194">Felder mit Platzhalterwerten enthalten Sternchen im gesamten Feld.</span><span class="sxs-lookup"><span data-stu-id="9628c-194">Fields with wildcard values contain asterisks in the entire field.</span></span>

<span data-ttu-id="9628c-195">Jede Eigenschaft, z. b. [**Day**](swbemdatetime-day.md), verfügt über einen entsprechenden festgelegten booleschen Wert, z. b. [**dayangegeben**](swbemdatetime-dayspecified.md).</span><span class="sxs-lookup"><span data-stu-id="9628c-195">Each property, for example [**Day**](swbemdatetime-day.md), has a corresponding specified Boolean value, such as [**DaySpecified**](swbemdatetime-dayspecified.md).</span></span> <span data-ttu-id="9628c-196">Wenn **dayangegebene** den Wert **false** hat, wird der Wert als Intervall und nicht als Zahl zwischen 01 und 31 interpretiert.</span><span class="sxs-lookup"><span data-stu-id="9628c-196">When **DaySpecified** is **FALSE**, then the value is interpreted as an interval rather than a number between 01 and 31.</span></span> <span data-ttu-id="9628c-197">Wenn ein Intervall an einer beliebigen Stelle im CIM- [DateTime](datetime.md) -Wert verwendet wird, wird [**isinterval**](swbemdatetime-isinterval.md) ebenfalls auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9628c-197">If an interval is used anywhere in the CIM [datetime](datetime.md) value, then [**IsInterval**](swbemdatetime-isinterval.md) is also set to **TRUE**.</span></span> <span data-ttu-id="9628c-198">Der Standardwert ist, dass ein CIM-DateTime-Wert ein Datum anstelle eines oder mehrerer Intervalle enthält.</span><span class="sxs-lookup"><span data-stu-id="9628c-198">The default is for a CIM datetime value to contain a date rather than one or more intervals.</span></span>

<span data-ttu-id="9628c-199">Wenn z. b. " [**skibemdatetime. dayangegebene**](swbemdatetime-dayspecified.md) " den Wert " **true**" hat, enthält " [**taubemdatetime. Value**](swbemdatetime-value.md) " den aktuellen Wert von " [**taubemdatetime. Day**](swbemdatetime-day.md)"; Andernfalls ist es ein Platzhalter Wert.</span><span class="sxs-lookup"><span data-stu-id="9628c-199">For example, if [**SWbemDateTime.DaySpecified**](swbemdatetime-dayspecified.md) is **TRUE**, then [**SWbemDateTime.Value**](swbemdatetime-value.md) includes the current value of [**SWbemDateTime.Day**](swbemdatetime-day.md), otherwise it is a wildcard value.</span></span> <span data-ttu-id="9628c-200">Die [**isinterval**](swbemdatetime-isinterval.md) -Eigenschaft ist in beiden Fällen **false** .</span><span class="sxs-lookup"><span data-stu-id="9628c-200">The [**IsInterval**](swbemdatetime-isinterval.md) property is **FALSE** in either case.</span></span>

## <a name="examples"></a><span data-ttu-id="9628c-201">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9628c-201">Examples</span></span>

<span data-ttu-id="9628c-202">Im folgenden Skriptcode Beispiel wird gezeigt, wie ein " **slibemdatetime** "-Objekt verwendet wird, um einen DateTime-Eigenschafts Wert zu analysieren, der aus dem WMI-Repository gelesen wird, die **InstallDate** -Eigenschaft im [**Win32- \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)</span><span class="sxs-lookup"><span data-stu-id="9628c-202">The following script code example shows how to use an **SWbemDateTime** object to parse a datetime property value read from the WMI repository, the **InstallDate** property in [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span></span>


```VB
' Create a new datetime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")

' Retrieve a WMI object that contains a datetime value.
for each os in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

    ' The InstallDate property is a CIM_DATETIME. 
    MsgBox os.InstallDate
    dateTime.Value = os.InstallDate

    ' Display the year of installation.
    MsgBox "This OS was installed in the year " & dateTime.Year

    ' Display the installation date using the VT_DATE format.
    MsgBox "Full installation date (VT_DATE format) is " _
    & dateTime.GetVarDate

    ' Display the installation date using the FILETIME format.
    MsgBox "Full installation date (FILETIME format) is " _
    & dateTime.GetFileTime 
next
Set datetime = Nothing
```



<span data-ttu-id="9628c-203">Im folgenden Beispiel wird gezeigt, wie Sie ein " **slibemdatetime** "-Objekt erstellen, einen Datumswert im Objekt speichern, das Datum als lokale und koordinierte Weltzeit (UTC) anzeigen und den Wert in einer neu erstellten Klasse und Eigenschaft speichern.</span><span class="sxs-lookup"><span data-stu-id="9628c-203">The following example shows how to create an **SWbemDateTime** object, store a date value in the object, display the date as local and Coordinated Universal Time (UTC), and store the value in a newly created class and property.</span></span> <span data-ttu-id="9628c-204">Weitere Informationen zur Konstanten **wbemcimtypedatetime** finden Sie unter [wbemcimtypeenum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span><span class="sxs-lookup"><span data-stu-id="9628c-204">For more information about the constant **wbemCimtypeDatetime**, see [WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span></span>


```VB
' Create an SWbemDateTime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
' Set the value 
Const wbemCimTypeDatetime = 101

' Construct a datetime value using the intrinsic VBScript CDate
' function interpreting this as a local date/time in
' the Pacific time zone (-8 hrs GMT). Convert to CIM datetime
' using SetVarDate method. The year defaults to current year.
dateTime.SetVarDate (CDate ("January 20 11:56:32"))

' The value in dateTime displays as 
' 20000120195632.000000-480. This is the equivalent time
' in GMT with the specified offset for PST of -8 hrs.
MsgBox "CIM datetime " & dateTime

' The value now displays as B=0/2000 11:56:32 AM because the
' parameter contains the default TRUE value causing the value to be
' interpreted as a local time.
MsgBox "Local datetime " & dateTime.GetVarDate ()

' The value now displays as B=0/2000 7:56:32 PM because the
' parameter value is FALSE, which indicates a GMT time.
' non-local time.
MsgBox "Datetime in GMT " & dateTime.GetVarDate (false)

' Create a new class and add a DateTime property value.
' SWbemServices.Get returns an empty SWbemObject
' which can become a new class. SWbemObject.Path_ returns an
' SWbemObjectPath object. 
set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "NewClass"

' Add a new property named "InterestingDate" to the NewObject class
' and define its datatype as a CIM datetime value.
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value of the SWbemDateTime object in the InterestingDate
' property.
NewObject.InterestingDate = dateTime.Value
MsgBox "Datetime in new object " & NewObject.InterestingDate

' Write the new class (named "NewClass") containing
' the SWbemDateTime object to the repository.
NewObject.Put_
WScript.Echo "NewClass is now in WMI repository"

' Clean up the example by deleting the new class from the repository
NewObject.Delete_
```



<span data-ttu-id="9628c-205">Im folgenden Skriptcode Beispiel wird veranschaulicht, wie Sie ein-Objekt mit einem " **Swap DateTime** "-Objekt für eine Eigenschaft ändern, die aus dem WMI-Repository gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="9628c-205">The following script code example shows how to use an **SWbemDateTime** object to modify an interval value on a property that is read from the WMI repository.</span></span>


```VB
' Construct an interval value of 100 days, 1 hour, and 3 seconds.
dateTime.IsInterval = true 
dateTime.Day = 100
dateTime.Hours = 1
dateTime.Seconds = 3

' The datetime displays as 00000100010003.000000:000.
MsgBox "Constructed interval value " & datetime

' Retrieve an empty WMI object and add a datetime property. 
Const wbemCimTypeDatetime = 101
Set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "Empty"
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value in the property and update. 
NewObject.InterestingDate = dateTime.Value
MsgBox "NewObject.InterestingDate = " & NewObject.InterestingDate

' Write the new SWbemDateTime object to the repository.
NewObject.Put_

' Delete the object.
NewObject.Delete_
```



<span data-ttu-id="9628c-206">Im folgenden Skriptcode Beispiel wird gezeigt, wie ein " **slibemdate** "-Objekt verwendet wird, um einen **FILETIME** -Wert zu lesen.</span><span class="sxs-lookup"><span data-stu-id="9628c-206">The following script code example shows how to use an **SWbemDate** object to read a **FILETIME** value.</span></span>


```VB
' Create a new datetime object.
Set datetime = CreateObject("WbemScripting.SWbemDateTime")

' Set from a FILETIME value (non-local).
' Assume a timezone -7 hrs. GMT.
MsgBox "FILETIME value " & "126036951652030000"
datetime.SetFileTime "126036951652030000", false

' Displays as 5/24/2000 7:26:05 PM.
MsgBox "GMT time " & dateTime.GetVarDate   

' Set from a FILETIME value (local).
datetime.SetFileTime "126036951652030000"

' Displays as 5/25/2000 2:26:05 AM.
MsgBox "Same value in local time " & dateTime.GetVarDate
Set datetime = Nothing
```



<span data-ttu-id="9628c-207">Mit dem folgenden PowerShell-Code wird eine Instanz eines SWbemDateTime-Objekts erstellt, das Installationsdatum des Betriebssystems abgerufen und das Datum in ein anderes Format konvertiert.</span><span class="sxs-lookup"><span data-stu-id="9628c-207">The following PowerShell code creates an instance of a SWbemDateTime object, retrieves the OS install date, and converts the date to a different format</span></span>


```PowerShell
# Create swbemdatetime object
$datetime = New-Object -ComObject WbemScripting.SWbemDateTime

#  Get OS installation time and assign to datetime object
$os = Get-WmiObject -Class Win32_OperatingSystem
$dateTime.Value = $os.InstallDate

# Now display the time
"This OS was installed in the year {0}"           -f $dateTime.Year
"Full installation date (VT_DATE format) is {0}"  -f $dateTime.GetVarDate()
"Full installation date (FILETIME format) is {0}" -f $dateTime.GetFileTime() 
```



<span data-ttu-id="9628c-208">Der folgende PowerShell-Code übersetzt den Code in ein Format, das von einem CIM-Anbieter verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9628c-208">The following Powershell code translates the code into a format ready to be consumed by a CIM provider.</span></span>


```PowerShell
 $time = (Get-Date)
 $objScriptTime = New-Object -ComObject WbemScripting.SWbemDateTime
 $objScriptTime.SetVarDate($time)
 $cimTime = $objScriptTime.Value
```



## <a name="requirements"></a><span data-ttu-id="9628c-209">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9628c-209">Requirements</span></span>



| <span data-ttu-id="9628c-210">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9628c-210">Requirement</span></span> | <span data-ttu-id="9628c-211">Wert</span><span class="sxs-lookup"><span data-stu-id="9628c-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9628c-212">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9628c-212">Minimum supported client</span></span><br/> | <span data-ttu-id="9628c-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9628c-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9628c-214">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9628c-214">Minimum supported server</span></span><br/> | <span data-ttu-id="9628c-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9628c-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9628c-216">Header</span><span class="sxs-lookup"><span data-stu-id="9628c-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="9628c-217"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9628c-217"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9628c-218">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9628c-218">Type library</span></span><br/>             | <dl> <span data-ttu-id="9628c-219"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9628c-219"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9628c-220">DLL</span><span class="sxs-lookup"><span data-stu-id="9628c-220">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9628c-221"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9628c-221"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9628c-222">CLSID</span><span class="sxs-lookup"><span data-stu-id="9628c-222">CLSID</span></span><br/>                    | <span data-ttu-id="9628c-223">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="9628c-223">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="9628c-224">IID</span><span class="sxs-lookup"><span data-stu-id="9628c-224">IID</span></span><br/>                      | <span data-ttu-id="9628c-225">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="9628c-225">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="9628c-226">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9628c-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9628c-227">Wbemcimtypeerum</span><span class="sxs-lookup"><span data-stu-id="9628c-227">WbemCimtypeEnum</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dt>

[<span data-ttu-id="9628c-228">DateTime</span><span class="sxs-lookup"><span data-stu-id="9628c-228">DATETIME</span></span>](datetime.md)
</dt> <dt>

[<span data-ttu-id="9628c-229">API-Skript Objekte</span><span class="sxs-lookup"><span data-stu-id="9628c-229">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

