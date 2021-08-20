---
description: Ablaufverfolgungsereignis für die Speicherverwaltung für einen heapfreien Vorgang.
ms.assetid: 0CCC59F1-AB96-4B7A-9A86-19CA4FBA4A8A
title: ETW_HEAP_EVENT_FREE -Ereignis (Ntwmi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_FREE
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 4cdc7623f666e20b40bda5393b3ff31369181a7f93f3f2f2dc9881cf0c91f7ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117992877"
---
# <a name="etw_heap_event_free-event"></a>ETW \_ HEAP \_ EVENT \_ FREE-Ereignis

Das **ETW \_ HEAP \_ EVENT \_ FREE-Ereignis** ist ein Speicherverwaltungsablaufverfolgungsereignis für einen heapfreien Vorgang.


```C++
typedef struct ETW_HEAP_EVENT_FREE
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HeapHandle* 
</dt> <dd>

Das Handle des Heaps, in dem der Arbeitsspeicher zugeordnet wurde. Dies ist das Heaphanden einer App, die an die [**AllocateHeap-Funktion**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) übergeben wurde, als der Arbeitsspeicher zugeordnet wurde.

</dd> <dt>

*Adresse* 
</dt> <dd>

Die Adresse des Speichers, der frei wurde.

</dd> <dt>

*Quelle* 
</dt> <dd>

Die Quelle des Arbeitsspeichers, den die Zuweisung für die Heapzuordnung verwendet hat.

In der folgenden Tabelle sind die möglichen Werte für den *Source-Parameter* aufgeführt, wie in der *Headerdatei "ntetw.h"* definiert:



| Wert                                                                                                                                                                                                                                                                               | Bedeutung                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <dt>**ARBEITSSPEICHER \_ FROM \_ LOOKASIDE**</dt> <dt>1</dt> </dl>                                       | Arbeitsspeicher aus der Lookasideliste.<br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <dt>**ARBEITSSPEICHER \_ FROM \_ LOWFRAG**</dt> <dt>2</dt> </dl>                                             | Arbeitsspeicher aus dem Heap mit geringer Fragmentierung.<br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <dt>**ARBEITSSPEICHER \_ FROM \_ MAINPATH**</dt> <dt>3</dt> </dl>                                          | Arbeitsspeicher aus dem Hauptcodepfad.<br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <dt> **ARBEITSSPEICHER \_ AUS \_ SLOWPATH**</dt> <dt>4</dt> </dl> | Arbeitsspeicher von langsam c.<br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <dt>**ARBEITSSPEICHER \_ FROM \_ INVALID**</dt> <dt>5</dt> </dl>                                             | Ungültiger Arbeitsspeicher.<br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <dt>**ARBEITSSPEICHER \_ AUS \_ SEGMENT \_ HEAP**</dt> <dt>6</dt> </dl>                             | Dieser Wert ist für die zukünftige Verwendung reserviert und wird nie zurückgegeben.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **ETW \_ HEAP \_ EVENT \_ FREE-Ereignis** wird bei allen Heap-freien Vorgängen protokolliert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Ntwmi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ablaufverfolgungsereignisse für die Speicherverwaltung](memory-management-tracing-events.md)
</dt> </dl>

 

 
