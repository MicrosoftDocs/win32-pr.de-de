---
description: Die abstrakte Basisklasse für alle konkreten unformatierte Leistungsindikatorklassen.
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
ms.openlocfilehash: f6500706b7e2298ad98aa894e33436b0306e406e003562fcb6533265abd0b2be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020128"
---
# <a name="win32_perfrawdata-class"></a>Win32 \_ PerfRawData-Klasse

Die abstrakte Basisklasse für alle konkreten unformatierte Leistungsindikatorklassen.

Um im Systemmonitor angezeigt zu werden, müssen Dem Cimv2-Stammnamespace Leistungsindikatorklassen hinzugefügt und von \\ **Win32 \_ PerfRawData abgeleitet werden.** Daten in diesen Klassen werden vom Leistungsindikatoranbieter [für hohe Leistung bereitgestellt.](../wmisdk/performance-counter-provider.md)

Die folgenden Eigenschaften werden geerbt, wenn eine Klasse von **Win32 \_ PerfRawData abgeleitet wird:**

-   **Timestamp \_ PerfTime**
-   **\_Zeitstempel Sys100NS**
-   **\_Timestamp-Objekt**
-   **Frequency \_ PerfTime**
-   **Häufigkeit \_ Sys100NS**
-   **\_Frequency-Objekt**

In jedem Fall müssen die Eigenschaften vom Anbieter ausgefüllt werden, oder die Klasse kann nicht im Systemmonitor angezeigt werden. Diese Eigenschaften werden verwendet, um Indikatortypformeln von Kunden von Leistungsdaten zu berechnen.

Die folgende Syntax wird durch MOF-Code vereinfacht und zeigt alle geerbten Eigenschaften an.

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

Die **Win32 \_ PerfRawData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ PerfRawData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Kurze Textbeschreibung für die Statistik oder Metrik.

Diese Eigenschaft wird von [**CIM \_ StatisticalInformation geerbt.**](cim-statisticalinformation.md)

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung der Statistik oder Metrik.

Diese Eigenschaft wird von [**CIM \_ StatisticalInformation geerbt.**](cim-statisticalinformation.md)

</dd> <dt>

**\_Frequency-Objekt**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Häufigkeit in Ticks pro Sekunde der **Timestamp \_ Object-Eigenschaft.** Wenn der Anbieter unterklassig ist, definiert er diese Eigenschaft.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

Diese Eigenschaft wird von [**Win32 \_ Perf geerbt.**](win32-perf.md)

</dd> <dt>

**Frequency \_ PerfTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Häufigkeit in Ticks pro Sekunde der **Frequency \_ PerfTime-Eigenschaft.** Sie können einen Wert erhalten, indem Sie die Windows [**QueryPerformanceCounter aufrufen.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

Diese Eigenschaft wird von [**Win32 \_ Perf geerbt.**](win32-perf.md)

</dd> <dt>

**Häufigkeit \_ Sys100NS**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Häufigkeit in Ticks pro Sekunde der **\_ Timestamp Sys100NS-Eigenschaft** (10000000).

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

Diese Eigenschaft wird von [**Win32 \_ Perf geerbt.**](win32-perf.md)

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Bezeichnung, unter der die Statistik oder Metrik bekannt ist. Bei Unterklassen kann diese Eigenschaft überschrieben werden, um eine Schlüsseleigenschaft zu sein.

Diese Eigenschaft wird von [**CIM \_ StatisticalInformation geerbt.**](cim-statisticalinformation.md)

</dd> <dt>

**\_Timestamp-Objekt**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Objektdefinierter Zeitstempel. Der Anbieter definiert seine Eigenschaft.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

Diese Eigenschaft wird von [**Win32 \_ Perf geerbt.**](win32-perf.md)

</dd> <dt>

**Timestamp \_ PerfTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeitstempel des Leistungsindikators. Sie können einen Wert erhalten, indem Sie die Windows [**QueryPerformanceCounter aufrufen.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

Diese Eigenschaft wird von [**Win32 \_ Perf geerbt.**](win32-perf.md)

</dd> <dt>

**\_Zeitstempel Sys100NS**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeitstempelwert in Einheiten von 100 Nanosekunden.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

Diese Eigenschaft wird von [**Win32 \_ Perf geerbt.**](win32-perf.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ PerfRawData-Klasse** wird von [**Win32 \_ Perf**](win32-perf.md)abgeleitet, das von [**CIM \_ StatisticalInformation abgeleitet wird.**](cim-statisticalinformation.md)

Alle von [**Win32 \_ Perf abgeleiteten**](win32-perf.md) Klassen sind für die Verwendung mit einem [*Aktualisierungsobjekt*](../wmisdk/gloss-r.md) konzipiert. Weitere Informationen zum Erstellen und Verwenden eines Aktualisierungsobjekts in der Programmiersprache C++ finden Sie unter Zugreifen auf [Leistungsdaten in C++.](../wmisdk/accessing-performance-data-in-c--.md) Weitere Informationen zum Erstellen und Verwenden eines Aktualisierungsobjekts in einer Skriptprogrammiersprache finden Sie unter Aktualisieren von [WMI-Daten in Skripts.](../wmisdk/refreshing-wmi-data-in-scripts.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                             |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>WmiPerfInst.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ Perf**](win32-perf.md)
</dt> <dt>

[Leistungsindikatorklassen](performance-counter-classes.md)
</dt> <dt>

[Zugreifen auf vorinstallierte WMI-Leistungsklassen](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[WMI-Aufgaben: Leistungsüberwachung](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Zugreifen auf Leistungsdaten in Skripts](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
