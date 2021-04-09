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
# <a name="win32_timezone-class"></a>Win32- \_ Zeit Zonen Klasse

Die  [WMI-Klasse](../wmisdk/retrieving-a-class.md) der **Win32- \_ Zeitzone** stellt die Zeitzoneninformationen für ein Computersystem dar, auf dem Windows ausgeführt wird, das die Änderungen beinhaltet, die für den Übergang zur Sommerzeit Umstellung erforderlich sind.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

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

Die **Win32- \_ Zeit Zonen** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ Zeit Zonen** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Verzerrung (Bias)**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Zeitstrukturen \| [**Zeit \_ Zonen \_ Informationen**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| Bias"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Minuten")
</dt> </dl>

Aktuelle Abweichung für die lokale Zeit Übersetzung. Die Verschiebung ist der Unterschied zwischen koordinierter Weltzeit (UTC) und Ortszeit. Alle Übersetzungen zwischen UTC und Ortszeit basieren auf der folgenden Formel: UTC = Local Time-Bias. Diese Eigenschaft ist obligatorisch.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen-Objekts.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**DaylightBias**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("Minutes")
</dt> </dl>

Der für die lokale Zeit Übersetzungen zu verwendende Wert, der während der Sommerzeit auftritt. Diese Eigenschaft wird ignoriert, wenn kein Wert für die **DaylightDay** -Eigenschaft angegeben wird. Der Wert dieser Eigenschaft wird der Eigenschaft " **Bias** " hinzugefügt, um die während der Sommerzeit verwendete Abweichung zu bilden. In den meisten Zeitzonen ist der Wert dieser Eigenschaft-60.

</dd> <dt>

**DaylightDay**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate \| wDay")
</dt> </dl>

**DaylightDayOfWeek** von **DaylightMonth** , wenn die Umstellung von Standardzeit auf Sommerzeit auf diesem Betriebssystem erfolgt.

Beispiel: Wenn der Übergangs Tag (**daylightdayosweek**) an einem Sonntag stattfindet, gibt der Wert "1" den ersten Sonntag des **DaylightMonth** an, "2" gibt den zweiten Sonntag an usw. Der Wert "5" gibt die letzte **daylightdayof-Woche** im Monat an.

</dd> <dt>

**Daylightdayof Week**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate \| wdayof Week")
</dt> </dl>

Der Wochentag, an dem die Umstellung von Standardzeit auf Sommerzeit auf einem Betriebssystem erfolgt.

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

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate \| wHour")
</dt> </dl>

Stunde des Tages, zu der die Umstellung von Standardzeit auf Sommerzeit auf einem Betriebssystem erfolgt.

Beispiel: 2

</dd> <dt>

**Daylightmillisekunde**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate \| wMilliseconds")
</dt> </dl>

Millisekunde von **DaylightSecond** , wenn die Umstellung von Standardzeit auf Sommerzeit in einem Betriebssystem erfolgt.

</dd> <dt>

**DaylightMinute**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate \| wMinute")
</dt> </dl>

Minute von **DaylightHour** , wenn die Umstellung von Standardzeit auf Sommerzeit auf einem Betriebssystem erfolgt.

Beispiel: 59

</dd> <dt>

**DaylightMonth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate \| wMonth")
</dt> </dl>

Monat, in dem die Umstellung von Standardzeit auf Sommerzeit in einem Betriebssystem erfolgt.

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

**DaylightName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightName")
</dt> </dl>

Die Zeitzone, die dargestellt wird, wenn die Sommerzeit wirksam ist.

Beispiel: "EDT" (Eastern Sommerzeit)

</dd> <dt>

**DaylightSecond**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate \| wSecond")
</dt> </dl>

Second von **DaylightMinute** , wenn die Umstellung von Standardzeit auf Sommerzeit in einem Betriebssystem erfolgt.

Beispiel: 59

</dd> <dt>

**DaylightYear**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate \| wYear")
</dt> </dl>

Jahr, wenn die Sommerzeit wirksam ist. Diese Eigenschaft ist nicht erforderlich.

