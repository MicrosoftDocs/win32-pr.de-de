---
description: Diese Klasse ist die Ereignistyp Klasse für Geräte verzögerte Prozedur Aufrufe (DPC). Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 46010179-7f0a-47dd-95fd-04d30fc597ba
title: DPC-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DPC
- DPC.InitialTime
- DPC.Routine
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0e756c2b41499a6e5b82129d609befc41d5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862088"
---
# <a name="dpc-class"></a>DPC-Klasse

Diese Klasse ist die Ereignistyp Klasse für Geräte verzögerte Prozedur Aufrufe (DPC).

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{66, 68, 69}, EventTypeName{"ThreadDPC", "DPC", "TimerDPC"}]
class DPC : PerfInfo
{
  object InitialTime;
  uint32 Routine;
};
```

## <a name="members"></a>Member

Die **DPC** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **DPC** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Initialtime**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1), Erweiterung ("wmitime")
</dt> </dl>

DPC-Eintrags Zeit.

</dd> <dt>

**-Routine zurückgegebener Wert**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2), Zeiger
</dt> </dl>

Adresse der DPC-Routine. Verwenden Sie die Adresse mit den Bild Ereignissen, um zu ermitteln, welches Image gestartet wurde.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Ereignisse werden protokolliert, wenn ein DPC eingegeben wird. Mit diesen Ereignissen können Sie das Verhalten von Treibern und Kernelmoduskomponenten überwachen und überprüfen. Beispielsweise können Sie DPC-, ISR-und Image-Ereignisse verwenden, um die Komponenten zu bestimmen, die zu viel Zeit für hohe Unterbrechungs Stufen aufwenden. DPC-und ISR-Ereignisse verfügen über einen Eintrags Zeitstempel, der verwendet wird, um die Dauer der Routinen zu berechnen. Die Bild Ereignisse werden gelesen, um die Speicherbereiche zu erstellen, die bestimmten Modulen zugeordnet werden. Sie können die Zuordnung verwenden, um das Modul zu suchen, das die Interruptroutine enthält.

Das timerdpc-Ereignis zeichnet auf, wenn ein DPC aufgrund eines Zeit Geber Ablaufs und der threaddpc-Ereignisdaten Sätze ausgelöst wird, wenn ein Thread-DPC ausgeführt wird.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 




