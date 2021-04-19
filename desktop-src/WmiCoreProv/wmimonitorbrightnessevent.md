---
description: Stellt eine Änderung der Helligkeit eines Monitors dar.
ms.assetid: c2eb5630-a52f-4ad4-aaee-1cc8afef8c9e
title: Wmimonitorbrightnessvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessEvent
- WmiMonitorBrightnessEvent.Active
- WmiMonitorBrightnessEvent.Brightness
- WmiMonitorBrightnessEvent.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 7e53f90627c959db0140b01cf3b3d385afcc6e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349583"
---
# <a name="wmimonitorbrightnessevent-class"></a>Wmimonitorbrightnessvent-Klasse

Die **wmimonitorbrightnesgvent** WMI-Ereignisklasse stellt eine Änderung der Helligkeit eines Monitors dar.

## <a name="syntax"></a>Syntax

``` syntax
class WmiMonitorBrightnessEvent : WMIEvent
{
  boolean Active;
  uint8   Brightness;
  string  InstanceName;
};
```

## <a name="members"></a>Member

Die **wmimonitorbrightnestarvent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **wmimonitorbrightnessvent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den aktiven Monitor an.

</dd> <dt>

**Helligkeit**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aktuelle Monitor Helligkeit als Prozentsatz.

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
</dt> <dt>

[**Wmimonitorhelligkeit**](wmimonitorbrightness.md)
</dt> <dt>

[Empfangen eines WMI-Ereignisses](/windows/desktop/WmiSdk/receiving-a-wmi-event)
</dt> </dl>

 

