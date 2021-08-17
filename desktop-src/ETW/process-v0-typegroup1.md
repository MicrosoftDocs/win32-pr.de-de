---
description: 'Process_V0_TypeGroup1 Klasse: Diese Klasse ist die Ereignistypklasse für Prozessereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.'
ms.assetid: fcf2897d-32b4-42b9-892c-f0106687d3c2
title: Process_V0_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V0_TypeGroup1
- Process_V0_TypeGroup1.ProcessId
- Process_V0_TypeGroup1.ParentId
- Process_V0_TypeGroup1.UserSID
- Process_V0_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0d42ed4704eafcbb335b29c2c2d8d83e2ea82591c75855a6da096cb1e11a7572
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394436"
---
# <a name="process_v0_typegroup1-class"></a>Process \_ V0 \_ TypeGroup1-Klasse

Diese Klasse ist die Ereignistypklasse für Prozessereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V0_TypeGroup1 : Process_V0
{
  uint32 ProcessId;
  uint32 ParentId;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a>Member

Die **Process \_ V0 \_ TypeGroup1-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Klasse Process \_ V0 \_ TypeGroup1** verfügt über diese Eigenschaften.

<dl> <dt>

ImageFileName
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4), StringTermination("NullTerminated")
</dt> </dl>

Pfad zur ausführbaren Datei des Prozesses.

</dd> <dt>

ParentId
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), Zeiger
</dt> </dl>

Eindeutiger Bezeichner des Prozesses, der einen Prozess erstellt. Prozessbezeichnernummern werden wiederverwendet, sodass sie nur einen Prozess für die Lebensdauer dieses Prozesses identifizieren. Es ist möglich, dass der von ParentProcessId identifizierte Prozess beendet wird, sodass ParentProcessId möglicherweise nicht auf einen ausgeführten Prozess verweisen kann. Es ist auch möglich, dass ParentProcessId fälschlicherweise auf einen Prozess verweist, der einen Prozessbezeichner wiederverwendet.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Zeiger
</dt> </dl>

Globaler Prozessbezeichner, den Sie zum Identifizieren eines Prozesses verwenden können. Der Wert ist ab dem Zeitpunkt gültig, zu dem ein Prozess erstellt wird, bis er beendet wird.

</dd> <dt>

UserSID
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3), Extension("Sid")
</dt> </dl>

Sicherheits-ID (SID) für den Benutzerkontext, unter dem das Ereignis eintritt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Verarbeiten \_ von V0**](process-v0.md)
</dt> </dl>

 

 