Beispiel: 1997

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des aktuellen-Objekts.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**Standard Bias**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Zeitstrukturen \| [**Zeit \_ Zonen \_ Informationen**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardBias"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Minuten")
</dt> </dl>

Der zu verwendende biaswert, wenn die Sommerzeit nicht wirksam ist. Diese Eigenschaft wird ignoriert, wenn kein Wert für **StandardDay** angegeben wird. Der Wert dieser Eigenschaft wird der Eigenschaft " **Bias** " hinzugefügt, um die Verschiebung während der Standardzeit zu bilden.

Beispiel: 0

</dd> <dt>

**StandardDay**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate \| wDay")
</dt> </dl>

**StandardDayOfWeek** des **StandardMonth** , wenn der Übergang von Sommerzeit zu Normalzeit in einem Betriebssystem erfolgt.

Wenn der Übergangs Tag (**standarddayosweek**) an einem Sonntag stattfindet, gibt der Wert "1" den ersten Sonntag des **StandardMonth** an, "2" den zweiten Sonntag und so weiter. Der Wert "5" gibt die letzte **standarddayof-Woche** im Monat an.

</dd> <dt>

**Standarddayogweek**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**Zeit \_ Zonen \_ Informationen**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate \| wdayof Week")
</dt> </dl>

Der Wochentag, an dem die Umstellung von Sommerzeit auf Standardzeit in einem Betriebssystem erfolgt.

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

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**Zeit \_ Zonen \_ Informationen**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate \| wHour")
</dt> </dl>

Stunde des Tages, zu der die Umstellung von Sommerzeit auf Standardzeit in einem Betriebssystem erfolgt.

Beispiel: 11

</dd> <dt>

**Standardmillisekunde**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Zeitstrukturen \| [**Zeit \_ Zonen \_ Informationen**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate \| wMilliseconds")
</dt> </dl>

Millisekunde der **StandardSecond** , wenn die Umstellung von Sommerzeit auf Standardzeit in einem Betriebssystem erfolgt.

</dd> <dt>

**Standard Minute**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate \| wMinute")
</dt> </dl>

Minute des **StandardDay** , wenn die Umstellung von Sommerzeit auf Standardzeit in einem Betriebssystem erfolgt.

Beispiel: 59

</dd> <dt>

**StandardMonth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate \| wMonth")
</dt> </dl>

Monat, wenn die Umstellung von Sommerzeit auf Standardzeit in einem Betriebssystem erfolgt.

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

**Standardname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| Standardname")
</dt> </dl>

Der Name der Zeitzone, die dargestellt wird, wenn die Standardzeit wirksam ist.

Beispiel: "EST" (Eastern Normalzeit)

</dd> <dt>

**StandardSecond**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate \| wSecond")
</dt> </dl>

Die zweite der **Standard Minuten** , wenn die Umstellung von Sommerzeit auf Normalzeit in einem Betriebssystem erfolgt.

Beispiel: 59

</dd> <dt>

**Standard Jahr**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| time Structures \| [**time \_ Zone \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate \| wYear")
</dt> </dl>

Jahr, in dem die Standardzeit wirksam ist. Diese Eigenschaft ist nicht erforderlich.

Beispiel: 1997

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ Zeit Zonen** Klasse wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.

Beim Schreiben von WMI-Abfragen können Standardformate für Datum/Uhrzeit (z. b. 10/18/2002) nicht verwendet werden. Stattdessen müssen Sie alle Datumsangaben, die in Ihren Abfragen verwendet werden, in das UTC-Format konvertieren. Hierfür sind zwei Schritte erforderlich: 1) Sie müssen den Offset (Differenz in Minuten) zwischen Ihrer Zeitzone und der Ortszeit (Greenwich Mean Time) und 2) bestimmen. Sie müssen 10/18/2002 in einen UTC-Wert konvertieren.

Bestimmen des Offsets von der Greenwich Mean Time

