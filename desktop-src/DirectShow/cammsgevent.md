---
description: Die KLASSE OEMMsgEvent ist ein Wrapper für Ereignisobjekte, die die Nachrichtenverarbeitung ausführen.
ms.assetid: 4b94febe-169f-4f04-be93-043a8c75e3b4
title: OEMMsgEvent-Klasse (Wxutil.h)
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
ms.openlocfilehash: c7c4d3c8268f06e81d1bd1a5285f7e4785459889397ccf249bbde7f0dd627f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955434"
---
# <a name="cammsgevent-class"></a>CAMMsgEvent-Klasse

![msgevent-Klassenhierarchie](images/util06.png)

Die `CAMMsgEvent` -Klasse ist ein Wrapper für Ereignisobjekte, die die Nachrichtenverarbeitung ausführen.

Diese Klasse wird vom [**OBJEKT "WEBCAMEvent"**](camevent.md) ableiten. Sie fügt eine Methode hinzu, [**DIEMsgEvent::WaitMsg,**](cammsgevent-waitmsg.md)die eingehende Nachrichten während des Wartens weitersingend.



| Öffentliche Methoden                                 | Beschreibung                                                          |
|------------------------------------------------|----------------------------------------------------------------------|
| [**CAMMsgEvent**](cammsgevent-cammsgevent.md) | Konstruktor.                                                         |
| [**WaitMsg**](cammsgevent-waitmsg.md)         | Wartet, bis das Ereignis signalisiert wird, während gesendete Nachrichten gesendet werden. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




