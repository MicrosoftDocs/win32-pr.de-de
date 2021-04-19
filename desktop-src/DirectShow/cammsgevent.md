---
description: Die "cammsgevent"-Klasse ist ein Wrapper für Ereignis Objekte, die die Nachrichtenverarbeitung durchführen.
ms.assetid: 4b94febe-169f-4f04-be93-043a8c75e3b4
title: Cammsgevent-Klasse (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ebac7aae11f7a7b7d6b846e262e93b5759210b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367084"
---
# <a name="cammsgevent-class"></a>Cammsgevent-Klasse

![cammsgevent-Klassenhierarchie](images/util06.png)

Die- `CAMMsgEvent` Klasse ist ein Wrapper für Ereignis Objekte, die die Nachrichtenverarbeitung durchführen.

Diese Klasse wird vom [**camevent**](camevent.md) -Objekt abgeleitet. Es wird eine Methode hinzugefügt, " [**cammsgevent:: waitmsg**](cammsgevent-waitmsg.md)", die eingehende Nachrichten während des Wartens sendet.



| Öffentliche Methoden                                 | BESCHREIBUNG                                                          |
|------------------------------------------------|----------------------------------------------------------------------|
| [**Cammsgevent**](cammsgevent-cammsgevent.md) | Konstruktor.                                                         |
| [**Waitmsg**](cammsgevent-waitmsg.md)         | Wartet, bis das-Ereignis signalisiert wird, während gesendete Nachrichten versendet werden. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




