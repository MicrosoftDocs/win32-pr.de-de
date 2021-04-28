---
description: 'SystemConfig_V0_Services-Klasse: Diese Klasse ist die Ereignistypklasse für Dienstkonfigurationsereignisse.'
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
ms.openlocfilehash: b69ca7cf4ee4e16a5fbcb6a5f10c659f713ab458
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105928"
---
# <a name="systemconfig_v0_services-class"></a>SystemConfig \_ V0 \_ Services-Klasse

Diese Klasse ist die Ereignistypklasse für Dienstkonfigurationsereignisse.

Die folgende Syntax wird aus MOF-Code vereinfacht.

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

Die **SystemConfig \_ V0 \_ Services-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SystemConfig \_ V0 \_ Services-Klasse** verfügt über diese Eigenschaften.

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



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




