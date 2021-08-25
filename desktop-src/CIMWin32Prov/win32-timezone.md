---
description: Win32 \_ TimeZone&\# 8194; Die WMI-Klasse stellt die Zeitzoneninformationen für ein Computersystem dar, auf dem Windows ausgeführt wird, einschließlich der Änderungen, die für den Übergang zur Sommerzeit erforderlich sind.
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
ms.openlocfilehash: 02b6d9d5c6100a652cf50096f5ef513fc164cfcfd2d8036e8444adc702459d1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827660"
---
# <a name="win32_timezone-class"></a>Win32 \_ TimeZone-Klasse

Die  [WMI-Klasse](../wmisdk/retrieving-a-class.md) **Win32 \_ TimeZone** stellt die Zeitzoneninformationen für ein Computersystem dar, auf dem Windows ausgeführt wird, einschließlich der Änderungen, die für den Übergang zur Sommerzeit erforderlich sind.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge sortiert.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **Win32 \_ TimeZone-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TimeZone-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Verzerrung (Bias)**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Zeitstrukturen \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| Bias"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Minuten")
</dt> </dl>

Aktuelle Verschiebung für die Ortszeitübersetzung. Die Verschiebung ist der Unterschied zwischen koordinierte Weltzeit (UTC) und Ortszeit. Alle Übersetzungen zwischen UTC und Ortszeit basieren auf der folgenden Formel: UTC = Ortszeit – Verschiebung. Diese Eigenschaft ist erforderlich.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen Objekts.

Diese Eigenschaft wird von [**cim \_ setting**](cim-setting.md)geerbt.

</dd> <dt>

**DaylightBias**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Zeitstrukturen \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightBias"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Minuten")
</dt> </dl>

Verschiebungswert, der während Ortszeitübersetzungen verwendet werden soll, die während der Sommerzeit auftreten. Diese Eigenschaft wird ignoriert, wenn kein Wert für die **DaylightDay-Eigenschaft** angegeben wird. Der Wert dieser Eigenschaft wird der **Bias-Eigenschaft** hinzugefügt, um die Verzerrung zu bilden, die während der Sommerzeit verwendet wird. In den meisten Zeitzonen ist der Wert dieser Eigenschaft -60.

</dd> <dt>

**DaylightDay**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Zeitstrukturen \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wDay")
</dt> </dl>

**DaylightDayOfWeek** des **DaylightMonth,** wenn der Übergang von der Standardzeit zur Sommerzeit in diesem Betriebssystem erfolgt.

Beispiel: Wenn der Übergangstag (**DaylightDayOfWeek**) an einem Sonntag auftritt, gibt der Wert "1" den ersten Sonntag des **DaylightMonth** an, "2" den zweiten Sonntag usw. Der Wert "5" gibt den letzten **DaylightDayOfWeek** im Monat an.

</dd> <dt>

**DaylightDayOfWeek**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Zeitstrukturen \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wDayOfWeek")
</dt> </dl>

Wochentag, an dem der Übergang von der Standardzeit zur Sommerzeit auf einem Betriebssystem erfolgt.

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Sonntag** (0)


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Montag** (1)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Dienstag** (2)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Mittwoch** (3)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Donnerstag** (4)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Freitag** (5)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Samstag** (6)


</dt> <dd></dd> </dl>

Beispiel: 1

</dd> <dt>

**DaylightHour**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Zeitstrukturen \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wHour")
</dt> </dl>

Stunde des Tages, in der der Übergang von der Normalzeit zur Sommerzeit auf einem Betriebssystem erfolgt.

Beispiel: 2

</dd> <dt>

**DaylightMillisecond**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Zeitstrukturen \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMilliseconds")
</dt> </dl>

Millisekunde von **DaylightSecond,** wenn der Übergang von der Standardzeit zur Sommerzeit in einem Betriebssystem erfolgt.

</dd> <dt>

**DaylightMinute**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Zeitstrukturen \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMinute")
</dt> </dl>

Minute des **DaylightHour-Ausdrucks,** wenn der Übergang von der Normalzeit zur Sommerzeit auf einem Betriebssystem erfolgt.

Beispiel: 59

</dd> <dt>

**DaylightMonth**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Zeitstrukturen \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMonth")
</dt> </dl>

Monat, in dem der Übergang von der Standardzeit zur Sommerzeit auf einem Betriebssystem erfolgt.

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

**Januar** (1)


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**Februar** (2)


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

**März** (3)


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**April** (4)


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

**Mai** (5)


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

**Juni** (6)


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

**Juli** (7)


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

**August** (8)


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

**September** (9)


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

**Oktober** (10)


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

**November** (11)


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

**Dezember** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**Daylightname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Zeitstrukturen \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightName")
</dt> </dl>

