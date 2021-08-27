---
description: Enthält Methoden, die den Rohinhalt der Videoeingabedefinition von 128-Byte-Standarddatenblöcken der Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) v.1.x abrufen.
ms.assetid: c13d4ddd-d171-44d5-9e70-3a6f89ad55da
title: WmiMonitorDescriptorMethods-Klasse
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
ms.openlocfilehash: 7e8fe02540cd68047e3e74c052a8ea833a67d829228979da31bb12e13e84d9f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120960"
---
# <a name="wmimonitordescriptormethods-class"></a>WmiMonitorDescriptorMethods-Klasse

Die WMI-Klasse **WmiMonitorDescriptorMethods** enthält Methoden, die den Rohdateninhalt der 128-Byte-Standarddatenblöcke der Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) v.1.x abrufen.

## <a name="syntax"></a>Syntax

``` syntax
class WmiMonitorDescriptorMethods : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Member

Die **WmiMonitorDescriptorMethods-Klasse** verfügt über folgende Membertypen:

-   [Methoden](#wmimonitordescriptormethods-class)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **WmiMonitorDescriptorMethods-Klasse** verfügt über diese Methoden.



| Methode                                                                                           | Beschreibung                                                                   |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**WmiGetMonitorRawEEdidV1Block**](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md) | Greift auf die Rohdaten für einen angegebenen EDID v.1.x-Deskriptorblock zu.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **WmiMonitorDescriptorMethods-Klasse** verfügt über diese Eigenschaften.

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

 

 




