---
description: Die Win32- \_ Zeitzone&\# 8194; Die WMI-Klasse stellt die Zeitzoneninformationen für ein Computersystem dar, auf dem Windows ausgeführt wird, einschließlich der Änderungen, die für den Übergang zur Sommerzeit Umstellung erforderlich sind.
ms.assetid: c1c7731e-768f-42ea-a36c-57b00df6848e
ms.tgt_platform: multiple
title: Win32_TimeZone-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TimeZone
- Win32_TimeZone.Caption
- Win32_TimeZone.Description
- Win32_TimeZone.SettingID
- Win32_TimeZone.Bias
- Win32_TimeZone.DaylightBias
- Win32_TimeZone.DaylightDay
- Win32_TimeZone.DaylightDayOfWeek
- Win32_TimeZone.DaylightHour
- Win32_TimeZone.DaylightMillisecond
- Win32_TimeZone.DaylightMinute
- Win32_TimeZone.DaylightMonth
- Win32_TimeZone.DaylightName
- Win32_TimeZone.DaylightSecond
- Win32_TimeZone.DaylightYear
- Win32_TimeZone.StandardBias
- Win32_TimeZone.StandardDay
- Win32_TimeZone.StandardDayOfWeek
- Win32_TimeZone.StandardHour
- Win32_TimeZone.StandardMillisecond
- Win32_TimeZone.StandardMinute
- Win32_TimeZone.StandardMonth
- Win32_TimeZone.StandardName
- Win32_TimeZone.StandardSecond
- Win32_TimeZone.StandardYear
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 433682f045ca7fb127c7dc69e3a26ed8356371ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861016"
---
# <a name="win32_timezone-class"></a><span data-ttu-id="7e20a-103">Win32- \_ Zeit Zonen Klasse</span><span class="sxs-lookup"><span data-stu-id="7e20a-103">Win32\_TimeZone class</span></span>

<span data-ttu-id="7e20a-104">Die  [WMI-Klasse](../wmisdk/retrieving-a-class.md) der **Win32- \_ Zeitzone** stellt die Zeitzoneninformationen für ein Computersystem dar, auf dem Windows ausgeführt wird, das die Änderungen beinhaltet, die für den Übergang zur Sommerzeit Umstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7e20a-104">The **Win32\_TimeZone** [WMI class](../wmisdk/retrieving-a-class.md) represents the time zone information for a computer system running Windows, which includes the changes required for transitioning to daylight saving time transition.</span></span>

