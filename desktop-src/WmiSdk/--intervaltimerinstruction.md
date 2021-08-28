---
description: Generiert Ereignisse in Intervallen, ähnlich wie eine WM \_ TIMER-Nachricht in Windows Programmierung.
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
ms.openlocfilehash: 17f0c55edceb3c5fb009f49ae97e3765ec3e0255a82f8c75e133344379c24d90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640760"
---
# <a name="__intervaltimerinstruction-class"></a>\_\_IntervalTimerInstruction-Klasse

Die **\_ \_ IntervalTimerInstruction-Systemklasse** generiert Ereignisse in Intervallen, ähnlich wie eine WM \_ TIMER-Nachricht in Windows Programmierung. Ein Ereignisverbraucher registriert sich zum Empfangen von Intervalltimerereignissen, indem er eine Ereignisabfrage erstellt, die auf diese Klasse verweist. Aufgrund des Betriebssystemverhaltens gibt es keine Garantie dafür, dass Ereignisse genau im angeforderten Intervall übermittelt werden.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

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

Die **\_ \_ IntervalTimerInstruction-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ IntervalTimerInstruction-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**IntervalBetweenEvents**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](standard-qualifiers.md) (Millisekunden)
</dt> </dl>

Anzahl von Millisekunden zwischen Ereignisauslösung.

</dd> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True gibt an, dass dieses Ereignis übersprungen werden soll, wenn das Intervall bereits überschritten wurde. Der Standardwert ist **FALSE.** Diese Eigenschaft wird von [**\_ \_ TimerInstruction**](--timerinstruction.md)geerbt.

<dt>

FALSE
</dt> <dd>

Wenn WMI oder der Consumer wieder verfügbar ist, wird ein Benachrichtigungsereignis generiert und empfangen.

</dd> <dt>

TRUE
</dt> <dd>

Das Timerereignis tritt nicht auf, wenn WMI nicht verfügbar ist, um es im entsprechenden Zeitintervall zu generieren, oder wenn der Consumer, der den Empfang des Ereignisses anfordert, nicht verfügbar ist.

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

Eindeutiger Bezeichner für dieses **\_ \_ IntervalTimerInstruction-Objekt.** Diese Eigenschaft wird von [**\_ \_ TimerInstruction**](--timerinstruction.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ IntervalTimerInstruction-Klasse** wird von [**\_ \_ TimerInstruction**](--timerinstruction.md)abgeleitet.

Die Ereignisabfrage, die eingegeben wurde, um sich für ein Intervalltimerereignis zu registrieren, basiert in der Regel auf der **TimerId-Eigenschaft.** Benachrichtigungsereignisse, die von einem Intervalltimerereignis generiert werden, enthalten die Eigenschaft **NumFirings,** die Daten enthält, die die Anzahl der Ereignisse widerspiegeln, die während des Empfangs der Ereignisse ausgelöst wurden. Wenn **SkipIfPassed** auf **TRUE** festgelegt ist, werden diese Informationen verworfen.

Der Wert für die **IntervalBetweenEvents-Eigenschaft** sollte relativ groß sein. Wenn sie zu klein ist, ignoriert WMI sie möglicherweise und generiert das Ereignis aufgrund von Einschränkungen in einigen Betriebssystemen nicht.

WMI generiert das Intervallzeitgeberereignis, indem eine Instanz der [**\_ \_ TimerEvent-Klasse**](--timerevent.md) erstellt wird.

Um diese Timerereignisse in einem temporären Ereignisverbraucher zu empfangen, führen [**Sie IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) mit der folgenden Ereignisabfragezeichenfolge aus:


```sql
SELECT * FROM __TimerEvent WHERE TimerID = "MyEvent"
```



Um diese Timerereignisse in einem permanenten Ereignisverbraucher zu empfangen, müssen Sie die vorherige Abfrage in einen Ereignisfilter laden, einen logischen Consumer definieren und eine Filter-zu-Consumer-Bindung für den Filter und Consumer erstellen. Weitere Informationen finden Sie unter [Empfangen von Ereignissen zu allen Zeiten.](receiving-events-at-all-times.md)

## <a name="examples"></a>Beispiele

Die folgende MOF-Deklaration zeigt, wie sie alle 10 Sekunden ein Intervalltimerereignis mit der Schlüsseleigenschaft "MyEvent" generieren:


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

[**\_\_TimerInstruction**](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> <dt>

[Empfangen von Zeit- oder Wiederholungsereignissen](receiving-a-timed-or-repeating-event.md)
</dt> </dl>

 

