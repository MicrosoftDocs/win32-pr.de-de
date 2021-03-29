---
description: Diese Klasse ist die Ereignistyp Klasse für Prozess Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: fc2308965de5c06a25858a138d4536763613a4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347839"
---
# <a name="process_v1_typegroup1-class"></a>Process \_ v1 \_ TypeGroup1-Klasse

Diese Klasse ist die Ereignistyp Klasse für Prozess Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die **Process \_ v1 \_ TypeGroup1** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Process \_ v1 \_ TypeGroup1** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

ExitStatus
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (5)
</dt> </dl>

Beenden Sie den Status des beendeten Prozesses.

</dd> <dt>

Imagefilename
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (7), stringbeendigung ("nullterminiert")
</dt> </dl>

Pfad zur ausführbaren Datei des Prozesses.

</dd> <dt>

Pagedirectoriybase
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1), Zeiger
</dt> </dl>

Reserviert.

</dd> <dt>

ParentId
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3)
</dt> </dl>

Eindeutiger Bezeichner des Prozesses, der diesen Prozess erstellt. Die prozesbezeichnernummern werden wieder verwendet, sodass Sie nur einen Prozess für die Lebensdauer dieses Prozesses identifizieren. Es ist möglich, dass der durch "parameterprocessid" identifizierte Prozess beendet wird, sodass "parameterprocessid" möglicherweise nicht auf einen laufenden Prozess verweist. Es ist auch möglich, dass "paramedprocessid" fälschlicherweise auf einen Prozess verweist, der einen Prozess Bezeichner wieder verwendet.

**Windows Server 2003:** Schließt den Format Bezeichner "x" ein.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2)
</dt> </dl>

Die globale Prozess-ID, mit der Sie einen Prozess identifizieren können. Der Wert ist gültig ab dem Zeitpunkt, zu dem ein Prozess erstellt wird, bis er beendet wird.

**Windows Server 2003:** Schließt den Format Bezeichner "x" ein.

</dd> <dt>

SessionID
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4)
</dt> </dl>

Eindeutiger Bezeichner, den ein Betriebssystem generiert, wenn eine neue Sitzung erstellt wird. Eine Sitzung erstreckt sich über einen Zeitraum von der Anmeldung bis zum Abmelden von einem bestimmten System.

</dd> <dt>

UserSID
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (6), Erweiterung ("sid")
</dt> </dl>

Sicherheits-ID (SID) für den Benutzer Kontext, in dem das Ereignis auftritt.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Prozess \_ v1**](process.md)
</dt> <dt>

[**Prozess \_ v1**](process-v1.md)
</dt> </dl>

 

 