<span data-ttu-id="7e20a-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7e20a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7e20a-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="7e20a-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e20a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e20a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_TimeZone : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  sint32 Bias;
  sint32 DaylightBias;
  uint32 DaylightDay;
  uint8  DaylightDayOfWeek;
  uint32 DaylightHour;
  uint32 DaylightMillisecond;
  uint32 DaylightMinute;
  uint32 DaylightMonth;
  string DaylightName;
  uint32 DaylightSecond;
  uint32 DaylightYear;
  uint32 StandardBias;
  uint32 StandardDay;
  uint8  StandardDayOfWeek;
  uint32 StandardHour;
  uint32 StandardMillisecond;
  uint32 StandardMinute;
  uint32 StandardMonth;
  string StandardName;
  uint32 StandardSecond;
  uint32 StandardYear;
};
```

## <a name="members"></a><span data-ttu-id="7e20a-108">Member</span><span class="sxs-lookup"><span data-stu-id="7e20a-108">Members</span></span>

<span data-ttu-id="7e20a-109">Die **Win32- \_ Zeit Zonen** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7e20a-109">The **Win32\_TimeZone** class has these types of members:</span></span>

-   [<span data-ttu-id="7e20a-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7e20a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e20a-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7e20a-111">Properties</span></span>

<span data-ttu-id="7e20a-112">Die **Win32- \_ Zeit Zonen** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7e20a-112">The **Win32\_TimeZone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e20a-113">**Verzerrung (Bias)**</span><span class="sxs-lookup"><span data-stu-id="7e20a-113">**Bias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-114">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e20a-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-116">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Zeitstrukturen \| [**Zeit \_ Zonen \_ Informationen**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| Bias"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Minuten")</span><span class="sxs-lookup"><span data-stu-id="7e20a-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|Bias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-117">Aktuelle Abweichung für die lokale Zeit Übersetzung.</span><span class="sxs-lookup"><span data-stu-id="7e20a-117">Current bias for local time translation.</span></span> <span data-ttu-id="7e20a-118">Die Verschiebung ist der Unterschied zwischen koordinierter Weltzeit (UTC) und Ortszeit.</span><span class="sxs-lookup"><span data-stu-id="7e20a-118">The bias is the difference between Coordinated Universal Time (UTC) and local time.</span></span> <span data-ttu-id="7e20a-119">Alle Übersetzungen zwischen UTC und Ortszeit basieren auf der folgenden Formel: UTC = Local Time-Bias.</span><span class="sxs-lookup"><span data-stu-id="7e20a-119">All translations between UTC and local time are based on the following formula: UTC = local time - bias.</span></span> <span data-ttu-id="7e20a-120">Diese Eigenschaft ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="7e20a-120">This property is required.</span></span>

</dd> <dt>

<span data-ttu-id="7e20a-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7e20a-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e20a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-124">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="7e20a-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-125">Kurze Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7e20a-125">Short textual description of the current object.</span></span>

<span data-ttu-id="7e20a-126">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e20a-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e20a-127">**DaylightBias**</span><span class="sxs-lookup"><span data-stu-id="7e20a-127">**DaylightBias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-128">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e20a-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-130">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("Minutes")</span><span class="sxs-lookup"><span data-stu-id="7e20a-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-131">Der für die lokale Zeit Übersetzungen zu verwendende Wert, der während der Sommerzeit auftritt.</span><span class="sxs-lookup"><span data-stu-id="7e20a-131">Bias value to be used during local time translations that occur during daylight saving time.</span></span> <span data-ttu-id="7e20a-132">Diese Eigenschaft wird ignoriert, wenn kein Wert für die **DaylightDay** -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7e20a-132">This property is ignored if a value for the **DaylightDay** property is not supplied.</span></span> <span data-ttu-id="7e20a-133">Der Wert dieser Eigenschaft wird der Eigenschaft " **Bias** " hinzugefügt, um die während der Sommerzeit verwendete Abweichung zu bilden.</span><span class="sxs-lookup"><span data-stu-id="7e20a-133">The value of this property is added to the **Bias** property to form the bias used during daylight time.</span></span> <span data-ttu-id="7e20a-134">In den meisten Zeitzonen ist der Wert dieser Eigenschaft-60.</span><span class="sxs-lookup"><span data-stu-id="7e20a-134">In most time zones, the value of this property is -60.</span></span>

</dd> <dt>

<span data-ttu-id="7e20a-135">**DaylightDay**</span><span class="sxs-lookup"><span data-stu-id="7e20a-135">**DaylightDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-136">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e20a-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-138">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate \| wDay")</span><span class="sxs-lookup"><span data-stu-id="7e20a-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wDay")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-139">**DaylightDayOfWeek** von **DaylightMonth** , wenn die Umstellung von Standardzeit auf Sommerzeit auf diesem Betriebssystem erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7e20a-139">**DaylightDayOfWeek** of the **DaylightMonth** when the transition from standard time to daylight saving time occurs on this operating system.</span></span>

<span data-ttu-id="7e20a-140">Beispiel: Wenn der Übergangs Tag (**daylightdayosweek**) an einem Sonntag stattfindet, gibt der Wert "1" den ersten Sonntag des **DaylightMonth** an, "2" gibt den zweiten Sonntag an usw.</span><span class="sxs-lookup"><span data-stu-id="7e20a-140">Example: If the transition day (**DaylightDayOfWeek**) occurs on a Sunday, then the value "1" indicates the first Sunday of the **DaylightMonth**, "2" indicates the second Sunday, and so on.</span></span> <span data-ttu-id="7e20a-141">Der Wert "5" gibt die letzte **daylightdayof-Woche** im Monat an.</span><span class="sxs-lookup"><span data-stu-id="7e20a-141">The value "5" indicates the last **DaylightDayOfWeek** in the month.</span></span>

</dd> <dt>

<span data-ttu-id="7e20a-142">**Daylightdayof Week**</span><span class="sxs-lookup"><span data-stu-id="7e20a-142">**DaylightDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-143">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="7e20a-143">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-145">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate \| wdayof Week")</span><span class="sxs-lookup"><span data-stu-id="7e20a-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wDayOfWeek")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-146">Der Wochentag, an dem die Umstellung von Standardzeit auf Sommerzeit auf einem Betriebssystem erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7e20a-146">Day of the week when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="7e20a-147">**Sonntag** (0)</span><span class="sxs-lookup"><span data-stu-id="7e20a-147">**Sunday** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="7e20a-148">**Montag** (1)</span><span class="sxs-lookup"><span data-stu-id="7e20a-148">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="7e20a-149">**Dienstag** (2)</span><span class="sxs-lookup"><span data-stu-id="7e20a-149">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="7e20a-150">**Mittwoch** (3)</span><span class="sxs-lookup"><span data-stu-id="7e20a-150">**Wednesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="7e20a-151">**Donnerstag** (4)</span><span class="sxs-lookup"><span data-stu-id="7e20a-151">**Thursday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="7e20a-152">**Freitag** (5)</span><span class="sxs-lookup"><span data-stu-id="7e20a-152">**Friday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="7e20a-153">**Samstag** (6)</span><span class="sxs-lookup"><span data-stu-id="7e20a-153">**Saturday** (6)</span></span>


<span data-ttu-id="7e20a-154"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7e20a-154"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="7e20a-155">Beispiel: 1</span><span class="sxs-lookup"><span data-stu-id="7e20a-155">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="7e20a-156">**DaylightHour**</span><span class="sxs-lookup"><span data-stu-id="7e20a-156">**DaylightHour**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e20a-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-159">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate \| wHour")</span><span class="sxs-lookup"><span data-stu-id="7e20a-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wHour")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-160">Stunde des Tages, zu der die Umstellung von Standardzeit auf Sommerzeit auf einem Betriebssystem erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7e20a-160">Hour of the day when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="7e20a-161">Beispiel: 2</span><span class="sxs-lookup"><span data-stu-id="7e20a-161">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="7e20a-162">**Daylightmillisekunde**</span><span class="sxs-lookup"><span data-stu-id="7e20a-162">**DaylightMillisecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-163">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e20a-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-165">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate \| wMilliseconds")</span><span class="sxs-lookup"><span data-stu-id="7e20a-165">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMilliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-166">Millisekunde von **DaylightSecond** , wenn die Umstellung von Standardzeit auf Sommerzeit in einem Betriebssystem erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7e20a-166">Millisecond of the **DaylightSecond** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

</dd> <dt>

<span data-ttu-id="7e20a-167">**DaylightMinute**</span><span class="sxs-lookup"><span data-stu-id="7e20a-167">**DaylightMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-168">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e20a-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-170">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate \| wMinute")</span><span class="sxs-lookup"><span data-stu-id="7e20a-170">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMinute")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-171">Minute von **DaylightHour** , wenn die Umstellung von Standardzeit auf Sommerzeit auf einem Betriebssystem erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7e20a-171">Minute of the **DaylightHour** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="7e20a-172">Beispiel: 59</span><span class="sxs-lookup"><span data-stu-id="7e20a-172">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="7e20a-173">**DaylightMonth**</span><span class="sxs-lookup"><span data-stu-id="7e20a-173">**DaylightMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-174">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e20a-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-176">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate \| wMonth")</span><span class="sxs-lookup"><span data-stu-id="7e20a-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMonth")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-177">Monat, in dem die Umstellung von Standardzeit auf Sommerzeit in einem Betriebssystem erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7e20a-177">Month when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="7e20a-178">**Januar** (1)</span><span class="sxs-lookup"><span data-stu-id="7e20a-178">**January** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="7e20a-179">**Februar** (2)</span><span class="sxs-lookup"><span data-stu-id="7e20a-179">**February** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="7e20a-180">**März** (3)</span><span class="sxs-lookup"><span data-stu-id="7e20a-180">**March** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="7e20a-181">**April** (4)</span><span class="sxs-lookup"><span data-stu-id="7e20a-181">**April** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="7e20a-182">**Mai** (5)</span><span class="sxs-lookup"><span data-stu-id="7e20a-182">**May** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="7e20a-183">**Juni** (6)</span><span class="sxs-lookup"><span data-stu-id="7e20a-183">**June** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="7e20a-184">**Juli** (7)</span><span class="sxs-lookup"><span data-stu-id="7e20a-184">**July** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="7e20a-185">**August** (8)</span><span class="sxs-lookup"><span data-stu-id="7e20a-185">**August** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="7e20a-186">**September** (9)</span><span class="sxs-lookup"><span data-stu-id="7e20a-186">**September** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="7e20a-187">**Oktober** (10)</span><span class="sxs-lookup"><span data-stu-id="7e20a-187">**October** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="7e20a-188">**November** (11)</span><span class="sxs-lookup"><span data-stu-id="7e20a-188">**November** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="7e20a-189">**Dezember** (12)</span><span class="sxs-lookup"><span data-stu-id="7e20a-189">**December** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7e20a-190">**DaylightName**</span><span class="sxs-lookup"><span data-stu-id="7e20a-190">**DaylightName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-191">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e20a-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-193">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightName")</span><span class="sxs-lookup"><span data-stu-id="7e20a-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightName")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-194">Die Zeitzone, die dargestellt wird, wenn die Sommerzeit wirksam ist.</span><span class="sxs-lookup"><span data-stu-id="7e20a-194">Time zone being represented when daylight saving time is in effect.</span></span>

<span data-ttu-id="7e20a-195">Beispiel: "EDT" (Eastern Sommerzeit)</span><span class="sxs-lookup"><span data-stu-id="7e20a-195">Example: "EDT" (Eastern Daylight Time)</span></span>

</dd> <dt>

<span data-ttu-id="7e20a-196">**DaylightSecond**</span><span class="sxs-lookup"><span data-stu-id="7e20a-196">**DaylightSecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-197">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e20a-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-199">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate \| wSecond")</span><span class="sxs-lookup"><span data-stu-id="7e20a-199">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wSecond")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-200">Second von **DaylightMinute** , wenn die Umstellung von Standardzeit auf Sommerzeit in einem Betriebssystem erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7e20a-200">Second of the **DaylightMinute** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="7e20a-201">Beispiel: 59</span><span class="sxs-lookup"><span data-stu-id="7e20a-201">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="7e20a-202">**DaylightYear**</span><span class="sxs-lookup"><span data-stu-id="7e20a-202">**DaylightYear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-203">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e20a-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-205">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate \| wYear")</span><span class="sxs-lookup"><span data-stu-id="7e20a-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wYear")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-206">Jahr, wenn die Sommerzeit wirksam ist.</span><span class="sxs-lookup"><span data-stu-id="7e20a-206">Year when daylight saving time is in effect.</span></span> <span data-ttu-id="7e20a-207">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7e20a-207">This property is not required.</span></span>

<span data-ttu-id="7e20a-208">Beispiel: 1997</span><span class="sxs-lookup"><span data-stu-id="7e20a-208">Example: 1997</span></span>

</dd> <dt>

<span data-ttu-id="7e20a-209">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e20a-209">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e20a-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-212">Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7e20a-212">Textual description of the current object.</span></span>

<span data-ttu-id="7e20a-213">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e20a-213">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e20a-214">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="7e20a-214">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-215">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e20a-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-216">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-217">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="7e20a-217">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-218">Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="7e20a-218">Identifier by which the current object is known.</span></span>

<span data-ttu-id="7e20a-219">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e20a-219">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e20a-220">**Standard Bias**</span><span class="sxs-lookup"><span data-stu-id="7e20a-220">**StandardBias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-221">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e20a-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-223">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Zeitstrukturen \| [**Zeit \_ Zonen \_ Informationen**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardBias"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Minuten")</span><span class="sxs-lookup"><span data-stu-id="7e20a-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-224">Der zu verwendende biaswert, wenn die Sommerzeit nicht wirksam ist.</span><span class="sxs-lookup"><span data-stu-id="7e20a-224">Bias value to use when daylight saving time is not in effect.</span></span> <span data-ttu-id="7e20a-225">Diese Eigenschaft wird ignoriert, wenn kein Wert für **StandardDay** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7e20a-225">This property is ignored if a value for **StandardDay** is not supplied.</span></span> <span data-ttu-id="7e20a-226">Der Wert dieser Eigenschaft wird der Eigenschaft " **Bias** " hinzugefügt, um die Verschiebung während der Standardzeit zu bilden.</span><span class="sxs-lookup"><span data-stu-id="7e20a-226">The value of this property is added to the **Bias** property to form the bias during standard time.</span></span>

<span data-ttu-id="7e20a-227">Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="7e20a-227">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="7e20a-228">**StandardDay**</span><span class="sxs-lookup"><span data-stu-id="7e20a-228">**StandardDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-229">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e20a-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-231">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate \| wDay")</span><span class="sxs-lookup"><span data-stu-id="7e20a-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wDay")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-232">**StandardDayOfWeek** des **StandardMonth** , wenn der Übergang von Sommerzeit zu Normalzeit in einem Betriebssystem erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7e20a-232">**StandardDayOfWeek** of the **StandardMonth** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="7e20a-233">Wenn der Übergangs Tag (**standarddayosweek**) an einem Sonntag stattfindet, gibt der Wert "1" den ersten Sonntag des **StandardMonth** an, "2" den zweiten Sonntag und so weiter.</span><span class="sxs-lookup"><span data-stu-id="7e20a-233">If the transition day (**StandardDayOfWeek**) occurs on a Sunday, then the value "1" indicates the first Sunday of the **StandardMonth**, "2" indicates the second Sunday, and so on.</span></span> <span data-ttu-id="7e20a-234">Der Wert "5" gibt die letzte **standarddayof-Woche** im Monat an.</span><span class="sxs-lookup"><span data-stu-id="7e20a-234">The value "5" indicates the last **StandardDayOfWeek** in the month.</span></span>

</dd> <dt>

<span data-ttu-id="7e20a-235">**Standarddayogweek**</span><span class="sxs-lookup"><span data-stu-id="7e20a-235">**StandardDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-236">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="7e20a-236">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-237">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-238">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**Zeit \_ Zonen \_ Informationen**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate \| wdayof Week")</span><span class="sxs-lookup"><span data-stu-id="7e20a-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wDayOfWeek")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-239">Der Wochentag, an dem die Umstellung von Sommerzeit auf Standardzeit in einem Betriebssystem erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7e20a-239">Day of the week when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="7e20a-240">**Sonntag** (0)</span><span class="sxs-lookup"><span data-stu-id="7e20a-240">**Sunday** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="7e20a-241">**Montag** (1)</span><span class="sxs-lookup"><span data-stu-id="7e20a-241">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="7e20a-242">**Dienstag** (2)</span><span class="sxs-lookup"><span data-stu-id="7e20a-242">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="7e20a-243">**Mittwoch** (3)</span><span class="sxs-lookup"><span data-stu-id="7e20a-243">**Wednesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="7e20a-244">**Donnerstag** (4)</span><span class="sxs-lookup"><span data-stu-id="7e20a-244">**Thursday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="7e20a-245">**Freitag** (5)</span><span class="sxs-lookup"><span data-stu-id="7e20a-245">**Friday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="7e20a-246">**Samstag** (6)</span><span class="sxs-lookup"><span data-stu-id="7e20a-246">**Saturday** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7e20a-247">**StandardHour**</span><span class="sxs-lookup"><span data-stu-id="7e20a-247">**StandardHour**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-248">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e20a-248">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-249">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-250">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**Zeit \_ Zonen \_ Informationen**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate \| wHour")</span><span class="sxs-lookup"><span data-stu-id="7e20a-250">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wHour")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-251">Stunde des Tages, zu der die Umstellung von Sommerzeit auf Standardzeit in einem Betriebssystem erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7e20a-251">Hour of the day when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="7e20a-252">Beispiel: 11</span><span class="sxs-lookup"><span data-stu-id="7e20a-252">Example: 11</span></span>

</dd> <dt>

<span data-ttu-id="7e20a-253">**Standardmillisekunde**</span><span class="sxs-lookup"><span data-stu-id="7e20a-253">**StandardMillisecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-254">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e20a-254">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-255">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-256">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Zeitstrukturen \| [**Zeit \_ Zonen \_ Informationen**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate \| wMilliseconds")</span><span class="sxs-lookup"><span data-stu-id="7e20a-256">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMilliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-257">Millisekunde der **StandardSecond** , wenn die Umstellung von Sommerzeit auf Standardzeit in einem Betriebssystem erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7e20a-257">Millisecond of the **StandardSecond** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

</dd> <dt>

<span data-ttu-id="7e20a-258">**Standard Minute**</span><span class="sxs-lookup"><span data-stu-id="7e20a-258">**StandardMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-259">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e20a-259">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-260">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-261">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate \| wMinute")</span><span class="sxs-lookup"><span data-stu-id="7e20a-261">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMinute")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-262">Minute des **StandardDay** , wenn die Umstellung von Sommerzeit auf Standardzeit in einem Betriebssystem erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7e20a-262">Minute of the **StandardDay** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="7e20a-263">Beispiel: 59</span><span class="sxs-lookup"><span data-stu-id="7e20a-263">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="7e20a-264">**StandardMonth**</span><span class="sxs-lookup"><span data-stu-id="7e20a-264">**StandardMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-265">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e20a-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-266">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-267">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate \| wMonth")</span><span class="sxs-lookup"><span data-stu-id="7e20a-267">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMonth")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-268">Monat, wenn die Umstellung von Sommerzeit auf Standardzeit in einem Betriebssystem erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7e20a-268">Month when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="7e20a-269">**Januar** (1)</span><span class="sxs-lookup"><span data-stu-id="7e20a-269">**January** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="7e20a-270">**Februar** (2)</span><span class="sxs-lookup"><span data-stu-id="7e20a-270">**February** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="7e20a-271">**März** (3)</span><span class="sxs-lookup"><span data-stu-id="7e20a-271">**March** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="7e20a-272">**April** (4)</span><span class="sxs-lookup"><span data-stu-id="7e20a-272">**April** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="7e20a-273">**Mai** (5)</span><span class="sxs-lookup"><span data-stu-id="7e20a-273">**May** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="7e20a-274">**Juni** (6)</span><span class="sxs-lookup"><span data-stu-id="7e20a-274">**June** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="7e20a-275">**Juli** (7)</span><span class="sxs-lookup"><span data-stu-id="7e20a-275">**July** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="7e20a-276">**August** (8)</span><span class="sxs-lookup"><span data-stu-id="7e20a-276">**August** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="7e20a-277">**September** (9)</span><span class="sxs-lookup"><span data-stu-id="7e20a-277">**September** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="7e20a-278">**Oktober** (10)</span><span class="sxs-lookup"><span data-stu-id="7e20a-278">**October** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="7e20a-279">**November** (11)</span><span class="sxs-lookup"><span data-stu-id="7e20a-279">**November** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="7e20a-280">**Dezember** (12)</span><span class="sxs-lookup"><span data-stu-id="7e20a-280">**December** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7e20a-281">**Standardname**</span><span class="sxs-lookup"><span data-stu-id="7e20a-281">**StandardName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-282">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e20a-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-283">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-284">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| Standardname")</span><span class="sxs-lookup"><span data-stu-id="7e20a-284">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardName")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-285">Der Name der Zeitzone, die dargestellt wird, wenn die Standardzeit wirksam ist.</span><span class="sxs-lookup"><span data-stu-id="7e20a-285">Name of the time zone being represented when standard time is in effect.</span></span>

<span data-ttu-id="7e20a-286">Beispiel: "EST" (Eastern Normalzeit)</span><span class="sxs-lookup"><span data-stu-id="7e20a-286">Example: "EST" (Eastern Standard Time)</span></span>

</dd> <dt>

<span data-ttu-id="7e20a-287">**StandardSecond**</span><span class="sxs-lookup"><span data-stu-id="7e20a-287">**StandardSecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-288">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e20a-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-290">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate \| wSecond")</span><span class="sxs-lookup"><span data-stu-id="7e20a-290">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wSecond")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-291">Die zweite der **Standard Minuten** , wenn die Umstellung von Sommerzeit auf Normalzeit in einem Betriebssystem erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7e20a-291">Second of the **StandardMinute** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="7e20a-292">Beispiel: 59</span><span class="sxs-lookup"><span data-stu-id="7e20a-292">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="7e20a-293">**Standard Jahr**</span><span class="sxs-lookup"><span data-stu-id="7e20a-293">**StandardYear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e20a-294">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e20a-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e20a-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e20a-296">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate \| wYear")</span><span class="sxs-lookup"><span data-stu-id="7e20a-296">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wYear")</span></span>
</dt> </dl>

<span data-ttu-id="7e20a-297">Jahr, in dem die Standardzeit wirksam ist.</span><span class="sxs-lookup"><span data-stu-id="7e20a-297">Year when standard time is in effect.</span></span> <span data-ttu-id="7e20a-298">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7e20a-298">This property is not required.</span></span>

<span data-ttu-id="7e20a-299">Beispiel: 1997</span><span class="sxs-lookup"><span data-stu-id="7e20a-299">Example: 1997</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e20a-300">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e20a-300">Remarks</span></span>

<span data-ttu-id="7e20a-301">Die **Win32- \_ Zeit Zonen** Klasse wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7e20a-301">The **Win32\_TimeZone** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="7e20a-302">Beim Schreiben von WMI-Abfragen können Standardformate für Datum/Uhrzeit (z. b. 10/18/2002) nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e20a-302">You cannot use standard date-time formats - such as 10/18/2002 - when writing WMI queries.</span></span> <span data-ttu-id="7e20a-303">Stattdessen müssen Sie alle Datumsangaben, die in Ihren Abfragen verwendet werden, in das UTC-Format konvertieren.</span><span class="sxs-lookup"><span data-stu-id="7e20a-303">Instead, you need to convert any dates used in your queries to UTC format.</span></span> <span data-ttu-id="7e20a-304">Hierfür sind zwei Schritte erforderlich: 1) Sie müssen den Offset (Differenz in Minuten) zwischen Ihrer Zeitzone und der Ortszeit (Greenwich Mean Time) und 2) bestimmen. Sie müssen 10/18/2002 in einen UTC-Wert konvertieren.</span><span class="sxs-lookup"><span data-stu-id="7e20a-304">This requires two steps: 1) You must determine the offset (difference in minutes) between your time zone and Greenwich Mean Time, and 2) you must convert 10/18/2002 to a UTC value.</span></span>

<span data-ttu-id="7e20a-305">Bestimmen des Offsets von der Greenwich Mean Time</span><span class="sxs-lookup"><span data-stu-id="7e20a-305">Determining the Offset from Greenwich Mean Time</span></span>

<span data-ttu-id="7e20a-306">Zugegebenermaßen macht WMI es schwierig, mit Datums-und Uhrzeitwerten zu arbeiten. Glücklicherweise erleichtert WMI das Ermitteln des Offsets zwischen Ihrer Zeitzone und der Ortszeit (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="7e20a-306">Admittedly, WMI makes it difficult to work with dates and times; fortunately, WMI at least makes it easy to determine the offset between your time zone and Greenwich Mean Time.</span></span> <span data-ttu-id="7e20a-307">Die Win32-Zeitzone der WMI \_ -Klasse enthält eine Eigenschaft-Bias, die den GMT-Offset zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7e20a-307">The WMI class Win32\_TimeZone includes a property - Bias - that returns the GMT offset.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 Wscript.Echo "Offset: "& objTimeZone.Bias
Next
```



