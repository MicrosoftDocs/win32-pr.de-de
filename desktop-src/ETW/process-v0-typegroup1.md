---
description: Diese Klasse ist die Ereignistyp Klasse für Prozess Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: 2889feb05bfc396f2c2018ca59d2cf46fba8ec13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977704"
---
# <a name="process_v0_typegroup1-class"></a>Process \_ v0 \_ TypeGroup1-Klasse

Diese Klasse ist die Ereignistyp Klasse für Prozess Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die **Process \_ v0 \_ TypeGroup1** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Process \_ v0 \_ TypeGroup1** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

Imagefilename
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4), stringbeendigung ("nullterminiert")
</dt> </dl>

Pfad zur ausführbaren Datei des Prozesses.

</dd> <dt>

ParentId
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2), Zeiger
</dt> </dl>

Eindeutiger Bezeichner des Prozesses, von dem ein Prozess erstellt wird. Die prozesbezeichnernummern werden wieder verwendet, sodass Sie nur einen Prozess für die Lebensdauer dieses Prozesses identifizieren. Es ist möglich, dass der durch "parameterprocessid" identifizierte Prozess beendet wird, sodass "parameterprocessid" möglicherweise nicht auf einen laufenden Prozess verweist. Es ist auch möglich, dass "paramedprocessid" fälschlicherweise auf einen Prozess verweist, der einen Prozess Bezeichner wieder verwendet.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1), Zeiger
</dt> </dl>

Die globale Prozess-ID, mit der Sie einen Prozess identifizieren können. Der Wert ist gültig ab dem Zeitpunkt, zu dem ein Prozess erstellt wird, bis er beendet wird.

</dd> <dt>

UserSID
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3), Erweiterung ("sid")
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

[**Prozess \_ v0**](process-v0.md)
</dt> </dl>

 

 




