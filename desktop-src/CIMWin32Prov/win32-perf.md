---
description: Die Basisklasse für die Leistungsindikatorklassen Win32 \_ PerfRawData und Win32 \_ PerfFormattedData.
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
ms.openlocfilehash: 356fdba0e2ebb7fb202f4996daa6b1929cd61fc67b028f67e8b041748306c0ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972240"
---
# <a name="win32_perf-class"></a>Win32 \_ Perf-Klasse

Die Basisklasse für die Leistungsindikatorklassen [**Win32 \_ PerfRawData**](win32-perfrawdata.md) und [**Win32 \_ PerfFormattedData.**](win32-perfformatteddata.md)

**Win32 \_ Perf** definiert die erforderlichen Zeitstempel- und Häufigkeitseigenschaften, die in [**den CounterType-Algorithmen**](../wmisdk/countertype-qualifier.md) für die Leistungsindikatorklassen verwendet werden.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

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

Die **Win32 \_ Perf-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ Perf-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
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

Datentyp: **Zeichenfolge**
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

</dd> <dt>

**Frequency \_ PerfTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Häufigkeit in Ticks pro Sekunde der **Frequency \_ PerfTime-Eigenschaft.** Sie können einen Wert erhalten, indem Sie die Windows [**QueryPerformanceCounter aufrufen.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**Häufigkeit \_ Sys100NS**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Häufigkeit in Ticks pro Sekunde der **\_ Timestamp Sys100NS-Eigenschaft** (10000000).

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
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

</dd> <dt>

**Timestamp \_ PerfTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeitstempel des Leistungsindikators. Sie können einen Wert erhalten, indem Sie die Windows [**QueryPerformanceCounter aufrufen.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**\_Zeitstempel Sys100NS**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeitstempelwert in Einheiten von 100 Nanosekunden.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ Perf-Klasse** wird von [**CIM \_ StatisticalInformation ableiten.**](cim-statisticalinformation.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                             |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                     |
| DLL<br/>                      | <dl> <dt>WmiPerfInst.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)
</dt> <dt>

[Leistungsindikatorklassen](performance-counter-classes.md)
</dt> <dt>

[Zugreifen auf vorinstallierte WMI-Leistungsklassen](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[WMI-Aufgaben: Leistungsüberwachung](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Zugreifen auf Leistungsdaten in Skripts](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
