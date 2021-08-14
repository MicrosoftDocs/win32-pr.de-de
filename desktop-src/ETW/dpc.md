---
description: Diese Klasse ist die Ereignistypklasse für DPC-Ereignisse (Device Deferred Procedure Call). Die folgende Syntax wird durch einen MOF-Code vereinfacht.
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
ms.openlocfilehash: ef1f0c43d8b91aec1de266176aaef254360c73c99db163280b7bb2d1cbde4832
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118395164"
---
# <a name="dpc-class"></a>DPC-Klasse

Diese Klasse ist die Ereignistypklasse für DPC-Ereignisse (Device Deferred Procedure Call).

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

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

Die **DPC-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **DPC-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**InitialTime**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Extension("WmiTime")
</dt> </dl>

DPC-Einstiegszeit.

</dd> <dt>

**-Routine zurückgegebener Wert**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), Zeiger
</dt> </dl>

Adresse der DPC-Routine. Verwenden Sie die Adresse mit den Bildereignissen, um zu suchen, welches Image gestartet wurde.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Ereignisse werden protokolliert, wenn ein DPC eingegeben wird. Sie verwenden diese Ereignisse, um das Verhalten von Treibern und Kernelmoduskomponenten zu überwachen und zu überprüfen. Beispielsweise können Sie DPC-, ISR- und Imageereignisse verwenden, um die Komponenten zu bestimmen, die zu viel Zeit mit hohen Interruptebenen verbringen. DPC- und ISR-Ereignisse verfügen über einen Einstiegszeitstempel, mit dem die Dauer der Routinen berechnet wird. Die Bildereignisse werden gelesen, um die Speicherregionen zu erstellen, die bestimmten Modulen zuordnen. Sie können die Zuordnung verwenden, um das Modul zu suchen, das die Interruptroutine enthält.

Das TimerDPC-Ereignis zeichnet auf, wenn ein DPC als Ergebnis eines Timerablaufs und das ThreadDPC-Ereignis beim Ausführen eines Threaded DPC-Ereignisses ausgeführt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