<span data-ttu-id="7e20a-308">Wandeln eines Datums in einen UTC-Wert</span><span class="sxs-lookup"><span data-stu-id="7e20a-308">Converting a Date to a UTC Value</span></span>

<span data-ttu-id="7e20a-309">Nachdem Sie den GMT-Offset festgelegt haben, müssen Sie ein Standard Datum, z. b. 10/18/2002, in ein UTC-Datum konvertieren.</span><span class="sxs-lookup"><span data-stu-id="7e20a-309">After you determine the GMT offset, you must then convert a standard date such as 10/18/2002 to a UTC date.</span></span> <span data-ttu-id="7e20a-310">Zum Konvertieren eines Standard Datums in ein UTC-Datum können Sie VBScript-Datumsfunktionen wie z. b. Jahr, Monat und Tag verwenden, um die einzelnen Komponenten zu isolieren, die ein UTC-Datum bilden.</span><span class="sxs-lookup"><span data-stu-id="7e20a-310">To convert a standard date to a UTC date, you can use VBScript date functions such as Year, Month, and Day to isolate the individual components that make up a UTC date.</span></span> <span data-ttu-id="7e20a-311">Nachdem Sie einzelne Werte für diese Komponenten erstellt haben, können Sie Sie auf die gleiche Weise wie andere Zeichen folgen Werte verketten.</span><span class="sxs-lookup"><span data-stu-id="7e20a-311">After you have individual values for these components, you can concatenate them in the same manner as you would any other string value.</span></span> <span data-ttu-id="7e20a-312">UTC-Datumsangaben werden als Zeichen folgen behandelt, da der GMT-Offset am Ende angehängt werden muss.</span><span class="sxs-lookup"><span data-stu-id="7e20a-312">UTC dates are treated as strings because the GMT offset must be appended to the end.</span></span> <span data-ttu-id="7e20a-313">Wenn das Datum als Zahl angezeigt wird, lautet dieser Wert:</span><span class="sxs-lookup"><span data-stu-id="7e20a-313">If the date were seen as a number, this value:</span></span>

