---
description: Diese Klasse ist die Ereignistyp Klasse für Dienst Konfigurations Ereignisse.
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
ms.openlocfilehash: 6c061c6a0c4cbb3e807bcb3418155b1194fcfa28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349319"
---
# <a name="systemconfig_v0_services-class"></a>SystemConfig \_ v0 \_ Services-Klasse

Diese Klasse ist die Ereignistyp Klasse für Dienst Konfigurations Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die Klasse " **SystemConfig \_ v0 \_ Services** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SystemConfig \_ v0 \_ Services** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Datentyp: **char16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (2), **Max** (256)
</dt> </dl>

Der Anzeige Name des Dienstanbieter. Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten. Jedoch wird bei Vergleichen des Anzeigenamens immer nach Groß- und Kleinschreibung unterschieden.

</dd> <dt>

**ProcessID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (4)
</dt> </dl>

Der Bezeichner des Prozesses, in dem der Dienst ausgeführt wird.

</dd> <dt>

**ProcessName**
</dt> <dd> <dl> <dt>

Datentyp: **char16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (3), **Max** (34)
</dt> </dl>

Der Name des Prozesses, in dem der Dienst ausgeführt wird.

</dd> <dt>

**Service Name**
</dt> <dd> <dl> <dt>

Datentyp: **char16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (1), **Max** (34)
</dt> </dl>

Eindeutiger Bezeichner des Dienstanbieter. Der Bezeichner gibt Aufschluss über die Funktionen, die der Dienst bereitstellt.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemConfig \_ v0**](systemconfig-v0.md)
</dt> </dl>

 

 




