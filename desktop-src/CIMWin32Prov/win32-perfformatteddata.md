---
description: Eine abstrakte Basisklasse für die vorinstallierten, berechneten Daten Klassen.
ms.assetid: 4eb6ad42-0f68-44f4-be19-095c51b4b1b6
ms.tgt_platform: multiple
title: Win32_PerfFormattedData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfFormattedData
- Win32_PerfFormattedData.Caption
- Win32_PerfFormattedData.Description
- Win32_PerfFormattedData.Name
- Win32_PerfFormattedData.Frequency_Object
- Win32_PerfFormattedData.Frequency_PerfTime
- Win32_PerfFormattedData.Frequency_Sys100NS
- Win32_PerfFormattedData.Timestamp_Object
- Win32_PerfFormattedData.Timestamp_PerfTime
- Win32_PerfFormattedData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: c28d0366c80e8838b36e17cd0fa1074b6ad33629
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958538"
---
# <a name="win32_perfformatteddata-class"></a>Win32 \_ perfformatteddata-Klasse

Eine abstrakte Basisklasse für die vorinstallierten, berechneten Daten Klassen. Ein Beispiel für eine solche Klasse ist [**Win32 \_ perfformatteddata \_ perfdisk \_ LogicalDisk**](../wmisdk/retrieving-raw-and-formatted-performance-data.md). Diese Klassen enthalten berechnete Werte, die durch die [Leistungs Datenanbieter leistungsstarke formatierte Leistungs](../wmisdk/formatted-performance-data-provider.md)bereitgestellt werden.

Die folgende Syntax wird aus dem MOF-Code vereinfacht und zeigt alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[abstract, AMENDMENT]
class Win32_PerfFormattedData : Win32_Perf
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

Die **Win32 \_ perfformatteddata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ perfformatteddata** -Klasse verfügt über diese Eigenschaften.

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

Diese Eigenschaft wird von [**Win32 \_ perf**](win32-perf.md)geerbt.

</dd> <dt>

**\_PerfTime-Häufigkeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Häufigkeit in Ticks pro Sekunde der Eigenschaft " **Frequency \_ PerfTime** ". Ein Wert kann durch Aufrufen der Windows-Funktion " [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)" abgerufen werden.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Diese Eigenschaft wird von [**Win32 \_ perf**](win32-perf.md)geerbt.

</dd> <dt>

**Frequency \_ Sys100NS**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Häufigkeit in Ticks pro Sekunde der **timestamp \_ Sys100NS** -Eigenschaft (10 Millionen).

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Diese Eigenschaft wird von [**Win32 \_ perf**](win32-perf.md)geerbt.

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

Diese Eigenschaft wird von [**Win32 \_ perf**](win32-perf.md)geerbt.

</dd> <dt>

**Zeitstempel ( \_ PerfTime)**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Hoher Leistungszeit Stempel-Zeitstempel. Ein Wert kann durch Aufrufen der Windows-Funktion " [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)" abgerufen werden.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Diese Eigenschaft wird von [**Win32 \_ perf**](win32-perf.md)geerbt.

</dd> <dt>

**Zeitstempel \_ Sys100NS**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Timestamp-Wert in 100 Nanosekunden-Einheiten.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Diese Eigenschaft wird von [**Win32 \_ perf**](win32-perf.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32-Klasse \_ perfformatteddata** ist von [**Win32 \_ perf**](win32-perf.md)abgeleitet, das von [**CIM \_ statisticalinformation**](cim-statisticalinformation.md)abgeleitet ist. Die-Klasse befindet sich im **root \\ CIMV2** -Namespace.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                             |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>WmiPerfInst.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ -Leistung**](win32-perf.md)
</dt> <dt>

[Leistungs Leistungsdaten-Klassen](performance-counter-classes.md)
</dt> <dt>

[Zugreifen auf vorinstallierte WMI-Leistungsklassen](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[WMI-Tasks: Leistungsüberwachung](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Zugreifen auf Leistungsdaten im Skript](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
