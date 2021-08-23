---
description: Die KLASSE CABEvent ist ein Wrapper für Ereignisse mit manueller und automatischer Zurücksetzung.
ms.assetid: 228b4e51-afc5-4cb6-b225-309013713983
title: CABEvent-Klasse (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea87239628f001feaa82f84ca8c50941b56d3eb99f486934b551e832d1f588c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955529"
---
# <a name="camevent-class"></a>WEBCAMEvent-Klasse

![camevent-Klassenhierarchie](images/util06.png)

Die **KLASSE CABEvent** ist ein Wrapper für Ereignisse mit manueller und automatischer Zurücksetzung.

Diese Klasse bietet eine praktische Möglichkeit, Ereignisse zu verwalten, anstatt Funktionen wie [**CreateEvent,**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)und [**ResetEvent aufzurufen.**](/windows/desktop/api/synchapi/nf-synchapi-resetevent)



| Geschützte Membervariablen                          | Beschreibung                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [**m \_ hEvent**](camevent-m-hevent.md)              | Ereignishandle.                                                   |
| Öffentliche Methoden                                      | Beschreibung                                                     |
| [**WEBCAMEvent**](camevent-camevent.md)               | Konstruktormethode.                                             |
| [**~WEBCAMEvent**](camevent--camevent.md)             | Destruktormethode.                                              |
| [**prüfen**](camevent-check.md)                     | Überprüft, ob das Ereignis ohne Blockierung festgelegt ist.              |
| [**Zurücksetzen**](camevent-reset.md)                     | Legt den Zustand des Ereignisses auf nicht signalisiert fest.                     |
| [**Festgelegt**](camevent-set.md)                         | Signalisiert das Ereignis.                                              |
| [**Wait**](camevent-wait.md)                       | Blockiert, bis das Ereignis signalisiert wird, oder bis ein Time out auftritt. |
| Operatoren                                           | Beschreibung                                                     |
| [**Operator HANDLE**](camevent-operator-handle.md) | Ruft das Ereignishandle ab.                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

