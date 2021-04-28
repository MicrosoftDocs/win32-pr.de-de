---
description: 'Process_TypeGroup1 Klasse: Diese Klasse ist die Ereignistypklasse für Prozessereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: 4f06e1af-3f9a-4346-aa50-50f3ee82cd98
title: Process_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_TypeGroup1
- Process_TypeGroup1.UniqueProcessKey
- Process_TypeGroup1.ProcessId
- Process_TypeGroup1.ParentId
- Process_TypeGroup1.SessionId
- Process_TypeGroup1.ExitStatus
- Process_TypeGroup1.DirectoryTableBase
- Process_TypeGroup1.UserSID
- Process_TypeGroup1.ImageFileName
- Process_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: bd67059f5257dad9b66e1c21f642fef04f03719e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106378"
---
# <a name="process_typegroup1-class"></a>Process \_ TypeGroup1-Klasse

Diese Klasse ist die Ereignistypklasse für Prozessereignisse.

Die folgende Syntax wird durch MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_TypeGroup1 : Process
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  uint32 DirectoryTableBase;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a>Member

Die **Process \_ TypeGroup1-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Process \_ TypeGroup1-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

CommandLine
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(9), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Vollständige Befehlszeile des Prozesses.

</dd> <dt>

DirectoryTableBase
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(6), Zeiger
</dt> </dl>

Die physische Adresse der Seitentabelle des Prozesses.

</dd> <dt>

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

Datentyp: **String**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(8), StringTermination("NullTerminated")
</dt> </dl>

Pfad zur ausführbaren Datei des Prozesses.

</dd> <dt>

ParentId
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3), Format("x")
</dt> </dl>

Eindeutiger Bezeichner des Prozesses, der diesen Prozess erstellt. Prozessbezeichnernummern werden wiederverwendet, sodass sie nur einen Prozess für die Lebensdauer dieses Prozesses identifizieren. Es ist möglich, dass der durch ParentProcessId identifizierte Prozess beendet wird, sodass ParentProcessId möglicherweise nicht auf einen ausgeführten Prozess verweist. Es ist auch möglich, dass ParentProcessId fälschlicherweise auf einen Prozess verweist, der einen Prozessbezeichner wiederverwendet.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), Format("x")
</dt> </dl>

Globaler Prozessbezeichner, den Sie zum Identifizieren eines Prozesses verwenden können. Der Wert ist gültig ab dem Zeitpunkt, zu dem ein Prozess erstellt wird, bis er beendet wird.

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

UniqueProcessKey
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Zeiger
</dt> </dl>

Die Adresse des Prozessobjekts im Kernel.

</dd> <dt>

UserSID
</dt> <dd> <dl> <dt>

Datentyp: **object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(7), Extension("Sid")
</dt> </dl>

Sicherheits-ID (SID) für den Benutzerkontext, unter dem das Ereignis eintritt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die DCStart- und DCEnd-Ereignistypen zählen den Prozess auf, der derzeit ausgeführt wird, einschließlich Leerlauf und Systemprozess, zu dem Zeitpunkt, zu dem die Kernelsitzung gestartet bzw. beendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Prozess**](process.md)
</dt> </dl>

 

 




