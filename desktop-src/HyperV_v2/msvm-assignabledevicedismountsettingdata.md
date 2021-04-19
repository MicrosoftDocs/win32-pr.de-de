---
description: Stellt die Einstellungen eines zu importierenden virtuellen Systems dar. Wird von der Methode zum Aufheben der Einbindung der MSVM-Klasse "Zustell barkeit" verwendet \_ .
ms.assetid: 49892e21-3e8d-4644-8cde-72966927f350
title: Msvm_AssignableDeviceDismountSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceDismountSettingData
- Msvm_AssignableDeviceDismountSettingData.DeviceInstancePath
- Msvm_AssignableDeviceDismountSettingData.DeviceLocationPath
- Msvm_AssignableDeviceDismountSettingData.RequireAcsSupport
- Msvm_AssignableDeviceDismountSettingData.RequireDeviceMitigations
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c5783ed9611c16d875211f29d364fe3eaff29b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364041"
---
# <a name="msvm_assignabledevicedismountsettingdata-class"></a>MSVM zugewiesen \_ abledevicedismountsettingdata-Klasse

Stellt die Einstellungen eines zu importierenden virtuellen Systems dar. Wird von der [**Methode zum Aufheben der Einbindung**](msvm-assignabledeviceservice-dismountassignabledevice.md) der [**MSVM-Klasse " \_ Zustell barkeit**](msvm-assignabledeviceservice.md) " verwendet.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class Msvm_AssignableDeviceDismountSettingData : CIM_SettingData
{
  string  DeviceInstancePath;
  string  DeviceLocationPath;
  boolean RequireAcsSupport;
  boolean RequireDeviceMitigations;
};
```

## <a name="members"></a>Member

Die **MSVM \_** -Klasse "zuder Klasse" weist die folgenden Member auf:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_** -Klasse "zuder Klasse" weist die folgenden Eigenschaften auf.

<dl> <dt>

**Gerätepfad**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

PNP-Geräte Instanz-ID.

</dd> <dt>

**Devicelocationpath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

PNP-Speicherort Pfad des Geräts.

</dd> <dt>

**Requirements acssupport**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die erforderliche ACS-Unterstützung vorhanden sein sollte, bevor die Aufhebung der Einbindung zugelassen wird.

</dd> <dt>

**Requirements deviceentschärgationen**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob Geräte entschärfungen vorhanden sein sollten, bevor die Aufhebung der Einbindung zugelassen wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1703, \[ nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 




