---
description: Gibt an, wie Timer-Ereignisse für Consumer generiert werden sollen.
ms.assetid: b08edb25-bedf-4014-a835-4050f5749479
ms.tgt_platform: multiple
title: __TimerInstruction-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __TimerInstruction
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5c6bbbf905a141fb7e9e3621c78709fd78999393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350098"
---
# <a name="__timerinstruction-class"></a>\_\_Timerinstruction-Klasse

Die abstrakte System Klasse **\_ \_ timerinstruction** gibt Anweisungen dazu an, wie [Timer-Ereignisse](receiving-a-timed-or-repeating-event.md) für Consumer generiert werden sollen.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[abstract]
class __TimerInstruction : __EventGenerator
{
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a>Member

Die **\_ \_ timerinstruction** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ timerinstruction** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Skipifbestandene**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt, ob ein Benachrichtigungs Ereignis generiert und empfangen wird, wenn ein Consumer verfügbar wird.

<dt>

false
</dt> <dd>

Wenn WMI oder der Consumer wieder verfügbar wird, wird ein Benachrichtigungs Ereignis generiert und empfangen.

</dd> <dt>

TRUE
</dt> <dd>

Das Timer-Ereignis tritt nicht auf, wenn WMI nicht verfügbar ist, um es im entsprechenden Zeitintervall zu generieren, oder wenn der Consumer, der den Empfang des Ereignisses anfordert, nicht verfügbar ist.

</dd> </dl>

</dd> <dt>

**TimerId**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)
</dt> </dl>

Eindeutige vom Benutzer zugewiesene Zeichenfolge, die dieses bestimmte Timer-Ereignis bezeichnet. Um Namenskonflikte mit anderen Zeit Geber Bezeichners zu vermeiden, kann die Zeichen folgen Form einer DCE-GUID (verteilten Computer Environment) verwendet werden. Diese Eigenschaft ist Teil der [**\_ \_ TimerEvent**](--timerevent.md) -Instanz, die das Ereignis darstellt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ timerinstruction** -Klasse wird von [**\_ \_ eventgenerator**](--eventgenerator.md)abgeleitet.

Die **\_ \_ timerinstruction** -Unterklassen sind [**\_ \_ absolutetimerinstruction**](--absolutetimerinstruction.md), die von Consumern verwendet werden, um sich für ein absolutes Zeit Geber Ereignis und [**\_ \_ intervaltimerinstruction**](--intervaltimerinstruction.md)zu registrieren, das für die Registrierung für ein Intervallzeit Geber Ereignis verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Eventgenerator**](/windows/desktop/WmiSdk/--eventgenerator)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> </dl>

 

