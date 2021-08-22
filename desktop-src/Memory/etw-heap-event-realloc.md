---
description: Ablaufverfolgungsereignis für die Speicherverwaltung für einen Heap-Neuzuordnungsvorgang.
ms.assetid: D8080B7B-CECC-40DB-B52A-2C3E4F04ABA9
title: ETW_HEAP_EVENT_REALLOC -Ereignis (Ntwmi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_REALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 705f31eaf403c4edd608c0b3347713e43ec3c81746b5efde90e14b7213425963
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067870"
---
# <a name="etw_heap_event_realloc-event"></a>ETW \_ HEAP \_ EVENT \_ REALLOC-Ereignis

Das **ETW \_ HEAP EVENT \_ \_ REALLOC-Ereignis** ist ein Speicherverwaltungsablaufverfolgungsereignis für einen Heap-Neuzuordnungsvorgang.


```C++
typedef struct ETW_HEAP_EVENT_REALLOC
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HeapHandle* 
</dt> <dd>

Das Handle des Heaps, in dem der Arbeitsspeicher belegt wurde. Dies ist das Heaphandle, das eine App an die [**AllocateHeap-Funktion**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) übergeben hat, als der Arbeitsspeicher belegt wurde.

</dd> <dt>

*NewAddress* 
</dt> <dd>

Die neue Adresse des zugeordneten Arbeitsspeichers.

</dd> <dt>

*OldAddress* 
</dt> <dd>

Die alte Adresse des Speichers, der zuvor zugeordnet wurde.

</dd> <dt>

*NewSize* 
</dt> <dd>

Die neue Größe in Bytes, die vom Heap zugeordnet werden.

</dd> <dt>

*OldSize* 
</dt> <dd>

Die alte Größe in Bytes, die zuvor vom Heap zugeordnet wurden.

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
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <dt> **ARBEITSSPEICHER \_ AUS \_ SLOWPATH**</dt> <dt>4</dt> </dl> | Arbeitsspeicher aus langsamen c.<br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <dt>**ARBEITSSPEICHER \_ FROM \_ INVALID**</dt> <dt>5</dt> </dl>                                             | Ungültiger Arbeitsspeicher.<br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <dt>**ARBEITSSPEICHER \_ FROM \_ SEGMENT \_ HEAP**</dt> <dt>6</dt> </dl>                             | Dieser Wert ist für die zukünftige Verwendung reserviert und wird nie zurückgegeben.<br/> |



 

</dd> </dl>

Dieses Ereignis verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Das **ETW \_ HEAP EVENT \_ \_ REALLOC-Ereignis** wird bei allen Heapumlegungen protokolliert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Ntwmi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ablaufverfolgungsereignisse für die Speicherverwaltung](memory-management-tracing-events.md)
</dt> </dl>

 

 
