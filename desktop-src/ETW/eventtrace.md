---
description: Eine abstrakte Klasse, von der alle Ereignis Ablauf Verfolgungs Klassen abgeleitet werden.
ms.assetid: 03eea902-5050-4ab2-8a72-9bff7777e234
title: EventTrace-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace
- EventTrace.EventSize
- EventTrace.ReservedHeaderField
- EventTrace.EventType
- EventTrace.TraceLevel
- EventTrace.TraceVersion
- EventTrace.ThreadId
- EventTrace.TimeStamp
- EventTrace.EventGuid
- EventTrace.KernelTime
- EventTrace.UserTime
- EventTrace.InstanceId
- EventTrace.ParentGuid
- EventTrace.ParentInstanceId
- EventTrace.MofData
- EventTrace.MofLength
api_type:
- NA
api_location: ''
ms.openlocfilehash: f04399942b39a2da5b746933884a436a65bb370c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752408"
---
# <a name="eventtrace-class"></a>EventTrace-Klasse

Eine abstrakte Klasse, von der alle Ereignis Ablauf Verfolgungs Klassen abgeleitet werden.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[abstract]
class EventTrace
{
  uint16 EventSize;
  uint16 ReservedHeaderField;
  uint8  EventType;
  uint8  TraceLevel;
  uint16 TraceVersion;
  uint64 ThreadId;
  uint64 TimeStamp;
  uint8  EventGuid[];
  uint32 KernelTime;
  uint32 UserTime;
  uint32 InstanceId;
  uint8  ParentGuid[];
  uint32 ParentInstanceId;
  uint32 MofData;
  uint32 MofLength;
};
```

## <a name="members"></a>Member

Die **EventTrace** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **EventTrace** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Eventguid**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (8), **Max** (16)
</dt> </dl>

Die Ereignis-Ablaufverfolgungs-Klassen-GUID dieses Ereignisses.

</dd> <dt>

**Eventsize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (1)
</dt> </dl>

Gesamtanzahl der Bytes des Ereignisses.

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (3)
</dt> </dl>

Vom Anbieter definierter Ereignistyp. Gibt Aufschluss darüber, welche Ereignistyp Klasse zum Entschlüsseln der von einem Anbieter definierten Ereignisdaten verwendet werden soll (die Daten, auf die von " **mufdata**" verwiesen wird.

</dd> <dt>

**InstanceId**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (11)
</dt> </dl>

Der Bezeichner dieser Ereignis Instanz.

</dd> <dt>

**Kernelzeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (9)
</dt> </dl>

Verstrichene Ausführungszeit für Kernel Modus-Anweisungen in CPU-Ticks.

</dd> <dt>

**"MUF"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (14), **Zeiger**
</dt> </dl>

Zeiger auf die anbieterspezifischen Ereignisdaten.

</dd> <dt>

**"Muength"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (15)
</dt> </dl>

Die Länge der anbieterspezifischen Ereignisdaten.

</dd> <dt>

**Parametriguid**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (12), **Max** (16)
</dt> </dl>

Die Ereignis-Ablauf Verfolgungs Klassen-GUID der übergeordneten Instanz.

</dd> <dt>

**ParentInstanceId**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (13)
</dt> </dl>

Der Bezeichner der übergeordneten Instanzdaten.

</dd> <dt>

**Reservedheaderfield**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (2)
</dt> </dl>

Reserviert.

</dd> <dt>

**ThreadID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (6), **Zeiger**
</dt> </dl>

Gibt den Thread an, der das Ereignis generiert hat

</dd> <dt>

**Zeitstempel**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (7)
</dt> </dl>

Enthält das Datum und die Uhrzeit des Auftretens des Ereignisses.

</dd> <dt>

**TraceLevel**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (4)
</dt> </dl>

Vom Anbieter definierter Wert, der den Schweregrad definiert, der zum Generieren des Ereignisses verwendet wird.

</dd> <dt>

**Traceversion**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (5)
</dt> </dl>

Anbieter definierte Versionsnummer der Ereignis Ablauf Verfolgungs Klasse, die zum Generieren des Ereignisses verwendet wird.

</dd> <dt>

**Usertime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (10)
</dt> </dl>

Verstrichene Ausführungszeit für benutzermodusanweisungen in CPU-Ticks.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Eigenschaften nicht.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| MOF<br/>                      | <dl> <dt>WMI. MOF</dt> </dl> |



 

 




