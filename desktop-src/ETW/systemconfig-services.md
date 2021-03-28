---
description: Diese Klasse ist die Ereignistyp Klasse für Dienst Konfigurations Ereignisse.
ms.assetid: 7cba9992-d154-44b8-87d8-b46a8438f607
title: SystemConfig_Services-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Services
- SystemConfig_Services.ProcessId
- SystemConfig_Services.ServiceState
- SystemConfig_Services.SubProcessTag
- SystemConfig_Services.ServiceName
- SystemConfig_Services.DisplayName
- SystemConfig_Services.ProcessName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 97b4d2a56f2ed739403681875e0be4d9e21481ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977472"
---
# <a name="systemconfig_services-class"></a>SystemConfig- \_ Dienstklasse

Diese Klasse ist die Ereignistyp Klasse für Dienst Konfigurations Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_Services : SystemConfig
{
  uint32 ProcessId;
  uint32 ServiceState;
  uint32 SubProcessTag;
  string ServiceName[];
  string DisplayName[];
  string ProcessName[];
};
```

## <a name="members"></a>Member

Die **SystemConfig \_ Services** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SystemConfig \_ Services** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (5), **stringbeendigung ("nullterminiert")**, **Format ("w")**
</dt> </dl>

Der Anzeige Name des Dienstanbieter. Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten. Jedoch wird bei Vergleichen des Anzeigenamens immer nach Groß- und Kleinschreibung unterschieden.

</dd> <dt>

**ProcessID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (1), **Format ("x")**
</dt> </dl>

Der Bezeichner des Prozesses, in dem der Dienst ausgeführt wird.

</dd> <dt>

**ProcessName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (6), **stringbeendigung ("nullterminiert")**, **Format ("w")**
</dt> </dl>

Der Name des Prozesses, in dem der Dienst ausgeführt wird.

</dd> <dt>

**Service Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (4), **stringbeendigung ("nullterminiert")**, **Format ("w")**
</dt> </dl>

Eindeutiger Bezeichner des Dienstanbieter. Der Bezeichner gibt Aufschluss über die Funktionen, die der Dienst bereitstellt.

</dd> <dt>

**ServiceState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (2), **Format ("x")**
</dt> </dl>

Aktueller Status des Dienstanbieter. Mögliche Werte finden Sie unter dem **dwcurrentstate** -Member des **Dienst \_ Status \_ Prozesses**.

</dd> <dt>

**Subprocesstag**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (3), **Format ("x")**
</dt> </dl>

Identifiziert den Dienst.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




