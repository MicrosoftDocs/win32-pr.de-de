---
description: Gibt Anweisungen dazu an, wie Timerereignisse für Consumers generiert werden sollen.
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
ms.openlocfilehash: d9081cef3ed58929fa976470b1c567c6accd0f60029f64f28ee7a90d16600d2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132013"
---
# <a name="__timerinstruction-class"></a>\_\_TimerInstruction-Klasse

Die **\_ \_ abstrakte Systemklasse TimerInstruction** gibt Anweisungen dazu an, wie [Timerereignisse](receiving-a-timed-or-repeating-event.md) für Consumers generiert werden sollen.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

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

Die **\_ \_ TimerInstruction-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ TimerInstruction-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt, ob ein Benachrichtigungsereignis generiert und empfangen wird, wenn ein Consumer verfügbar wird.

<dt>

FALSE
</dt> <dd>

Wenn WMI oder der Consumer wieder verfügbar ist, wird ein Benachrichtigungsereignis generiert und empfangen.

</dd> <dt>

TRUE
</dt> <dd>

Das Timerereignis tritt nicht auf, wenn WMI nicht zum Generieren im entsprechenden Zeitintervall verfügbar ist oder der Consumer, der das Ereignis empfangen möchte, nicht verfügbar ist.

</dd> </dl>

</dd> <dt>

**TimerId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)
</dt> </dl>

Eindeutige vom Benutzer zugewiesene Zeichenfolge, die dieses bestimmte Timerereignis identifiziert. Um Namenskonflikte mit anderen Timerbezeichnern zu vermeiden, kann die Zeichenfolgenform einer GUID im DCE-Stil (Distributed Computer Environment) verwendet werden. Diese Eigenschaft ist Teil der [**\_ \_ TimerEvent-Instanz,**](--timerevent.md) die das Ereignis darstellt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ TimerInstruction-Klasse** wird von [**\_ \_ EventGenerator abgeleitet.**](--eventgenerator.md)

Die **\_ \_ TimerInstruction-Unterklassen** sind [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md), die von Consumers verwendet werden, um sich für ein absolutes Timerereignis zu registrieren, und [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md), das zum Registrieren für ein Intervalltimerereignis verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_\_EventGenerator**](/windows/desktop/WmiSdk/--eventgenerator)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> </dl>

 

