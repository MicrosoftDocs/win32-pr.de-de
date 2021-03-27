---
description: Stellt die Ereignistyp Klasse für die Behandlung von duplikatereignissen dar.
ms.assetid: a933ffaa-8c99-4b87-ad00-4c40fa4d8d26
title: Obshandduplicateevent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleDuplicateEvent
- ObHandleDuplicateEvent.Object
- ObHandleDuplicateEvent.ObjectType
- ObHandleDuplicateEvent.SourceHandle
- ObHandleDuplicateEvent.TargetHandle
- ObHandleDuplicateEvent.TargetProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0f81ff9d85c0c5de8469f563db21e2054fa065f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980688"
---
# <a name="obhandleduplicateevent-class"></a>Obshandduplicateevent-Klasse

Stellt die Ereignistyp Klasse für die Behandlung von duplikatereignissen dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, EventType(34), EventTypeName("DuplicateHandle")]
class ObHandleDuplicateEvent : ObTrace
{
  uint32 Object;
  uint16 ObjectType;
  uint32 SourceHandle;
  uint32 TargetHandle;
  uint32 TargetProcessId;
};
```

## <a name="members"></a>Member

Die **obshandduplicateevent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **obshandduplicateevent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Object**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Zeiger**](event-tracing-mof-qualifiers.md), [**wmidataid**](event-tracing-mof-qualifiers.md) (1)
</dt> </dl>

Das Objekt.

</dd> <dt>

**ObjectType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (5)
</dt> </dl>

Der Objekttyp.

</dd> <dt>

**SourceHandle**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**wmidataid**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

Das Handle des Quell Objekts.

</dd> <dt>

**TargetHandle**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**wmidataid**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Das Handle des Zielobjekts.

</dd> <dt>

**TargetProcessID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**wmidataid**](event-tracing-mof-qualifiers.md) (4)
</dt> </dl>

Der Prozess Bezeichner des Ziels.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>WMI Core. MOF</dt> </dl> |



 

 