Zugegebenermaßen macht WMI es schwierig, mit Datums-und Uhrzeitwerten zu arbeiten. Glücklicherweise erleichtert WMI das Ermitteln des Offsets zwischen Ihrer Zeitzone und der Ortszeit (Greenwich Mean Time). Die Win32-Zeitzone der WMI \_ -Klasse enthält eine Eigenschaft-Bias, die den GMT-Offset zurückgibt.


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



Wandeln eines Datums in einen UTC-Wert

Nachdem Sie den GMT-Offset festgelegt haben, müssen Sie ein Standard Datum, z. b. 10/18/2002, in ein UTC-Datum konvertieren. Zum Konvertieren eines Standard Datums in ein UTC-Datum können Sie VBScript-Datumsfunktionen wie z. b. Jahr, Monat und Tag verwenden, um die einzelnen Komponenten zu isolieren, die ein UTC-Datum bilden. Nachdem Sie einzelne Werte für diese Komponenten erstellt haben, können Sie Sie auf die gleiche Weise wie andere Zeichen folgen Werte verketten. UTC-Datumsangaben werden als Zeichen folgen behandelt, da der GMT-Offset am Ende angehängt werden muss. Wenn das Datum als Zahl angezeigt wird, lautet dieser Wert:

`20011018113047.000000-480`

Wird fälschlicherweise als mathematische Gleichung behandelt (aus Gründen der Übersichtlichkeit hinzugefügte Klammern):

`(20011018113047.000000) - (480)`

Beispielsweise sind im Datum 10/18/2002 die einzelnen Komponenten wie folgt:

-   Jahr: 2002
-   Monat: 10
-   Tag: 18

Das Skript muss diese drei Werte kombinieren, die Zeichenfolge "113047,000000" (die die Uhrzeit, einschließlich der Millisekunden) und der GMT-Offset zum Ableiten eines UTC-Datums. Z. b. (aus Gründen der Übersichtlichkeit wurden wieder Klammern hinzugefügt):

`(2002) & (10) & (18) & (113047.000000) & (-480)`

> [!Note]  
> Sie können die VBScript-Funktionen "Hour", "Minute" und "Second" verwenden, um den Uhrzeit Teil eines UTC-Datums zu konvertieren. Eine Uhrzeit, z. b. 11:30:47 Uhr würde in 113047 konvertiert werden.

 

Es gibt einen complilikations Faktor. Der Monat muss die Positionen 5 und 6 in der Zeichenfolge belegen. der Tag muss die Positionen 7 und 8 annehmen. Dies ist kein Problem für den Monat 10 und den 18. Tag. Aber wie erhalten Sie den 5. Juli (Monat 7, Tag 5), um die erforderlichen Positionen zu füllen? Die Antwort besteht darin, jedem Wert einen führenden Null-Wert hinzuzufügen und somit 7 in 07 und 5 in 05 zu ändern.

Verwenden Sie hierzu die VBScript-Len-Funktion, um die Länge (Anzahl der Zeichen) im Monat und Tag zu überprüfen. Wenn die Länge 1 beträgt (was bedeutet, dass es nur ein Zeichen gibt), fügen Sie eine führende Null hinzu. Bisher


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



Das folgende VBScript-samplebestimmt den GMT-Offset und konvertiert dann ein angegebenes Aktuelles Datum (in diesem Fall 10/18/2002) in das UTC-Datums-/Uhrzeitformat. Nachdem das Datum konvertiert wurde, wird dieser Wert zum Durchsuchen eines Computers verwendet und gibt eine Liste aller Ordner zurück, die nach 10/18/2002 erstellt wurden.


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



Im folgenden VBScript-Codebeispiel werden die Einstellungen für Win32- \_ Zeit Zonen Instanzen angezeigt.


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
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Einstellung**](cim-setting.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> <dt>

[**Swap-DateTime**](../wmisdk/swbemdatetime.md)
</dt> <dt>

[Datums-und Uhrzeit Format](../wmisdk/date-and-time-format.md)
</dt> <dt>

[WMI-Tasks: Datumsangaben und Uhrzeiten](../wmisdk/wmi-tasks--dates-and-times.md)
</dt> </dl>

 

 