`20011018113047.000000-480`

<span data-ttu-id="7e20a-314">Wird fälschlicherweise als mathematische Gleichung behandelt (aus Gründen der Übersichtlichkeit hinzugefügte Klammern):</span><span class="sxs-lookup"><span data-stu-id="7e20a-314">Would be erroneously treated as a mathematical equation (parentheses added for clarity):</span></span>

`(20011018113047.000000) - (480)`

<span data-ttu-id="7e20a-315">Beispielsweise sind im Datum 10/18/2002 die einzelnen Komponenten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7e20a-315">For example, in the date 10/18/2002, the individual components are:</span></span>

-   <span data-ttu-id="7e20a-316">Jahr: 2002</span><span class="sxs-lookup"><span data-stu-id="7e20a-316">Year: 2002</span></span>
-   <span data-ttu-id="7e20a-317">Monat: 10</span><span class="sxs-lookup"><span data-stu-id="7e20a-317">Month: 10</span></span>
-   <span data-ttu-id="7e20a-318">Tag: 18</span><span class="sxs-lookup"><span data-stu-id="7e20a-318">Day: 18</span></span>

<span data-ttu-id="7e20a-319">Das Skript muss diese drei Werte kombinieren, die Zeichenfolge "113047,000000" (die die Uhrzeit, einschließlich der Millisekunden) und der GMT-Offset zum Ableiten eines UTC-Datums.</span><span class="sxs-lookup"><span data-stu-id="7e20a-319">The script would need to combine these three values, the string "113047.000000" (representing the time, including milliseconds), and the GMT offset to derive a UTC date.</span></span> <span data-ttu-id="7e20a-320">Z. b. (aus Gründen der Übersichtlichkeit wurden wieder Klammern hinzugefügt):</span><span class="sxs-lookup"><span data-stu-id="7e20a-320">For example, (parentheses again added for clarity):</span></span>

