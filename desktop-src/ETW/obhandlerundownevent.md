---
description: Stellt die Ereignistyp Klasse für Objekt Handle-Ereignisse dar, die mit dem Anfang und dem Ende der Datensammlung verknüpft sind.
ms.assetid: 96231819-f4ca-4c5c-bc19-4a76add5d3cf
title: Obhandlerundownvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleRundownEvent
- ObHandleRundownEvent.Handle
- ObHandleRundownEvent.Object
- ObHandleRundownEvent.ObjectName
- ObHandleRundownEvent.ObjectType
- ObHandleRundownEvent.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5477acc1851d9799fe2bf68f9b867ab3f4c032fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980120"
---
# <a name="obhandlerundownevent-class"></a>Obhandlerundownvent-Klasse

Stellt die Ereignistyp Klasse für Objekt Handle-Ereignisse dar, die mit dem Anfang und dem Ende der Datensammlung verknüpft sind. Dieses Ereignis umfasst das Aufzählen aller Handles, wenn der rundown ausgeführt wird.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, EventType{38,39}, EventTypeName{HandleDCStart,HandleDCEnd}]
class ObHandleRundownEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
  uint32 ProcessId;
};
```

## <a name="members"></a>Member

Die **obhandlerundownetvent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **obhandlerundownetvent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Handle**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**wmidataid**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Das Objekt handle.

</dd> <dt>

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

**ObjectName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**stringbeendigung**](event-tracing-mof-qualifiers.md) ("nullterminiert"), [**wmidataid**](event-tracing-mof-qualifiers.md) (5)
</dt> </dl>

Der Name des Objekts.

</dd> <dt>

**ObjectType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (4)
</dt> </dl>

Der Objekttyp.

</dd> <dt>

**ProcessID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**wmidataid**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

Der Prozessbezeichner.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>WMI Core. MOF</dt> </dl> |



 

 




