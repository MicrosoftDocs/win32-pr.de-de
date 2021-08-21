---
description: Die abstrakte Basisklasse für alle konkreten unformatierten Leistungsindikatorklassen.
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

Die abstrakte Basisklasse für alle konkreten unformatierten Leistungsindikatorklassen.

Um im Systemmonitor angezeigt zu werden, müssen Dem Stammnamespace cimv2 Leistungsindikatorklassen hinzugefügt \\ und von **Win32 \_ PerfRawData** abgeleitet werden. Daten in diesen Klassen werden vom [Leistungsindikatoranbieter](../wmisdk/performance-counter-provider.md)für hohe Leistung bereitgestellt.

Die folgenden Eigenschaften werden geerbt, wenn eine Klasse von **Win32 \_ PerfRawData** abgeleitet wird:

-   **Timestamp \_ PerfTime**
-   **Zeitstempel \_ Sys100NS**
-   **\_Timestamp-Objekt**
-   **Frequency \_ PerfTime**
-   **Frequency \_ Sys100NS**
-   **\_Frequency-Objekt**

In jedem Fall müssen die Eigenschaften vom Anbieter ausgefüllt werden, oder die Klasse kann nicht im Systemmonitor angezeigt werden. Diese Eigenschaften werden verwendet, um Indikatortypformeln von Consumern von Leistungsdaten zu berechnen.

Die folgende Syntax wird aus MOF-Code vereinfacht und zeigt alle geerbten Eigenschaften an.

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

Die **Win32 \_ PerfRawData-Klasse** verfügt über folgende Typen von Membern:

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

Diese Eigenschaft wird von [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung der Statistik oder Metrik.

Diese Eigenschaft wird von [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)geerbt.

</dd> <dt>

**\_Frequency-Objekt**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Häufigkeit in Ticks pro Sekunde der **Timestamp \_ Object-Eigenschaft.** Wenn die Unterklasse festgelegt ist, definiert der Anbieter diese Eigenschaft.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

Diese Eigenschaft wird von [**Win32 \_ Perf**](win32-perf.md)geerbt.

</dd> <dt>

**Frequency \_ PerfTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Häufigkeit in Ticks pro Sekunde der **Frequency \_ PerfTime-Eigenschaft.** Ein Wert kann abgerufen werden, indem die Windows Funktion [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)aufgerufen wird.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

Diese Eigenschaft wird von [**Win32 \_ Perf**](win32-perf.md)geerbt.

</dd> <dt>

**Frequency \_ Sys100NS**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Häufigkeit in Ticks pro Sekunde der **Timestamp \_ Sys100NS-Eigenschaft** (100000000).

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

Diese Eigenschaft wird von [**Win32 \_ Perf**](win32-perf.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Bezeichnung, mit der die Statistik oder Metrik bekannt ist. Bei Einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.

Diese Eigenschaft wird von [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)geerbt.

</dd> <dt>

**\_Timestamp-Objekt**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Objektdefinierter Zeitstempel. Der Anbieter definiert seine -Eigenschaft.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

Diese Eigenschaft wird von [**Win32 \_ Perf**](win32-perf.md)geerbt.

</dd> <dt>

**Timestamp \_ PerfTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeitstempel des Leistungsindikators. Ein Wert kann abgerufen werden, indem die Windows Funktion [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)aufgerufen wird.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

Diese Eigenschaft wird von [**Win32 \_ Perf**](win32-perf.md)geerbt.

</dd> <dt>

**Zeitstempel \_ Sys100NS**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Timestamp-Wert in Einheiten von 100 Nanosekunden.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

Diese Eigenschaft wird von [**Win32 \_ Perf**](win32-perf.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ PerfRawData-Klasse** wird von [**Win32 \_ Perf**](win32-perf.md)abgeleitet, das von [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)abgeleitet wird.

Alle von [**Win32 \_ Perf**](win32-perf.md) abgeleiteten Klassen sind für die Verwendung mit einem [*Aktualisierungsobjekt*](../wmisdk/gloss-r.md) konzipiert. Weitere Informationen zum Erstellen und Verwenden eines Aktualisierungsobjekts in der Programmiersprache C++ finden Sie unter [Zugreifen auf Leistungsdaten in C++.](../wmisdk/accessing-performance-data-in-c--.md) Weitere Informationen zum Erstellen und Verwenden eines Aktualisierungsobjekts in einer Skriptprogrammiersprache finden Sie unter [Aktualisieren von WMI-Daten in Skripts.](../wmisdk/refreshing-wmi-data-in-scripts.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                             |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>WmiPerfInst.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

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

 

 
