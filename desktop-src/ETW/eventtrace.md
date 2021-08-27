---
description: Eine abstrakte Klasse, von der alle Ereignisablaufverfolgungsklassen abgeleitet werden.
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
ms.openlocfilehash: 37124a1c5ef23782261cbe94462c737d137dc6965363d9c907ea895e289237d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130610"
---
# <a name="eventtrace-class"></a>EventTrace-Klasse

Eine abstrakte Klasse, von der alle Ereignisablaufverfolgungsklassen abgeleitet werden.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

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

Die **EventTrace-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **EventTrace-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**EventGuid**
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (8), **Max** (16)
</dt> </dl>

Die GUID der Ereignisablaufverfolgungsklasse dieses Ereignisses.

</dd> <dt>

**EventSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (1)
</dt> </dl>

Gesamtzahl der Bytes des Ereignisses.

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (3)
</dt> </dl>

Vom Anbieter definierter Ereignistyp. Teilt Ihnen mit, welche Ereignistypklasse verwendet werden soll, um die vom Anbieter definierten Ereignisdaten zu entschlüsseln (die Daten, auf die **mofData** zeigt).

</dd> <dt>

**InstanceId**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (11)
</dt> </dl>

Bezeichner dieser Ereignisinstanz.

</dd> <dt>

**KernelTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (9)
</dt> </dl>

Verstrichene Ausführungszeit für Kernelmodusanweisungen in CPU-Ticks.

</dd> <dt>

**MofData**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (14), **Zeiger**
</dt> </dl>

Zeiger auf die anbieterspezifischen Ereignisdaten.

</dd> <dt>

**MofLength**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (15)
</dt> </dl>

Länge der anbieterspezifischen Ereignisdaten.

</dd> <dt>

**ParentGuid**
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (12), **Max** (16)
</dt> </dl>

GUID der Ereignisablaufverfolgungsklasse der übergeordneten Instanz.

</dd> <dt>

**ParentInstanceId**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (13)
</dt> </dl>

Bezeichner der Daten der übergeordneten Instanz.

</dd> <dt>

**ReservedHeaderField**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (2)
</dt> </dl>

Reserviert.

</dd> <dt>

**Threadid**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (6), **Zeiger**
</dt> </dl>

Gibt den Thread an, der das Ereignis generiert hat

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (7)
</dt> </dl>

Enthält das Datum und die Uhrzeit des Auftretens des Ereignisses.

</dd> <dt>

**Tracelevel**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (4)
</dt> </dl>

Vom Anbieter definierter Wert, der den Schweregrad definiert, der zum Generieren des Ereignisses verwendet wird.

</dd> <dt>

**TraceVersion**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (5)
</dt> </dl>

Vom Anbieter definierte Versionsnummer der Ereignisablaufverfolgungsklasse, die zum Generieren des Ereignisses verwendet wird.

</dd> <dt>

**UserTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (10)
</dt> </dl>

Verstrichene Ausführungszeit für Benutzermodusanweisungen in CPU-Ticks.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Eigenschaften nicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| MOF<br/>                      | <dl> <dt>Wmi.mof</dt> </dl> |



 

 




