---
description: Diese Klasse ist die Ereignistypklasse für bereite Threadereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 861ab070-5536-4897-b523-9b09a7d59b3e
title: ReadyThread-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadyThread
- ReadyThread.TThreadId
- ReadyThread.AdjustReason
- ReadyThread.AdjustIncrement
- ReadyThread.Flag
- ReadyThread.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1b4b3d63b63e4deb9c48f9e117122f021e9d63791292e60da3cc919a6e4535e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069810"
---
# <a name="readythread-class"></a>ReadyThread-Klasse

Diese Klasse ist die Ereignistypklasse für bereite Threadereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{50}, EventTypeName{"ReadyThread"}]
class ReadyThread : Thread_V2
{
  uint32 TThreadId;
  sint8  AdjustReason;
  sint8  AdjustIncrement;
  sint8  Flag;
  sint8  Reserved;
};
```

## <a name="members"></a>Member

Die **ReadyThread-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ReadyThread-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

AdjustIncrement
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3)
</dt> </dl>

Der Wert, um den die Priorität angepasst wird.

</dd> <dt>

AdjustReason
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2)
</dt> </dl>

Der Grund für die Prioritätssteigerung.



| Wert                                                                        | Bedeutung                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Ignorieren Sie das Inkrement.<br/>                                                                                        |
| <dl> <dt>1</dt> </dl> | Wenden Sie das Inkrement an, das inkrementell am Ende jedes Quantens abfällt.<br/>                              |
| <dl> <dt>2</dt> </dl> | Wenden Sie das Inkrement als Verstärkung an, die im Quantenzustand vollständig verfällt (in der Regel für Prioritätsverfall).<br/> |



 

</dd> <dt>

Flag
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4)
</dt> </dl>

Im Folgenden finden Sie die möglichen Statusflags:



| Wert                                                                          | Bedeutung                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>0x1</dt> </dl> | Der Thread wurde aus DPC (verzögerter Prozeduraufruf) gelesen.<br/> |
| <dl> <dt>0x2</dt> </dl> | Der Kernelstapel wird derzeit ausgetauscht.<br/>                      |
| <dl> <dt>0x4</dt> </dl> | Der Prozessadressenbereich wird ausgetauscht.<br/>                       |



 

Beachten Sie, dass beim Austauschen des Kernelstapels oder des Prozessadressenbereichs ein zusätzliches ReadyThread-Ereignis erfolgt, nachdem der Kernelstapel oder der Prozessadressenbereich wieder ausgetauscht und der Thread für die Versendung bereit gemacht wurde.

</dd> <dt>

Reserviert
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(5)
</dt> </dl>

Reserviert.

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Format("x")
</dt> </dl>

Der Threadbezeichner des Threads, der für die Ausführung gelesen wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Thread \_ V2**](thread-v2.md)
</dt> </dl>

 

 




