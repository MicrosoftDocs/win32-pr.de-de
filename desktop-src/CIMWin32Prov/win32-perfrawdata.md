---
description: Die abstrakte Basisklasse für alle konkreten Klassen des-rohleistungs Zählers.
ms.assetid: 3c457996-54d9-4425-8a57-15176d027e3a
ms.tgt_platform: multiple
title: Win32_PerfRawData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfRawData
- Win32_PerfRawData.Caption
- Win32_PerfRawData.Description
- Win32_PerfRawData.Name
- Win32_PerfRawData.Frequency_Object
- Win32_PerfRawData.Frequency_PerfTime
- Win32_PerfRawData.Frequency_Sys100NS
- Win32_PerfRawData.Timestamp_Object
- Win32_PerfRawData.Timestamp_PerfTime
- Win32_PerfRawData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: db5b74ae7508d15a48d2f71c3a586ad7e40362f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524272"
---
# <a name="win32_perfrawdata-class"></a>Win32 \_ perfrawdata-Klasse

Die abstrakte Basisklasse für alle konkreten Klassen des-rohleistungs Zählers.

Um im System Monitor angezeigt zu werden, müssen Leistungsindikatoren Klassen zum Stamm \\ CIMV2-Namespace hinzugefügt und von **Win32 \_ perfrawdata** abgeleitet werden. Die Daten in diesen Klassen werden vom Hochleistungs [Anbieter für Leistungs Anbieter](../wmisdk/performance-counter-provider.md)bereitgestellt.

Die folgenden Eigenschaften werden geerbt, wenn eine Klasse von **Win32 \_ perfrawdata** abgeleitet wird:

-   **Zeitstempel ( \_ PerfTime)**
-   **Zeitstempel \_ Sys100NS**
-   **Timestamp- \_ Objekt**
-   **\_PerfTime-Häufigkeit**
-   **Frequency \_ Sys100NS**
-   **Frequency- \_ Objekt**

In jedem Fall müssen die Eigenschaften vom Anbieter ausgefüllt werden, oder die Klasse kann nicht im System Monitor angezeigt werden. Diese Eigenschaften werden zum Berechnen von Counter-typformeln durch Consumer von Leistungsdaten verwendet.

Die folgende Syntax wird aus dem MOF-Code vereinfacht und zeigt alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[abstract, AMENDMENT]
class Win32_PerfRawData : Win32_Perf
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

Die **Win32 \_ perfrawdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ perfrawdata** -Klasse verfügt über diese Eigenschaften.

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

Die **Win32 \_ perfrawdata** -Klasse wird von [**Win32- \_ perf**](win32-perf.md)abgeleitet, die von [**CIM \_ statisticalinformation**](cim-statisticalinformation.md)abgeleitet ist.

Alle Klassen, die von [**Win32 \_ perf**](win32-perf.md) abgeleitet werden, sind für die Verwendung [*mit einem*](../wmisdk/gloss-r.md) Aktualisierungs Objekt konzipiert. Weitere Informationen zum Erstellen und Verwenden eines Aktualisierungs Objekts in der Programmiersprache C++ finden Sie unter [zugreifen auf Leistungsdaten in C++](../wmisdk/accessing-performance-data-in-c--.md). Weitere Informationen zum Erstellen und Verwenden eines Aktualisierungs Objekts in einer Skript Programmiersprache finden Sie unter Aktualisieren von [WMI-Daten in](../wmisdk/refreshing-wmi-data-in-scripts.md)Skripts.

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

 

 
