---
description: Bewirkt, dass ein Ereignis zu einem bestimmten Zeitpunkt zu einem bestimmten Zeitpunkt generiert wird.
ms.assetid: bcb64c81-3b40-4665-a880-a100629656e0
ms.tgt_platform: multiple
title: __AbsoluteTimerInstruction-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AbsoluteTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5f4f55e635e42ec34e9b3558a0784d319e4d91ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350988"
---
# <a name="__absolutetimerinstruction-class"></a>\_\_Absolutetimerinstruction-Klasse

Die **\_ \_ absolutetimerinstruction** -System Klasse bewirkt, dass ein Ereignis zu einem bestimmten Zeitpunkt zu einem bestimmten Zeitpunkt generiert wird. Ein Ereignisconsumer registriert sich, um ein absolutes Timer-Ereignis zu erhalten, indem eine Instanz dieser Klasse erstellt wird. Das Ereignis wird einmal generiert.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __AbsoluteTimerInstruction : __TimerInstruction
{
  datetime EventDateTime;
  boolean  SkipIfPassed = FALSE;
  string   TimerId;
};
```

## <a name="members"></a>Member

Die **\_ \_ absolutetimerinstruction** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ absolutetimerinstruction** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**EventDateTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Zeichenfolge mit fester Länge im [DMTF-Format](date-and-time-format.md) , das angibt, wann der Timer ausgelöst wird.

</dd> <dt>

**Skipifbestandene**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass das Timer-Ereignis auftritt, wenn WMI es nicht im richtigen Zeitintervall generieren kann oder der Consumer, der den Empfang des Ereignisses anfordert, nicht verfügbar ist. **True** gibt an, dass das Ereignis nicht auftritt. Der Standardwert ist **false**. Wenn WMI oder der Consumer verfügbar wird, wird ein Benachrichtigungs Ereignis generiert und empfangen. Diese Eigenschaft wird von [**\_ \_ timerinstruction**](--timerinstruction.md)geerbt.

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

Eindeutige vom Benutzer zugewiesene Zeichenfolge, die ein bestimmtes Timer-Ereignis bezeichnet. Um Namenskonflikte mit anderen Zeit Geber Bezeichners zu vermeiden, kann die Zeichen folgen Form einer Umgebungs Stil-GUID für verteilte Computer verwendet werden. Diese Eigenschaft wird von [**\_ \_ timerinstruction**](--timerinstruction.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ absolutetimerinstruction** -Klasse wird von [**\_ \_ timerinstruction**](--timerinstruction.md)abgeleitet.

WMI generiert das absolute Timer-Ereignis, indem eine Instanz der [**\_ \_ TimerEvent**](--timerevent.md) -Klasse erstellt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Timerinstruction**](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[Empfangen von zeitgesteuerten oder wiederkehrenden Ereignissen](receiving-a-timed-or-repeating-event.md)
</dt> <dt>

[Empfangen von Ereignissen zu allen Zeitpunkten](receiving-events-at-all-times.md)
</dt> <dt>

[Empfangen von Ereignissen für die Dauer der Anwendung](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

