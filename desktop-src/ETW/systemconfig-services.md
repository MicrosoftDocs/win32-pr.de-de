---
description: 'SystemConfig_Services-Klasse: Diese Klasse ist die Ereignistypklasse für Dienstkonfigurationsereignisse.'
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
ms.openlocfilehash: 754b0e10c3882911c6e91fc2590c11739c3f7531
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106058"
---
# <a name="systemconfig_services-class"></a>SystemConfig \_ Services-Klasse

Diese Klasse ist die Ereignistypklasse für Dienstkonfigurationsereignisse.

Die folgende Syntax wird aus MOF-Code vereinfacht.

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

Die **SystemConfig \_ Services-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SystemConfig \_ Services-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (5), **StringTermination("NullTerminated")**, **Format("w")**
</dt> </dl>

Anzeigename des Diensts. Der Name wird im Dienststeuerungs-Manager beibehalten. Jedoch wird bei Vergleichen des Anzeigenamens immer nach Groß- und Kleinschreibung unterschieden.

</dd> <dt>

**Processid**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (1), **Format("x")**
</dt> </dl>

Bezeichner des Prozesses, in dem der Dienst ausgeführt wird.

</dd> <dt>

**ProcessName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (6), **StringTermination("NullTerminated")**, **Format("w")**
</dt> </dl>

Name des Prozesses, in dem der Dienst ausgeführt wird.

</dd> <dt>

**Servicename**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (4), **StringTermination("NullTerminated")**, **Format("w")**
</dt> </dl>

Eindeutiger Bezeichner des Diensts. Der Bezeichner gibt einen Hinweis auf die Funktionalität an, die der Dienst bietet.

</dd> <dt>

**ServiceState**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (2), **Format("x")**
</dt> </dl>

Aktueller Status des Diensts. Mögliche Werte finden Sie im **dwCurrentState-Member** von **SERVICE STATUS \_ \_ PROCESS.**

</dd> <dt>

**SubProcessTag**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (3), **Format("x")**
</dt> </dl>

Identifiziert den Dienst.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