`(2002) & (10) & (18) & (113047.000000) & (-480)`

> [!Note]  
> <span data-ttu-id="7e20a-321">Sie können die VBScript-Funktionen "Hour", "Minute" und "Second" verwenden, um den Uhrzeit Teil eines UTC-Datums zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="7e20a-321">You can use the VBScript functions Hour, Minute, and Second to convert the time portion of a UTC date.</span></span> <span data-ttu-id="7e20a-322">Eine Uhrzeit, z. b. 11:30:47 Uhr</span><span class="sxs-lookup"><span data-stu-id="7e20a-322">Thus, a time such as 11:30:47 A.M.</span></span> <span data-ttu-id="7e20a-323">würde in 113047 konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="7e20a-323">would be converted to 113047.</span></span>

 

<span data-ttu-id="7e20a-324">Es gibt einen complilikations Faktor.</span><span class="sxs-lookup"><span data-stu-id="7e20a-324">There is one complicating factor.</span></span> <span data-ttu-id="7e20a-325">Der Monat muss die Positionen 5 und 6 in der Zeichenfolge belegen. der Tag muss die Positionen 7 und 8 annehmen.</span><span class="sxs-lookup"><span data-stu-id="7e20a-325">The month must take up positions 5 and 6 in the string; the day must take up positions 7 and 8.</span></span> <span data-ttu-id="7e20a-326">Dies ist kein Problem für den Monat 10 und den 18. Tag.</span><span class="sxs-lookup"><span data-stu-id="7e20a-326">This is no problem with month 10 and day 18.</span></span> <span data-ttu-id="7e20a-327">Aber wie erhalten Sie den 5. Juli (Monat 7, Tag 5), um die erforderlichen Positionen zu füllen?</span><span class="sxs-lookup"><span data-stu-id="7e20a-327">But how do you get July 5 (month 7, day 5) to fill up the requisite positions?</span></span> <span data-ttu-id="7e20a-328">Die Antwort besteht darin, jedem Wert einen führenden Null-Wert hinzuzufügen und somit 7 in 07 und 5 in 05 zu ändern.</span><span class="sxs-lookup"><span data-stu-id="7e20a-328">The answer is to add a leading zero to each value, thus changing the 7 to 07 and the 5 to 05.</span></span>

