---
description: Enthält Methoden, die den unformatierten Inhalt der Videoeingabe Definition von (VESA) erweiterten erweiterten Display Identification Data (E-EDID) v. 1. x-Standard-128-Byte-Datenblöcken abrufen.
ms.assetid: c13d4ddd-d171-44d5-9e70-3a6f89ad55da
title: Wmimonitordescriptormethods-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods
- WmiMonitorDescriptorMethods.Active
- WmiMonitorDescriptorMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 578c08c48ada4859b69e00655c5eea8c075515fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359207"
---
# <a name="wmimonitordescriptormethods-class"></a>Wmimonitordescriptormethods-Klasse

Die **wmimonitordescriptormethods** -WMI-Klasse enthält Methoden, die den unformatierten Inhalt der Videoeingabe Definition von (VESA) erweiterten erweiterten Display Identification Data (E-EDID) v. 1. x-Standard-128-Byte-Datenblöcken abrufen.

## <a name="syntax"></a>Syntax

``` syntax
class WmiMonitorDescriptorMethods : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Member

Die **wmimonitordescriptormethods** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#wmimonitordescriptormethods-class)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **wmimonitordescriptormethods** -Klasse verfügt über diese Methoden.



| Methode                                                                                           | BESCHREIBUNG                                                                   |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**WmiGetMonitorRawEEdidV1Block**](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md) | Greift auf die Rohdaten für einen angegebenen EDID v. 1. x-deskriptorblock zu.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **wmimonitordescriptormethods** -Klasse verfügt über diese Eigenschaften.

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

 

 




