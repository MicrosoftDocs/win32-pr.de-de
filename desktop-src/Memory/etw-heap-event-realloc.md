---
description: Ablauf Verfolgungs Ereignis für die Speicherverwaltung für einen Heap-neuzuordnungs Vorgang.
ms.assetid: D8080B7B-CECC-40DB-B52A-2C3E4F04ABA9
title: ETW_HEAP_EVENT_REALLOC-Ereignis (ntwmi. h)
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
ms.openlocfilehash: 7aec225793967c38b97fecae88d28141e48a3cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351667"
---
# <a name="etw_heap_event_realloc-event"></a>Ereignis zur \_ \_ \_ erneuten Zuweisung von etw-Heap Ereignissen

Das Ereignis **\_ \_ \_ realloc für das ETW-Heap Ereignis** ist ein Ablauf Verfolgungs Ereignis für die Speicherverwaltung für einen Heap-neuzuordnungs Vorgang.


```C++
typedef struct ETW_HEAP_EVENT_REALLOC
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Heaphandle* 
</dt> <dd>

Das Handle des Heaps, dem der Arbeitsspeicher zugeordnet wurde. Dies ist der Heap, mit dem eine APP an die Funktion " [**zugewiescateheap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) " übermittelt wurde, als der Arbeitsspeicher belegt wurde.

</dd> <dt>

*NewAddress* 
</dt> <dd>

Die neue Adresse des zugewiesenen Speichers.

</dd> <dt>

*Oldaddress* 
</dt> <dd>

Die alte Adresse des zuvor zugewiesenen Speichers.

</dd> <dt>

*NewSize* 
</dt> <dd>

Die neue Größe in Bytes, die vom Heap zugewiesen wird.

</dd> <dt>

*OldSize* 
</dt> <dd>

Die alte Größe in Bytes, die zuvor vom Heap zugewiesen wurden.

</dd> <dt>

*Quelle* 
</dt> <dd>

Die Quelle des Speichers, der von der Zuweisung für die Heap Zuordnung verwendet wurde.

In der folgenden Tabelle sind die möglichen Werte für den *Quell* Parameter aufgeführt, die in der *ntetw. h* -Header Datei definiert sind:



| Wert                                                                                                                                                                                                                                                                               | Bedeutung                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> Arbeits <dt>**Speicher \_ Von \_ Lookaside**</dt> <dt>1</dt> </dl>                                       | Arbeitsspeicher aus der Lookaside-Liste.<br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> Arbeits <dt>**Speicher \_ Aus \_ lowfrag**</dt> <dt>2</dt> </dl>                                             | Arbeitsspeicher vom Heap mit niedriger Fragmentierung.<br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> Arbeits <dt>**Speicher \_ Aus \_ mainpath**</dt> <dt>3</dt> </dl>                                          | Arbeitsspeicher vom Hauptcodepfad.<br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> Arbeits <dt> **Speicher \_ von \_ slowpath**</dt> <dt>4</dt> </dl> | Arbeitsspeicher von langsamer c.<br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> Arbeits <dt>**Speicher \_ Aus \_ ungültigem**</dt> <dt>5</dt> </dl>                                             | Ungültiger Arbeitsspeicher.<br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> Arbeits <dt>**Speicher \_ Aus \_ Segment \_ Heap**</dt> <dt>6</dt> </dl>                             | Dieser Wert ist für die zukünftige Verwendung reserviert und wird nie zurückgegeben.<br/> |



 

</dd> </dl>

Dieses Ereignis weist keine Parameter auf.

## <a name="remarks"></a>Bemerkungen

Das Ereignis **\_ \_ \_ realloc für das ETW-Heap Ereignis** wird bei allen Heap Zuordnungen protokolliert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Ntwmi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ablauf Verfolgungs Ereignisse für die Speicherverwaltung](memory-management-tracing-events.md)
</dt> </dl>

 

 
