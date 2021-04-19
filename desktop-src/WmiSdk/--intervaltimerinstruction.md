---
description: Generiert Ereignisse in Intervallen, ähnlich einer WM-Zeit Geber \_ Meldung in der Windows-Programmierung.
ms.assetid: 0895a743-a0dd-4833-a2bf-0196369e18b9
ms.tgt_platform: multiple
title: __IntervalTimerInstruction-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __IntervalTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 20dd1c9fb2d009de4d8d957b4d5980cc6d6ff45e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369802"
---
# <a name="__intervaltimerinstruction-class"></a>\_\_Intervaltimerinstruction-Klasse

Die **\_ \_ intervaltimerinstruction** -System Klasse generiert Ereignisse in Intervallen, ähnlich einer WM-Zeit Geber \_ Meldung bei der Windows-Programmierung. Ein Ereignisconsumer registriert sich für das Empfangen von Intervallzeit Geber Ereignissen durch Erstellen einer Ereignis Abfrage, die auf diese Klasse verweist. Aufgrund des Betriebssystem Verhaltens gibt es keine Garantie, dass Ereignisse in genau dem angeforderten Intervall übermittelt werden.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __IntervalTimerInstruction : __TimerInstruction
{
  uint32  IntervalBetweenEvents;
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a>Member

Die **\_ \_ intervaltimerinstruction** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ intervaltimerinstruction** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Intervalbetweerevents**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](standard-qualifiers.md) (Millisekunden)
</dt> </dl>

Anzahl von Millisekunden zwischen Ereignis Ausgründungen.

</dd> <dt>

**Skipifbestandene**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass dieses Ereignis übersprungen werden soll, wenn das Intervall bereits verstrichen ist. Der Standardwert ist **false**. Diese Eigenschaft wird von [**\_ \_ timerinstruction**](--timerinstruction.md)geerbt.

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

Eindeutiger Bezeichner für dieses **\_ \_ intervaltimerinstruction** -Objekt. Diese Eigenschaft wird von [**\_ \_ timerinstruction**](--timerinstruction.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ intervaltimerinstruction** -Klasse wird von [**\_ \_ timerinstruction**](--timerinstruction.md)abgeleitet.

Die für ein Intervallzeit Geber Ereignis eingegebene Ereignis Abfrage basiert in der Regel auf der **timerId-** Eigenschaft. Benachrichtigungs Ereignisse, die von einem Intervall-Timer-Ereignis generiert werden, enthalten die Eigenschaft **numfirings** , die Daten enthält, die die Anzahl der Ereignisse enthalten, die während der Zeit ausgelöst wurden, die Ereignisse nicht empfangen Wenn **skipifover** auf **true** festgelegt ist, werden diese Informationen verworfen.

Der Wert für die **intervalbetweenevents** -Eigenschaft sollte relativ groß sein. Wenn Sie zu klein ist, kann Sie von WMI ignoriert werden, und das Ereignis kann aufgrund von Einschränkungen in einigen Betriebssystemen nicht generiert werden.

WMI generiert das Intervall Timer-Ereignis, indem eine Instanz der [**\_ \_ TimerEvent**](--timerevent.md) -Klasse erstellt wird.

Um diese Timer-Ereignisse in einem temporären Ereignisconsumer zu empfangen, führen Sie [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) mit der folgenden Ereignis Abfrage Zeichenfolge aus:


```sql
SELECT * FROM __TimerEvent WHERE TimerID = "MyEvent"
```



Um diese Timer-Ereignisse in einem permanenten Ereignisconsumer zu empfangen, müssen Sie die vorherige Abfrage in einen Ereignis Filter laden, einen logischen Consumer definieren und eine Filter-zu-Consumer-Bindung für den Filter und den Consumer erstellen. Weitere Informationen finden Sie [unter empfangen von Ereignissen zu allen Zeit](receiving-events-at-all-times.md)Punkten.

## <a name="examples"></a>Beispiele

Die folgende MOF-Deklaration zeigt, wie ein Intervallzeit Geber Ereignis generiert wird, bei dem die Key-Eigenschaft alle 10 Sekunden auf "MyEvent" festgelegt ist:


```mof
instance of __IntervalTimerInstruction
{
  TimerId = "MyEvent";     // inherited from __TimerInstruction
  SkipIfPassed = FALSE;    // also inherited
  IntervalBetweenEvents = 10000;
};
```



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
</dt> </dl>

 

