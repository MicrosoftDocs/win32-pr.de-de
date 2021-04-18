---
description: Die ctransformoutputpin-Klasse implementiert eine Ausgabe-PIN, die von der ctransformfilter-Klasse verwendet wird.
ms.assetid: 76f9a981-8f0d-45d4-b901-c5ec5b5ac9ee
title: Ctransformoutputpin-Klasse (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c55c57fbec0a8441b80398370542d94b2b70c1ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371771"
---
# <a name="ctransformoutputpin-class"></a>Ctransformoutputpin-Klasse

![ctransformoutputpin-Klassenhierarchie](images/tfrm02.png)

Die- `CTransformOutputPin` Klasse implementiert eine Ausgabe-PIN, die von der [**ctransformfilter**](ctransformfilter.md) -Klasse verwendet wird.

In der Regel müssen Sie keine Ableitung von dieser Klasse durchführen. Die meisten Methoden in dieser Klasse können die entsprechenden Methoden der **ctransformfilter** -Klasse aufzurufen, die Sie überschreiben können. Wenn Sie von dieser Klasse ableiten, müssen Sie die [**ctransformfilter:: getpin**](ctransformfilter-getpin.md) -Methode des Filters überschreiben, um Instanzen ihrer abgeleiteten Klasse zu erstellen.

Diese Klasse macht die Schnittstellen **imediaseeking** und **imediaposition** über das [**cpospassthru**](cpospassthru.md) -Objekt verfügbar. Alle Suchanforderungen werden an den nächsten Filter Upstream weitergeleitet.



| Geschützte Member-Variablen                                               | BESCHREIBUNG                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**m \_ ptransformfilter**](ctransformoutputpin-m-ptransformfilter.md)    | Zeiger auf den besitzenden Filter.                            |
| Öffentliche Element Variablen                                                  | BESCHREIBUNG                                              |
| [**m \_ pposition**](ctransformoutputpin-m-pposition.md)                  | Hilfsobjekt, um Seek-Befehle zu übergeben.            |
| Öffentliche Methoden                                                           | BESCHREIBUNG                                              |
| [**Ctransformoutputpin**](ctransformoutputpin-ctransformoutputpin.md)   | Konstruktormethode.                                      |
| [**~ Ctransformoutputpin**](ctransformoutputpin--ctransformoutputpin.md) | Dekonstruktormethode.                                       |
| [**Check Connect**](ctransformoutputpin-checkconnect.md)                 | Bestimmt, ob eine PIN-Verbindung geeignet ist.         |
| [**Breakconnect**](ctransformoutputpin-breakconnect.md)                 | Gibt die PIN von einer Verbindung frei.                      |
| [**Completeconnect**](ctransformoutputpin-completeconnect.md)           | Schließt eine Verbindung mit einer anderen Pin ab.                   |
| [**Checkmediatype**](ctransformoutputpin-checkmediatype.md)             | Bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.     |
| [**Setmediatype**](ctransformoutputpin-setmediatype.md)                 | Legt den Medientyp für die Verbindung fest.                  |
| [**Decidebuffersize**](ctransformoutputpin-decidebuffersize.md)         | Legt die Puffer Anforderungen fest.                            |
| [**Getmediatype**](ctransformoutputpin-getmediatype.md)                 | Ruft einen bevorzugten Medientyp nach Indexwert ab.        |
| [**Currentmediatype**](ctransformoutputpin-currentmediatype.md)         | Ruft den Medientyp für die aktuelle PIN-Verbindung ab. |
| IPin-Methoden                                                             | BESCHREIBUNG                                              |
| [**QueryId**](ctransformoutputpin-queryid.md)                           | Ruft einen Bezeichner für die PIN ab.                     |
| Iqualitycontrol-Methoden                                                  | BESCHREIBUNG                                              |
| [**Benachrichtigen**](ctransformoutputpin-notify.md)                             | Benachrichtigt die PIN, dass eine Qualitätsänderung angefordert wird.     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