Die Zeitzone wird dargestellt, wenn die Sommerzeit wirksam ist.

Beispiel: "EDT" (Eastern Daylight Time)

</dd> <dt>

**DaylightSecond**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Zeitstrukturen \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wSecond")
</dt> </dl>

Zweite von **DaylightMinute,** wenn der Übergang von der Standardzeit zur Sommerzeit auf einem Betriebssystem erfolgt.

Beispiel: 59

</dd> <dt>

**DaylightYear**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Zeitstrukturen \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wYear")
</dt> </dl>

Jahr, in dem die Sommerzeit wirksam ist. Diese Eigenschaft ist nicht erforderlich.

Beispiel: 1997

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des aktuellen -Objekts.

Diese Eigenschaft wird von [**cim \_ setting**](cim-setting.md)geerbt.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Bezeichner, durch den das aktuelle Objekt bekannt ist.

Diese Eigenschaft wird von [**cim \_ setting**](cim-setting.md)geerbt.

</dd> <dt>

**StandardBias**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Zeitstrukturen \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardBias"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Minuten")
</dt> </dl>

Verzerrungswert, der verwendet werden soll, wenn die Sommerzeit nicht wirksam ist. Diese Eigenschaft wird ignoriert, wenn kein Wert für **StandardDay** angegeben wird. Der Wert dieser Eigenschaft wird der **Bias-Eigenschaft** hinzugefügt, um die Verschiebung während der Standardzeit zu bilden.

Beispiel: 0

</dd> <dt>

**StandardDay**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Zeitstrukturen \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wDay")
</dt> </dl>

**StandardDayOfWeek** des **StandardMonth,** wenn der Übergang von Sommerzeit zu Normalzeit in einem Betriebssystem erfolgt.

Wenn der Übergangstag (**StandardDayOfWeek**) an einem Sonntag auftritt, gibt der Wert "1" den ersten Sonntag des **StandardMonth** an, "2" den zweiten Sonntag usw. Der Wert "5" gibt den letzten **StandardDayOfWeek** im Monat an.

</dd> <dt>

**StandardDayOfWeek**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Zeitstrukturen \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wDayOfWeek")
</dt> </dl>

Wochentag, an dem der Übergang von sommerzeit zu Normalzeit in einem Betriebssystem erfolgt.

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Sonntag** (0)


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Montag** (1)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Dienstag** (2)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Mittwoch** (3)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Donnerstag** (4)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Freitag** (5)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Samstag** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**StandardHour**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Zeitstrukturen \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wHour")
</dt> </dl>

Stunde des Tages, in der der Übergang von der Sommerzeit zur Normalzeit auf einem Betriebssystem erfolgt.

Beispiel: 11

</dd> <dt>

**StandardMillisecond**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Zeitstrukturen \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMilliseconds")
</dt> </dl>

Millisekunde von **StandardSecond,** wenn der Übergang von Sommerzeit zu Normalzeit in einem Betriebssystem erfolgt.

</dd> <dt>

**StandardMinute**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Zeitstrukturen \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMinute")
</dt> </dl>

Minute von **StandardDay,** wenn der Übergang von Sommerzeit zu Normalzeit in einem Betriebssystem erfolgt.

Beispiel: 59

</dd> <dt>

**StandardMonth**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Zeitstrukturen \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMonth")
</dt> </dl>

Monat, in dem der Übergang von Sommerzeit zu Normalzeit unter einem Betriebssystem erfolgt.

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

**Januar** (1)


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**Februar** (2)


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

**März** (3)


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**April** (4)


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

**Mai** (5)


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

**Juni** (6)


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

**Juli** (7)


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

**August** (8)


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

**September** (9)


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

**Oktober** (10)


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

**November** (11)


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

**Dezember** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**StandardName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardName")
</dt> </dl>

Name der Zeitzone, die dargestellt wird, wenn die Standardzeit wirksam ist.

Beispiel: "EST" (Eastern Standard Time)

</dd> <dt>

**StandardSecond**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Zeitstrukturen \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wSecond")
</dt> </dl>

Zweite **standardMinute,** wenn der Übergang von Sommerzeit zu Normalzeit auf einem Betriebssystem erfolgt.

Beispiel: 59

</dd> <dt>

**StandardYear**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Zeitstrukturen \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wYear")
</dt> </dl>

Jahr, in dem die Standardzeit in Kraft ist. Diese Eigenschaft ist nicht erforderlich.

Beispiel: 1997

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ TimeZone-Klasse** wird von [**der \_ CIM-Einstellung**](cim-setting.md)abgeleitet.

