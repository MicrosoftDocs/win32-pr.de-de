---
description: Stellt die Ereignistypklasse für Handleerstellungs- oder Abschlussereignisse dar.
ms.assetid: 39d27cdf-fa51-4fb1-8998-7150ca627eff
title: ObHandleEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleEvent
- ObHandleEvent.Handle
- ObHandleEvent.Object
- ObHandleEvent.ObjectName
- ObHandleEvent.ObjectType
api_type:
- NA
api_location: ''
ms.openlocfilehash: eec4e0eb00f7c821e3977f448d9c1af7e286d72a21a0a1b9473a6d3cd8fa3451
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083220"
---
# <a name="obhandleevent-class"></a>ObHandleEvent-Klasse

Stellt die Ereignistypklasse für Handleerstellungs- oder Abschlussereignisse dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, EventType{32,33}, EventTypeName{CreateHandle,CloseHandle}]
class ObHandleEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
};
```

## <a name="members"></a>Member

Die **ObHandleEvent-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ObHandleEvent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Handle**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

Das Objekthand handle.

</dd> <dt>

**Object**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Zeiger,**](event-tracing-mof-qualifiers.md) [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)
</dt> </dl>

Das Objekt.

</dd> <dt>

**ObjectName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)
</dt> </dl>

Der Name des Objekts.

</dd> <dt>

**ObjectType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Der Objekttyp.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |



 

 




