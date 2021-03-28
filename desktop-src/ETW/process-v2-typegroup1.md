---
description: Diese Klasse ist die Ereignistyp Klasse für Prozess Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: 01da5a8254627d6378c9f99aa2ba36dc6714e6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980408"
---
# <a name="process_v2_typegroup1-class"></a>Process \_ v2 \_ TypeGroup1-Klasse

Diese Klasse ist die Ereignistyp Klasse für Prozess Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die **Process \_ v2 \_ TypeGroup1** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Process \_ v2 \_ TypeGroup1** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

CommandLine
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (8), stringbeendigung ("nullterminiert"), Format ("w")
</dt> </dl>

Vollständige Befehlszeile des Prozesses.

</dd> <dt>

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

ParentId
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3), Format ("x")
</dt> </dl>

Eindeutiger Bezeichner des Prozesses, der diesen Prozess erstellt. Die prozesbezeichnernummern werden wieder verwendet, sodass Sie nur einen Prozess für die Lebensdauer dieses Prozesses identifizieren. Es ist möglich, dass der durch "parameterprocessid" identifizierte Prozess beendet wird, sodass "parameterprocessid" möglicherweise nicht auf einen laufenden Prozess verweist. Es ist auch möglich, dass "paramedprocessid" fälschlicherweise auf einen Prozess verweist, der einen Prozess Bezeichner wieder verwendet.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2), Format ("x")
</dt> </dl>

Die globale Prozess-ID, mit der Sie einen Prozess identifizieren können. Der Wert ist gültig ab dem Zeitpunkt, zu dem ein Prozess erstellt wird, bis er beendet wird.

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

Uniqueprocesskey
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1), Zeiger
</dt> </dl>

Die Adresse des Prozess Objekts im Kernel.

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

## <a name="remarks"></a>Bemerkungen

Die Ereignis Typen DCStart und DCEnd zählen den Prozess, der derzeit ausgeführt wird, einschließlich Leerlauf und System Prozess, zu dem Zeitpunkt, zu dem die Kernel Sitzung beginnt bzw. endet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Prozess \_ v2**](process-v2.md)
</dt> </dl>

 

 




