---
description: Listet die vom Monitor unterstützten Häufigkeitsbereiche auf.
ms.assetid: e4713650-5f8c-4808-8b4f-1d29c54ab4e3
title: WmiMonitorListedFrequencyRanges-Klasse
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
ms.openlocfilehash: 41b49c293d5661d523138b01c093fce627e5bedf3d1e783dccb8248edf88546c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051138"
---
# <a name="wmimonitorlistedfrequencyranges-class"></a>WmiMonitorListedFrequencyRanges-Klasse

Die WMI-Klasse **WMI WmiMonitorListedFrequencyRanges** listet die vom Monitor unterstützten Frequenzbereiche auf. Diese Bereiche befinden sich im Block Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) oder in der Windows INF-Datei, die Gerätetreiberdaten enthält.

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

Die **WmiMonitorListedFrequencyRanges-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **WmiMonitorListedFrequencyRanges-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den aktiven Monitor an.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Name der spezifischen Überwachungsinstanz.

</dd> <dt>

**MonitorFreqRanges**
</dt> <dd> <dl> <dt>

Datentyp: **FrequencyRangeDescriptor-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Liste der Überwachungshäufigkeitsbereiche, die durch Instanzen der [**FrequencyRangeDescriptor-Klasse**](frequencyrangedescriptor.md) dargestellt werden.

</dd> <dt>

**NumOfMonitorFreqRanges**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der aufgeführten unterstützten Überwachungshäufigkeitsbereiche.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | Root \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