Sie können beim Schreiben von WMI-Abfragen keine Standardformate für Datum und Uhrzeit verwenden , z. B. 18.10.2002. Stattdessen müssen Sie alle Datumsangaben, die in Ihren Abfragen verwendet werden, in das UTC-Format konvertieren. Dies erfordert zwei Schritte: 1) Sie müssen den Offset (Unterschied in Minuten) zwischen Ihrer Zeitzone und Greenwich Mean Time bestimmen, und 2) Sie müssen den 18.10.2002 in einen UTC-Wert konvertieren.

Bestimmen des Offsets von Greenwich Mean Time

Mit WMI ist es natürlich schwierig, mit Datums- und Zeitangaben zu arbeiten. Glücklicherweise erleichtert WMI zumindest die Bestimmung des Offsets zwischen Ihrer Zeitzone und Greenwich Mean Time. Die WMI-Klasse Win32 TimeZone enthält die Eigenschaft \_ Bias, die den GMT-Offset zurückgibt.


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



Konvertieren eines Datums in einen UTC-Wert

Nachdem Sie den GMT-Offset ermittelt haben, müssen Sie ein Standarddatum wie den 18.10.2002 in ein UTC-Datum konvertieren. Um ein Standarddatum in ein UTC-Datum zu konvertieren, können Sie VBScript-Datumsfunktionen wie Jahr, Monat und Tag verwenden, um die einzelnen Komponenten zu isolieren, aus denen ein UTC-Datum besteht. Nachdem Sie über einzelne Werte für diese Komponenten verfügen, können Sie sie auf die gleiche Weise verketten wie andere Zeichenfolgenwerte. UTC-Datumsangaben werden als Zeichenfolgen behandelt, da der GMT-Offset an das Ende angefügt werden muss. Wenn das Datum als Zahl gesehen wurde, gilt dieser Wert:

`20011018113047.000000-480`

Wird fälschlicherweise als mathematische Gleichung behandelt (aus Gründen der Übersichtlichkeit werden Klammern hinzugefügt):

`(20011018113047.000000) - (480)`

Beispielsweise sind die einzelnen Komponenten am 18.10.2002:

-   Jahr: 2002
-   Monat: 10
-   Tag: 18

Das Skript muss diese drei Werte kombinieren: die Zeichenfolge "113047.000000" (die die Uhrzeit darstellt, einschließlich Millisekunden) und den GMT-Offset, um ein UTC-Datum zu leiten. Beispiel: (Aus Gründen der Übersichtlichkeit wurden erneut Klammern hinzugefügt):

`(2002) & (10) & (18) & (113047.000000) & (-480)`

> [!Note]  
> Sie können die VBScript-Funktionen Hour, Minute und Second verwenden, um den Zeitteil eines UTC-Datums zu konvertieren. Daher ein Zeitpunkt wie 11:30:47 Uhr wird in 113047.

 

Es gibt einen erschwerenden Faktor. Der Monat muss die Positionen 5 und 6 in der Zeichenfolge übernehmen. der Tag muss die Positionen 7 und 8 übernehmen. Dies ist kein Problem mit Monat 10 und Tag 18. Aber wie erhalten Sie den 5. Juli (Monat 7, Tag 5), um die erforderlichen Positionen zu füllen? Die Antwort besteht im Hinzufügen einer führenden Null zu jedem Wert, wodurch die Werte 7 in 07 und 5 in 05 geändert werden.

Verwenden Sie hierzu die VBScript-Len-Funktion, um die Länge (Anzahl der Zeichen) im Monat und tag zu überprüfen. Wenn die Länge 1 beträgt (d. h., es gibt nur ein Zeichen), fügen Sie eine führende Null hinzu. So:


```VB
If Len(dtmMonth) = 1 Then
    dtmMonth = "0" & dtmMonth
End If
```



## <a name="examples"></a>Beispiele

Im folgenden VBScript-Beispiel wird das aktuelle Datum in ein UTC-Datum konvertiert.


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



Das folgende VBScript-Beispiel bestimmt den GMT-Offset und konvertiert dann ein angegebenes aktuelles Datum (in diesem Fall 18.10.2002) in das UTC-Datums-/Uhrzeitformat. Nachdem das Datum konvertiert wurde, wird dieser Wert zum Durchsuchen eines Computers verwendet und gibt eine Liste aller Ordner zurück, die nach dem 18.10.2002 erstellt wurden.


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



Im folgenden VBScript-Codebeispiel werden die Einstellungen für Win32 \_ TimeZone-Instanzen angezeigt.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Einstellung**](cim-setting.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> <dt>

[**SWbemDateTime**](../wmisdk/swbemdatetime.md)
</dt> <dt>

[Datums- und Uhrzeitformat](../wmisdk/date-and-time-format.md)
</dt> <dt>

[WMI-Aufgaben: Datums- und Zeitangaben](../wmisdk/wmi-tasks--dates-and-times.md)
</dt> </dl>

 

 