<span data-ttu-id="7e20a-329">Verwenden Sie hierzu die VBScript-Len-Funktion, um die Länge (Anzahl der Zeichen) im Monat und Tag zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7e20a-329">To do this, use the VBScript Len function to check the length (number of characters) in the month and the day.</span></span> <span data-ttu-id="7e20a-330">Wenn die Länge 1 beträgt (was bedeutet, dass es nur ein Zeichen gibt), fügen Sie eine führende Null hinzu.</span><span class="sxs-lookup"><span data-stu-id="7e20a-330">If the length is 1 (meaning that there is just one character), add a leading zero.</span></span> <span data-ttu-id="7e20a-331">Bisher</span><span class="sxs-lookup"><span data-stu-id="7e20a-331">Thus:</span></span>


```VB
If Len(dtmMonth) = 1 Then
    dtmMonth = "0" & dtmMonth
End If
```



## <a name="examples"></a><span data-ttu-id="7e20a-332">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e20a-332">Examples</span></span>

<span data-ttu-id="7e20a-333">Im folgenden VBScript-Beispiel wird das aktuelle Datum in ein UTC-Datum konvertiert.</span><span class="sxs-lookup"><span data-stu-id="7e20a-333">The following VBScript example converts the current date to a UTC date.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 strBias = objTimeZone.Bias
Next

