---
description: Listet die vom Monitor unterstützten Häufigkeits Bereiche auf.
ms.assetid: e4713650-5f8c-4808-8b4f-1d29c54ab4e3
title: Wmimonitorlistedfrequencyranges-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedFrequencyRanges
- WmiMonitorListedFrequencyRanges.Active
- WmiMonitorListedFrequencyRanges.InstanceName
- WmiMonitorListedFrequencyRanges.NumOfMonitorFreqRanges
- WmiMonitorListedFrequencyRanges.MonitorFreqRanges
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e13828f6d5e844147fc0b041617c8452c503ceef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357862"
---
# <a name="wmimonitorlistedfrequencyranges-class"></a>Wmimonitorlistedfrequencyranges-Klasse

Die WMI-Klasse **wmimonitorlistedfrequencyranges** listet die vom Monitor unterstützten Häufigkeits Bereiche auf. Diese Bereiche finden Sie in der Videoeingabe Definition von "velectronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) Block" oder in der Windows INF-Datei, die Gerätetreiber Daten enthält.

## <a name="syntax"></a>Syntax

``` syntax
class WmiMonitorListedFrequencyRanges : MSMonitorClass
{
  boolean                  Active;
  string                   InstanceName;
  uint16                   NumOfMonitorFreqRanges;
  FrequencyRangeDescriptor MonitorFreqRanges[];
};
```

## <a name="members"></a>Member

Die **wmimonitorlistedfrequencyranges** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **wmimonitorlistedfrequencyranges** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den aktiven Monitor an.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Der Name der spezifischen Monitor Instanz.

</dd> <dt>

**Monitorfreqranges**
</dt> <dd> <dl> <dt>

Datentyp: **frequencyrangedescriptor** -Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Liste der Monitor Häufigkeits Bereiche, die durch Instanzen der [**frequencyrangedescriptor**](frequencyrangedescriptor.md) -Klasse dargestellt werden.

</dd> <dt>

**Numuf-monitorfreqranges**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der aufgeführten unterstützten Monitor Häufigkeits Bereiche.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | WMI-Stammdatei \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WMI Core. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




