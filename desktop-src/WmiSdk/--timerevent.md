---
description: Meldet ein Ereignis, das von WMI als Reaktion auf einen Consumer-Anforderung für ein Intervall-Timer-Ereignis oder ein absolutes Timer-Ereignis generiert wurde.
ms.assetid: 5ae29312-cfda-42c9-a154-e5bb31819be0
ms.tgt_platform: multiple
title: __TimerEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __TimerEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 2de8967110568e968bb241ebbf4942bf1504b332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352781"
---
# <a name="__timerevent-class"></a>\_\_TimerEvent-Klasse

Die **\_ \_ TimerEvent** -System Klasse meldet ein Ereignis, das von WMI als Antwort auf die Anforderung eines Intervalls für Intervalle oder ein absolutes Zeit Geber Ereignis generiert wurde. Ein Intervall-Timer-Ereignis ist ein Ereignis, das in regelmäßigen Abständen auftritt. Ein absolutes Timer-Ereignis ist ein Ereignis, das zu einem bestimmten Zeitpunkt auftritt. Timer-Ereignisse können in einem beliebigen Namespace auftreten.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __TimerEvent : __Event
{
  uint32 NumFirings;
  uint8  SECURITY_DESCRIPTOR[];
  string TimerId;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Member

Die **\_ \_ TimerEvent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ TimerEvent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Numfirings**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie oft das Ereignis aufgetreten ist, bevor eine Benachrichtigung an den Consumer gesendet wurde.

</dd> <dt>

**Sicherheits \_ Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.

</dd> <dt>

**\_Erstellungszeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde. Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt. Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**TimerId**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Instanz der [**\_ \_ timerinstruction**](--timerinstruction.md) -Unterklasse, die bewirkt hat, dass WMI dieses Ereignis ausgelöst hat. Consumer geben eine **\_ \_ timerkennung** in der **timerId-** Eigenschaft der timerinstruction-Unterklasse an, die Sie für die Registrierung erstellen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ TimerEvent** -Klasse wird von [**\_ \_ Event**](--event.md)abgeleitet.

Ereignisconsumer registrieren sich für ein absolutes Timer-Ereignis, indem eine Instanz der [**\_ \_ absolutetimerinstruction**](--absolutetimerinstruction.md) -System Klasse erstellt wird. Sie registrieren sich für ein Intervallzeit Geber Ereignis, indem eine Instanz der [**\_ \_ intervaltimerinstruction**](--intervaltimerinstruction.md) -System Klasse erstellt wird.

Während des normalen Betriebs wird die **numfirings** -Eigenschaft auf 1 festgelegt. Wenn es nicht möglich ist, den Consumer zu erreichen, oder das auslöserintervall deutlich schneller ist als die Möglichkeit, das Ereignis zu übermitteln, wird **numfirings** auf eine Zahl größer als 1 festgelegt. Wenn **numfirings** größer als 1 ist, führt WMI automatisch viele Timer-Ereignisse in dasselbe Ereignis zusammen. Diese Zusammenführung ähnelt der Vorgehensweise bei [**WM \_**](/windows/desktop/winmsg/wm-timer) -Zeit Geber Nachrichten in der Windows-Programmierung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Ereignis**](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[Empfangen von zeitgesteuerten oder wiederkehrenden Ereignissen](receiving-a-timed-or-repeating-event.md)
</dt> <dt>

[Empfangen von Ereignissen zu allen Zeitpunkten](receiving-events-at-all-times.md)
</dt> <dt>

[Empfangen von Ereignissen für die Dauer der Anwendung](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