dtmCurrentDate = Date
dtmTargetDate = Year(dtmCurrentDate)

dtmMonth = Month(dtmCurrentDate)
If Len(dtmMonth) = 1 Then
 dtmMonth = "0" & dtmMonth
End If

dtmTargetDate = dtmTargetDate & dtmMonth

dtmDay = Day(dtmCurrentDate)
If Len(dtmDay) = 1 Then
 dtmDay = "0" & dtmDay
End If

dtmTargetDate = dtmTargetDate & dtmDay & "000000.000000"
dtmTargetDate = dtmTargetDate & Cstr(strBias)
```



<span data-ttu-id="7e20a-334">Das folgende VBScript-samplebestimmt den GMT-Offset und konvertiert dann ein angegebenes Aktuelles Datum (in diesem Fall 10/18/2002) in das UTC-Datums-/Uhrzeitformat.</span><span class="sxs-lookup"><span data-stu-id="7e20a-334">The following VBScript sampledetermines the GMT offset, and then converts a specified current date (in this case, 10/18/2002) to UTC date-time format.</span></span> <span data-ttu-id="7e20a-335">Nachdem das Datum konvertiert wurde, wird dieser Wert zum Durchsuchen eines Computers verwendet und gibt eine Liste aller Ordner zurück, die nach 10/18/2002 erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="7e20a-335">After the date has been converted, that value is used to search a computer and returns a list of all the folders that were created after 10/18/2002.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 strBias = objTimeZone.Bias
Next

dtmCurrentDate = "10/18/2002"
dtmTargetDate = Year(dtmCurrentDate)

dtmMonth = Month(dtmCurrentDate)
If Len(dtmMonth) = 1 Then
 dtmMonth = "0" & dtmMonth
End If

dtmTargetDate = dtmTargetDate & dtmMonth

dtmDay = Day(dtmCurrentDate)
If Len(dtmDay) = 1 Then
 dtmDay = "0" & dtmDay
End If

dtmTargetDate = dtmTargetDate & dtmDay & "000000.000000"
dtmTargetDate = dtmTargetDate & Cstr(strBias)

Set colFolders = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE CreationDate < '" & _
 dtmtargetDate & "'")
For Each objFolder in colFolders
 Wscript.Echo objFolder.Name
Next
```



