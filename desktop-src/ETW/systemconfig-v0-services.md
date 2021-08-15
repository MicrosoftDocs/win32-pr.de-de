---
description: 'SystemConfig_V0_Services Klasse: Diese Klasse ist die Ereignistypklasse für Dienstkonfigurationsereignisse.'
ms.assetid: 1e6c2061-f1a2-4253-a0c4-4b45b2feceda
title: SystemConfig_V0_Services-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Services
- SystemConfig_V0_Services.ServiceName
- SystemConfig_V0_Services.DisplayName
- SystemConfig_V0_Services.ProcessName
- SystemConfig_V0_Services.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5cfe3bfd4509a02eeafcb014f9265f810e4cb942e87b67390dbd1cbf841f7295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393789"
---
# <a name="systemconfig_v0_services-class"></a>SystemConfig \_ V0 \_ Services-Klasse

Diese Klasse ist die Ereignistypklasse für Dienstkonfigurationsereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_V0_Services : SystemConfig_V0
{
  char16 ServiceName[];
  char16 DisplayName[];
  char16 ProcessName[];
  uint32 ProcessId;
};
```

## <a name="members"></a>Member

Die **Klasse SystemConfig \_ V0 \_ Services** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Klasse SystemConfig \_ V0 \_ Services** verfügt über diese Eigenschaften.

<dl> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Datentyp: **char16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (2), **Max** (256)
</dt> </dl>

Anzeigename des Diensts. Der Name wird im Dienststeuerungs-Manager beibehalten. Jedoch wird bei Vergleichen des Anzeigenamens immer nach Groß- und Kleinschreibung unterschieden.

</dd> <dt>

**Processid**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (4)
</dt> </dl>

Bezeichner des Prozesses, in dem der Dienst ausgeführt wird.

</dd> <dt>

**ProcessName**
</dt> <dd> <dl> <dt>

Datentyp: **char16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (3), **Max** (34)
</dt> </dl>

Name des Prozesses, in dem der Dienst ausgeführt wird.

</dd> <dt>

**Servicename**
</dt> <dd> <dl> <dt>

Datentyp: **char16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (1), **Max** (34)
</dt> </dl>

Eindeutiger Bezeichner des Diensts. Der Bezeichner gibt einen Hinweis auf die Funktionalität an, die der Dienst bietet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




