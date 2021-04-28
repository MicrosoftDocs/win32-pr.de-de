---
description: 'Registry_V0_TypeGroup1-Klasse: Diese Klasse ist die Ereignistypklasse für Registrierungsereignisse. Die folgende Syntax wird aus MOF-Code vereinfacht.'
ms.assetid: 93031f3e-963f-46a6-9355-988eefd94836
title: Registry_V0_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V0_TypeGroup1
- Registry_V0_TypeGroup1.Status
- Registry_V0_TypeGroup1.KeyHandle
- Registry_V0_TypeGroup1.ElapsedTime
- Registry_V0_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 86f6d695afa2e05c87a076cf88ed8023e9416beb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106188"
---
# <a name="registry_v0_typegroup1-class"></a>Registry \_ V0 \_ TypeGroup1-Klasse

Diese Klasse ist die Ereignistypklasse für Registrierungsereignisse.

Die folgende Syntax wird aus MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush"}]
class Registry_V0_TypeGroup1 : Registry_V0
{
  uint32 Status;
  uint32 KeyHandle;
  sint64 ElapsedTime;
  string KeyName;
};
```

## <a name="members"></a>Member

Die **Klasse Registry \_ V0 \_ TypeGroup1** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Klasse Registry \_ V0 \_ TypeGroup1** verfügt über diese Eigenschaften.

<dl> <dt>

ElapsedTime
</dt> <dd> <dl> <dt>

Datentyp: **sint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3)
</dt> </dl>

Verstrichene Zeit des Registrierungsvorgangs.

</dd> <dt>

KeyHandle
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), Zeiger
</dt> </dl>

Handle für den Registrierungsschlüssel.

</dd> <dt>

KeyName
</dt> <dd> <dl> <dt>

Datentyp: **String**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Der Name des Registrierungsschlüssels

</dd> <dt>

Status
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Zeiger
</dt> </dl>

NTSTATUS-Wert des Registrierungsvorgang.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Registrierung \_ V0**](registry-v0.md)
</dt> </dl>

 

 




