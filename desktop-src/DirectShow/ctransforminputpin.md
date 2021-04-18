---
description: Die ctransforminputpin-Klasse implementiert eine Eingabe-PIN, die von der ctransformfilter-Klasse verwendet wird.
ms.assetid: 032da1bb-448d-48ea-ab3d-f721d790637f
title: Ctransforminputpin-Klasse (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6cbfad0a33384249ab474d6376ffc110294bca6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354820"
---
# <a name="ctransforminputpin-class"></a>Ctransforminputpin-Klasse

![ctransforminputpin-Klassenhierarchie](images/tfrm01.png)

Die- `CTransformInputPin` Klasse implementiert eine Eingabe-PIN, die von der [**ctransformfilter**](ctransformfilter.md) -Klasse verwendet wird.

In der Regel müssen Sie keine Ableitung von dieser Klasse durchführen. Die meisten Methoden in dieser Klasse können die entsprechenden Methoden der **ctransformfilter** -Klasse aufzurufen, die Sie überschreiben können. Wenn Sie von dieser Klasse ableiten, müssen Sie die [**ctransformfilter:: getpin**](ctransformfilter-getpin.md) -Methode des Filters überschreiben, um Instanzen ihrer abgeleiteten Klasse zu erstellen.



| Geschützte Member-Variablen                                           | BESCHREIBUNG                                                                            |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ ptransformfilter**](ctransforminputpin-m-ptransformfilter.md) | Zeiger auf den besitzenden Filter.                                                          |
| Öffentliche Methoden                                                       | BESCHREIBUNG                                                                            |
| [**Ctransforminputpin**](ctransforminputpin-ctransforminputpin.md)  | Konstruktormethode.                                                                    |
| [**Check Connect**](ctransforminputpin-checkconnect.md)              | Bestimmt, ob eine PIN-Verbindung geeignet ist.                                       |
| [**Breakconnect**](ctransforminputpin-breakconnect.md)              | Gibt die PIN von einer Verbindung frei.                                                    |
| [**Completeconnect**](ctransforminputpin-completeconnect.md)        | Schließt eine Verbindung mit einer anderen Pin ab.                                                 |
| [**Checkmediatype**](ctransforminputpin-checkmediatype.md)          | Bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.                                   |
| [**Setmediatype**](ctransforminputpin-setmediatype.md)              | Legt den Medientyp für die Verbindung fest.                                                |
| [**Checkstreaming**](ctransforminputpin-checkstreaming.md)          | Bestimmt, ob die PIN Beispiele annehmen kann. Virtu.                                |
| [**Currentmediatype**](ctransforminputpin-currentmediatype.md)      | Ruft den Medientyp für die aktuelle PIN-Verbindung ab.                               |
| IPin-Methoden                                                         | BESCHREIBUNG                                                                            |
| [**QueryId**](ctransforminputpin-queryid.md)                        | Ruft einen Bezeichner für die PIN ab.                                                   |
| [**EndOfStream**](ctransforminputpin-endofstream.md)                | Benachrichtigt die PIN, dass keine weiteren Daten erwartet werden.                                  |
| [**Beginflush**](ctransforminputpin-beginflush.md)                  | Startet einen Löschvorgang.                                                              |
| [**Endflush**](ctransforminputpin-endflush.md)                      | Beendet einen Löschvorgang.                                                                |
| [**Newsegment**](ctransforminputpin-newsegment.md)                  | Benachrichtigt die PIN, dass nach diesem-Befehl empfangene Medien Beispiele als Segment gruppiert werden. |
| IMemInputPin-Methoden                                                 | BESCHREIBUNG                                                                            |
| [**Medizinisch**](ctransforminputpin-receive.md)                        | Empfängt das nächste Medien Beispiel im Stream.                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




