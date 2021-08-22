---
description: 'Process_V1_TypeGroup1-Klasse: Diese Klasse ist die Ereignistypklasse für Prozessereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.'
ms.assetid: b114d7fd-c308-4f21-8f1a-ab27dc93abc5
title: Process_V1_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V1_TypeGroup1
- Process_V1_TypeGroup1.PageDirectoryBase
- Process_V1_TypeGroup1.ProcessId
- Process_V1_TypeGroup1.ParentId
- Process_V1_TypeGroup1.SessionId
- Process_V1_TypeGroup1.ExitStatus
- Process_V1_TypeGroup1.UserSID
- Process_V1_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: cd2b4ab072b04246351ede86027536d777bce3c7e2321260be4d0622f55663d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070000"
---
# <a name="process_v1_typegroup1-class"></a>Process \_ V1 \_ TypeGroup1-Klasse

Diese Klasse ist die Ereignistypklasse für Prozessereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V1_TypeGroup1 : Process_V1
{
  uint32 PageDirectoryBase;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a>Member

Die **\_ Process V1 \_ TypeGroup1-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Process \_ V1 \_ TypeGroup1-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

ExitStatus
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(5)
</dt> </dl>

Beendigungsstatus des beendeten Prozesses.

</dd> <dt>

ImageFileName
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(7), StringTermination("NullTerminated")
</dt> </dl>

Pfad zur ausführbaren Datei des Prozesses.

</dd> <dt>

PageDirectoryBase
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Zeiger
</dt> </dl>

Reserviert.

</dd> <dt>

ParentId
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3)
</dt> </dl>

Eindeutiger Bezeichner des Prozesses, der diesen Prozess erstellt. Prozessbezeichnernummern werden wiederverwendet, sodass sie nur einen Prozess für die Lebensdauer dieses Prozesses identifizieren. Es ist möglich, dass der durch ParentProcessId identifizierte Prozess beendet wird, sodass ParentProcessId möglicherweise nicht auf einen ausgeführten Prozess verweist. Es ist auch möglich, dass ParentProcessId fälschlicherweise auf einen Prozess verweist, der einen Prozessbezeichner wiederverwendet.

**Windows Server 2003:** Schließt den Format("x")-Qualifizierer ein.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2)
</dt> </dl>

Globaler Prozessbezeichner, den Sie zum Identifizieren eines Prozesses verwenden können. Der Wert ist von dem Zeitpunkt an gültig, zu dem ein Prozess erstellt wird, bis er beendet wird.

**Windows Server 2003:** Schließt den Format("x")-Qualifizierer ein.

</dd> <dt>

SessionID
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4)
</dt> </dl>

Eindeutiger Bezeichner, den ein Betriebssystem generiert, wenn es eine neue Sitzung erstellt. Eine Sitzung erstreckt sich über einen Zeitraum von der Anmeldung bis zur Abmeldung von einem bestimmten System.

</dd> <dt>

UserSID
</dt> <dd> <dl> <dt>

Datentyp: **object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(6), Extension("Sid")
</dt> </dl>

Sicherheits-ID (SID) für den Benutzerkontext, unter dem das Ereignis eintritt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Verarbeiten \_ von V1**](process.md)
</dt> <dt>

[**Verarbeiten \_ von V1**](process-v1.md)
</dt> </dl>

 

 




