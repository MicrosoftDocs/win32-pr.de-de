---
description: Stellt die Ereignistyp Klasse für Objekttyp Ereignisse dar, die mit dem Anfang und dem Ende der Datensammlung verknüpft sind.
ms.assetid: 16b21f61-e734-4f51-9b11-e507b5957107
title: Obtypeevent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTypeEvent
- ObTypeEvent.ObjectType
- ObTypeEvent.Reserved
- ObTypeEvent.TypeName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9d80d5fbe57565d64e9ea53587d7a2c3488e6cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131881"
---
# <a name="obtypeevent-class"></a>Obtypeevent-Klasse

Stellt die Ereignistyp Klasse für Objekttyp Ereignisse dar, die mit dem Anfang und dem Ende der Datensammlung verknüpft sind. Dieses Ereignis umfasst die Zuordnung der Typindex Werte zu den Typnamen.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, EventType{36,37}, EventTypeName{TypeDCStart,TypeDCEnd}]
class ObTypeEvent : ObTrace
{
  uint16 ObjectType;
  uint16 Reserved;
  string TypeName;
};
```

## <a name="members"></a>Member

Die **obtypeevent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **obtypeevent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**ObjectType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (1)
</dt> </dl>

Der Objekttyp.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

Reserviert.

</dd> <dt>

**TypeName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**stringbeendigung**](event-tracing-mof-qualifiers.md) ("nullterminiert"), [**wmidataid**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Der Typname.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>WMI Core. MOF</dt> </dl> |



 

 




