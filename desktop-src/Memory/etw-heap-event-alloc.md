---
description: Ablauf Verfolgungs Ereignis für die Speicherverwaltung für einen Heap Zuordnungs Vorgang.
ms.assetid: 572DEC3B-F909-45E5-849F-707AA62F2F5E
title: ETW_HEAP_EVENT_ALLOC-Ereignis (ntwmi. h)
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
ms.openlocfilehash: 57e09ed1785f31b6203c526f2b6d42cc4815a266
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343619"
---
# <a name="etw_heap_event_alloc-event"></a>Ereignis für etw- \_ Heap \_ Ereignis \_ Zuweisung

Das Ereignis **\_ \_ \_ Zuweisungs Ereignis für das ETW-Heap Ereignis** ist ein Ablauf Verfolgungs Ereignis der Speicherverwaltung für einen Heap Zuordnungs Vorgang.


```C++
typedef struct ETW_HEAP_EVENT_ALLOC
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Heaphandle* 
</dt> <dd>

Das Handle des Heaps, dem der Arbeitsspeicher zugeordnet wurde. Dies ist der Heap, mit dem eine APP an die Funktion " [**zugewiescateheap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) " übermittelt wurde, als der Arbeitsspeicher belegt wurde.

</dd> <dt>

*Größe* 
</dt> <dd>

Die Größe in Bytes, die vom Heap zugewiesen wird.

</dd> <dt>

*Adresse* 
</dt> <dd>

Die Adresse des zugeordneten Arbeitsspeichers.

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
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> Arbeits <dt> **Speicher \_ von \_ slowpath**</dt> <dt>4</dt> </dl> | Der Arbeitsspeicher von einem langsamen Pfad.<br/>                                            |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> Arbeits <dt>**Speicher \_ Aus \_ ungültigem**</dt> <dt>5</dt> </dl>                                             | Ungültiger Arbeitsspeicher.<br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> Arbeits <dt>**Speicher \_ Aus \_ Segment \_ Heap**</dt> <dt>6</dt> </dl>                             | Dieser Wert ist für die zukünftige Verwendung reserviert und wird nie zurückgegeben.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das Ereignis Zuordnungs Ereignis für den etw-Heap wird bei allen Heap **\_ \_ \_ Zuordnungen** protokolliert.

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

 

 