<span data-ttu-id="7e20a-336">Im folgenden VBScript-Codebeispiel werden die Einstellungen für Win32- \_ Zeit Zonen Instanzen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7e20a-336">The following VBScript code example displays the settings for Win32\_TimeZone instances.</span></span>


```VB
Dim arDayOrWeek(7)
arDayOrWeek(0) = "Sunday"
arDayOrWeek(1) = "Monday"
arDayOrWeek(2) = "Tuesday"
arDayOrWeek(3) = "Wednesday"
arDayOrWeek(4) = "Thursday"
arDayOrWeek(5) = "Friday"
arDayOrWeek(6) = "Saturday"

Dim arMonth(13)
arMonth(1) = "January"
arMonth(2) = "Feburary"
arMonth(3) = "March"
arMonth(4) = "April"
arMonth(5) = "May"
arMonth(6) = "June"
arMonth(7) = "July"
arMonth(8) = "August"
arMonth(9) = "September"
arMonth(10) = "October"
arMonth(11) = "November"
arMonth(12) = "December"

strComputer = "."
wmiQuery = "Select * from Win32_TimeZone"
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery(wmiQuery)

For Each objItem in colItems
    WScript.Echo "Day of Week setting is: " _
        & objItem.dayLightDayOfWeek _
        & " which is: " & arDayOrWeek(objItem.DaylightDayOfWeek)
    WScript.Echo "Hour: " & objItem.DaylightHour 
    WScript.Echo "Month: " & objItem.DaylightMonth _
        & " which is: " & arMonth(objItem.DaylightMonth )
    WScript.Echo "Description: " & objItem.DaylightName 
    WScript.Echo "The transition from DLS to Standard occurs: " 
    WScript.Echo "Day of Week setting is: " _
        & objItem.standardDayOfWeek _
        & " which is: " & arDayOrWeek(objItem.DaylightDayOfWeek)
    WScript.Echo "Hour: " & objItem.StandardHour 
    WScript.Echo "Month: " & objItem.StandardMonth _ 
        & " which is: " & arMonth(objItem.StandardMonth )
    WScript.Echo "Description: " & objItem.StandardName 
Next

```



## <a name="requirements"></a><span data-ttu-id="7e20a-337">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e20a-337">Requirements</span></span>



| <span data-ttu-id="7e20a-338">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e20a-338">Requirement</span></span> | <span data-ttu-id="7e20a-339">Wert</span><span class="sxs-lookup"><span data-stu-id="7e20a-339">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e20a-340">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e20a-340">Minimum supported client</span></span><br/> | <span data-ttu-id="7e20a-341">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e20a-341">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7e20a-342">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e20a-342">Minimum supported server</span></span><br/> | <span data-ttu-id="7e20a-343">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e20a-343">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7e20a-344">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e20a-344">Namespace</span></span><br/>                | <span data-ttu-id="7e20a-345">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7e20a-345">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7e20a-346">MOF</span><span class="sxs-lookup"><span data-stu-id="7e20a-346">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e20a-347"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7e20a-347"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e20a-348">DLL</span><span class="sxs-lookup"><span data-stu-id="7e20a-348">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e20a-349"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e20a-349"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e20a-350">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e20a-350">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e20a-351">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="7e20a-351">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="7e20a-352">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="7e20a-352">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="7e20a-353">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="7e20a-353">**SWbemDateTime**</span></span>](../wmisdk/swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="7e20a-354">Datums-und Uhrzeit Format</span><span class="sxs-lookup"><span data-stu-id="7e20a-354">Date and Time Format</span></span>](../wmisdk/date-and-time-format.md)
</dt> <dt>

[<span data-ttu-id="7e20a-355">WMI-Tasks: Datumsangaben und Uhrzeiten</span><span class="sxs-lookup"><span data-stu-id="7e20a-355">WMI Tasks: Dates and Times</span></span>](../wmisdk/wmi-tasks--dates-and-times.md)
</dt> </dl>

 

 
