---
description: Ablaufverfolgungsereignis für die Speicherverwaltung für einen Heapzuordnungsvorgang.
ms.assetid: 572DEC3B-F909-45E5-849F-707AA62F2F5E
title: ETW_HEAP_EVENT_ALLOC Ereignis (Ntwmi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_ALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 111c9268cb6ad174dc79323a9b867923e6264428f939caeae7089685e62f4318
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963200"
---
# <a name="etw_heap_event_alloc-event"></a>ETW \_ HEAP \_ EVENT \_ ALLOC-Ereignis

Das **ETW \_ HEAP EVENT \_ \_ ALLOC-Ereignis** ist ein Ablaufverfolgungsereignis für die Speicherverwaltung für einen Heapzuordnungsvorgang.


```C++
typedef struct ETW_HEAP_EVENT_ALLOC
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HeapHandle* 
</dt> <dd>

Das Handle des Heaps, in dem der Arbeitsspeicher belegt wurde. Dies ist das Heaphandle, das eine App an die [**AllocateHeap-Funktion**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) übergeben hat, als der Arbeitsspeicher belegt wurde.

</dd> <dt>

*Größe* 
</dt> <dd>

Die Größe in Bytes, die vom Heap zugeordnet werden.

</dd> <dt>

*Adresse* 
</dt> <dd>

Die Adresse des zugeordneten Arbeitsspeichers.

</dd> <dt>

*Quelle* 
</dt> <dd>

Die Quelle des Arbeitsspeichers, den die Zuweisung für die Heapbelegung verwendet hat.

In der folgenden Tabelle sind die möglichen Werte für den *Source-Parameter* aufgeführt, wie in der Headerdatei *ntetw.h* definiert:



| Wert                                                                                                                                                                                                                                                                               | Bedeutung                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <dt>**ARBEITSSPEICHER \_ FROM \_ LOOKASIDE**</dt> <dt>1</dt> </dl>                                       | Arbeitsspeicher aus der Lookaside-Liste.<br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <dt>**ARBEITSSPEICHER \_ FROM \_ LOWFRAG**</dt> <dt>2</dt> </dl>                                             | Arbeitsspeicher aus dem Heap mit geringer Fragmentierung.<br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <dt>**ARBEITSSPEICHER \_ FROM \_ MAINPATH**</dt> <dt>3</dt> </dl>                                          | Arbeitsspeicher aus dem Hauptcodepfad.<br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <dt> **ARBEITSSPEICHER \_ AUS \_ SLOWPATH**</dt> <dt>4</dt> </dl> | Arbeitsspeicher aus langsamen Pfaden.<br/>                                            |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <dt>**ARBEITSSPEICHER \_ FROM \_ INVALID**</dt> <dt>5</dt> </dl>                                             | Ungültiger Arbeitsspeicher.<br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <dt>**ARBEITSSPEICHER \_ FROM \_ SEGMENT \_ HEAP**</dt> <dt>6</dt> </dl>                             | Dieser Wert ist für die zukünftige Verwendung reserviert und wird nie zurückgegeben.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **ETW \_ HEAP EVENT \_ \_ ALLOC-Ereignis** wird für alle Heapzuordnungen protokolliert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Ntwmi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Ablaufverfolgungsereignisse für die Speicherverwaltung](memory-management-tracing-events.md)
</dt> </dl>

 

 
