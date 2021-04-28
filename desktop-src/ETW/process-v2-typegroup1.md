---
description: 'Process_V2_TypeGroup1 Klasse: Diese Klasse ist die Ereignistypklasse für Prozessereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: ff5c1f64-2087-4238-81f9-6283f0f0e68a
title: Process_V2_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup1
- Process_V2_TypeGroup1.UniqueProcessKey
- Process_V2_TypeGroup1.ProcessId
- Process_V2_TypeGroup1.ParentId
- Process_V2_TypeGroup1.SessionId
- Process_V2_TypeGroup1.ExitStatus
- Process_V2_TypeGroup1.UserSID
- Process_V2_TypeGroup1.ImageFileName
- Process_V2_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: b587a07f33b066cfd7dbeebc44d7277b33c6bee8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106308"
---
# <a name="process_v2_typegroup1-class"></a>Process \_ V2 \_ TypeGroup1-Klasse

Diese Klasse ist die Ereignistypklasse für Prozessereignisse.

Die folgende Syntax wird durch MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_V2_TypeGroup1 : Process_V2
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a>Member

Die **Klasse Process \_ V2 \_ TypeGroup1** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Klasse Process \_ V2 \_ TypeGroup1** verfügt über diese Eigenschaften.

<dl> <dt>

CommandLine
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(8), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Vollständige Befehlszeile des Prozesses.

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

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(7), StringTermination("NullTerminated")
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

Eindeutiger Bezeichner des Prozesses, der diesen Prozess erstellt. Prozessbezeichnernummern werden wiederverwendet, sodass sie nur einen Prozess für die Lebensdauer dieses Prozesses identifizieren. Es ist möglich, dass der von ParentProcessId identifizierte Prozess beendet wird, sodass ParentProcessId möglicherweise nicht auf einen ausgeführten Prozess verweisen kann. Es ist auch möglich, dass ParentProcessId fälschlicherweise auf einen Prozess verweist, der einen Prozessbezeichner wiederverwendet.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), Format("x")
</dt> </dl>

Globaler Prozessbezeichner, den Sie zum Identifizieren eines Prozesses verwenden können. Der Wert ist ab dem Zeitpunkt gültig, zu dem ein Prozess erstellt wird, bis er beendet wird.

</dd> <dt>

SessionID
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4)
</dt> </dl>

Eindeutiger Bezeichner, den ein Betriebssystem generiert, wenn es eine neue Sitzung erstellt. Eine Sitzung erstreckt sich über einen Zeitraum von der Anmeldung bis zur Abmelde von einem bestimmten System.

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

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(6), Extension("Sid")
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

[**Prozess \_ V2**](process-v2.md)
</dt> </dl>

 

 




