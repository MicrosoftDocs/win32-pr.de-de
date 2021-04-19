---
description: Die "camevent"-Klasse ist ein Wrapper für Ereignisse für manuelles Zurücksetzen und automatisches Zurücksetzen.
ms.assetid: 228b4e51-afc5-4cb6-b225-309013713983
title: Camevent-Klasse (wxutil. h)
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
ms.openlocfilehash: bde2db8adf2bb713df665e06eb2cc5f8d2a9a00f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370027"
---
# <a name="camevent-class"></a>Camevent-Klasse

![camevent-Klassenhierarchie](images/util06.png)

Die " **camevent** "-Klasse ist ein Wrapper für Ereignisse für manuelles Zurücksetzen und automatisches Zurücksetzen.

Diese Klasse bietet eine bequeme Möglichkeit, Ereignisse zu verwalten, anstatt Funktionen wie [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)und [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent)aufrufen zu müssen.



| Geschützte Member-Variablen                          | BESCHREIBUNG                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [**m \_ hevent**](camevent-m-hevent.md)              | Ereignis handle.                                                   |
| Öffentliche Methoden                                      | BESCHREIBUNG                                                     |
| [**Camevent**](camevent-camevent.md)               | Konstruktormethode.                                             |
| [**~ Camevent**](camevent--camevent.md)             | Dekonstruktormethode.                                              |
| [**Azure Functions**](camevent-check.md)                     | Überprüft, ob das Ereignis festgelegt ist, ohne zu blockieren.              |
| [**Zurücksetzen**](camevent-reset.md)                     | Legt den Zustand des Ereignisses auf "nicht signalisiert" fest.                     |
| [**Set**](camevent-set.md)                         | Signalisiert das Ereignis.                                              |
| [**Wait**](camevent-wait.md)                       | Blockiert, bis das-Ereignis signalisiert wird, oder bis ein Timeout auftritt. |
| Operatoren                                           | Beschreibung                                                     |
| [**Operator handle**](camevent-operator-handle.md) | Ruft das Ereignis Handle ab.                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

