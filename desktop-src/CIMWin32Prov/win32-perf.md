---
description: Die Basisklasse für die Leistungs Zählers-Klassen Win32 \_ perfrawdata und Win32 \_ perfformatteddata.
ms.assetid: c754b619-a70f-4a56-8a43-2b36c8f8370b
ms.tgt_platform: multiple
title: Win32_Perf-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Perf
- Root\CIMV2.Win32_Perf.Caption
- Root\CIMV2.Win32_Perf.Description
- Root\CIMV2.Win32_Perf.Name
- Root\CIMV2.Win32_Perf.Frequency_Object
- Root\CIMV2.Win32_Perf.Frequency_PerfTime
- Root\CIMV2.Win32_Perf.Frequency_Sys100NS
- Root\CIMV2.Win32_Perf.Timestamp_Object
- Root\CIMV2.Win32_Perf.Timestamp_PerfTime
- Root\CIMV2.Win32_Perf.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: 13b339e95e175e4d2dff50c0a9674f8002933c1a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344221"
---
# <a name="win32_perf-class"></a>Win32- \_ perf-Klasse

Die Basisklasse für die Leistungs Zählers-Klassen [**Win32 \_ perfrawdata**](win32-perfrawdata.md) und [**Win32 \_ perfformatteddata**](win32-perfformatteddata.md).

**Win32 \_ Perf** definiert die erforderlichen Zeitstempel-und Häufigkeits Eigenschaften, die in den [**CounterType**](../wmisdk/countertype-qualifier.md) -Algorithmen für die Leistungsindikator Klassen verwendet werden.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[abstract, AMENDMENT]
class Win32_Perf : CIM_StatisticalInformation
{
  string Caption;
  string Description;
  string Name;
  uint64 Frequency_Object;
  uint64 Frequency_PerfTime;
  uint64 Frequency_Sys100NS;
  uint64 Timestamp_Object;
  uint64 Timestamp_PerfTime;
  uint64 Timestamp_Sys100NS;
};
```

## <a name="members"></a>Member

Die **Win32- \_ perf** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ perf** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Kurze Textbeschreibung für die Statistik oder Metrik.

Diese Eigenschaft wird von [**CIM \_ statisticalinformation**](cim-statisticalinformation.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Textbeschreibung der Statistik oder Metrik.

Diese Eigenschaft wird von [**CIM \_ statisticalinformation**](cim-statisticalinformation.md)geerbt.

</dd> <dt>

**Frequency- \_ Objekt**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Häufigkeit in Ticks pro Sekunde der **timestamp- \_ Objekt** Eigenschaft. Bei einer untergeordneten Definition definiert der Anbieter diese Eigenschaft.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_PerfTime-Häufigkeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Häufigkeit in Ticks pro Sekunde der Eigenschaft " **Frequency \_ PerfTime** ". Ein Wert kann durch Aufrufen der Windows-Funktion " [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)" abgerufen werden.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Frequency \_ Sys100NS**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Häufigkeit in Ticks pro Sekunde der **timestamp \_ Sys100NS** -Eigenschaft (10 Millionen).

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Bezeichnung, nach der die Statistik oder Metrik bekannt ist. Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.

Diese Eigenschaft wird von [**CIM \_ statisticalinformation**](cim-statisticalinformation.md)geerbt.

</dd> <dt>

**Timestamp- \_ Objekt**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Objekt definierter Zeitstempel. Der Anbieter definiert seine-Eigenschaft.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Zeitstempel ( \_ PerfTime)**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Hoher Leistungszeit Stempel-Zeitstempel. Ein Wert kann durch Aufrufen der Windows-Funktion " [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)" abgerufen werden.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Zeitstempel \_ Sys100NS**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Timestamp-Wert in 100 Nanosekunden-Einheiten.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ perf** -Klasse wird von [**CIM \_ statisticalinformation**](cim-statisticalinformation.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                             |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                     |
| DLL<br/>                      | <dl> <dt>WmiPerfInst.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ statisticalinformation**](cim-statisticalinformation.md)
</dt> <dt>

[Leistungs Leistungsdaten-Klassen](performance-counter-classes.md)
</dt> <dt>

[Zugreifen auf vorinstallierte WMI-Leistungsklassen](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[WMI-Tasks: Leistungsüberwachung](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Zugreifen auf Leistungsdaten im Skript](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
