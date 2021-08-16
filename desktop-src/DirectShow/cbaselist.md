---
description: Die CBaseList-Methode implementiert eine abtract-Liste. Die CGenericList-Klassenvorlage, die von CBaseList stammt, bietet Typüberprüfung und eine einfachere Schnittstelle als die CBaseList-Klasse.
ms.assetid: 372ee6f7-be0c-469f-92b3-673970ebd6da
title: CBaseList-Klasse (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5616edd16921bb2ae4d1a0b7ad67f5bbec3fba560594d4710512bd2cec6f275f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823705"
---
# <a name="cbaselist-class"></a>CBaseList-Klasse

![cbaselist-Klassenhierarchie](images/list01.png)

Die **CBaseList-Methode** implementiert eine abtract-Liste. Die [**CGenericList-Klassenvorlage,**](cgenericlist.md) die von **CBaseList** ableitung, bietet Typüberprüfung und eine einfachere Schnittstelle als die **CBaseList-Klasse.**

Die **CBaseList-Klasse** wird nach der **CObList-Klasse** in der Microsoft Foundation Classes (MFC)-Bibliothek modelliert. Positionen in der Liste werden durch eine POSITION-Struktur dargestellt. Der Aufrufer sollte nicht auf die internen Member der POSITION-Struktur zugreifen. behandeln Sie es als Zeiger auf einen Listenknoten. Die Position eines Objekts in der Liste bleibt gültig, bis das Objekt gelöscht wird.

Die Liste erfordert keine Unterstützung durch die in ihr enthaltenen Objekte. Er führt keine Speicherverwaltung oder kein Kopieren der Objekte durch. Objekte können in mehreren Listen enthalten sein.

Ungefähr die Hälfte der Methoden in dieser Klasse agieren auf einzelne Objekte. Diese Methoden haben das Suffix I im Methodennamen. Die anderen Methoden wirken sich auf ganze Listen aus. Beispielsweise fügt die [**CBaseList::AddAfter-Methode**](cbaselist-addafter.md) eine Liste an eine andere Liste an. Einzelobjektvorgänge geben POSITION-Werte oder **NULL bei** Einem Fehler zurück. Listenvorgänge geben **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**



| Geschützte Membervariablen                             | Beschreibung                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------|
| [**m \_ Count**](cbaselist-m-count.md)                  | Anzahl der Elemente in der Liste.                                              |
| [**m \_ pFirst**](cbaselist-m-pfirst.md)                | Zeiger auf den ersten Knoten in der Liste.                                    |
| [**m \_ pLast**](cbaselist-m-plast.md)                  | Zeiger auf den letzten Knoten in der Liste.                                     |
| Geschützte Methoden                                      | Beschreibung                                                               |
| [**GetNextI**](cbaselist-getnexti.md)                 | Ruft das Element an der angegebenen Position ab und verfeinert die Position.  |
| [**GetI**](cbaselist-geti.md)                         | Ruft das Element an der angegebenen Position ab.                             |
| [**FindI**](cbaselist-findi.md)                       | Ruft die erste Position ab, die das angegebene Element enthält.               |
| [**RemoveHeadI**](cbaselist-removeheadi.md)           | Entfernt das erste Element in der Liste.                                       |
| [**RemoveTailI**](cbaselist-removetaili.md)           | Entfernt das letzte Element in der Liste.                                        |
| [**RemoveI**](cbaselist-removei.md)                   | Entfernt das Element an der angegebenen Position.                               |
| [**AddTailI**](cbaselist-addtaili.md)                 | Fügt am Ende der Liste ein Element hinzu.                                      |
| [**AddHeadI**](cbaselist-addheadi.md)                 | Fügt am Ende der Liste ein Element hinzu.                                    |
| [**AddAfterI**](cbaselist-addafteri.md)               | Fügt ein Element nach der angegebenen Position ein.                             |
| [**AddBeforeI**](cbaselist-addbeforei.md)             | Fügt ein Element vor der angegebenen Position ein.                            |
| Öffentliche Methoden                                         | Beschreibung                                                               |
| [**CBaseList**](cbaselist-cbaselist.md)               | Konstruktormethode.                                                       |
| [**~ CBaseList**](cbaselist--cbaselist.md)            | Destruktormethode.                                                        |
| [**Removeall**](cbaselist-removeall.md)               | Entfernt alle Knoten aus der Liste.                                          |
| [**GetHeadPositionI**](cbaselist-getheadpositioni.md) | Ruft die Position des ersten Elements in der Liste ab.                     |
| [**GetTailPositionI**](cbaselist-gettailpositioni.md) | Ruft die Position des letzten Elements der Liste ab.                      |
| [**GetCountI**](cbaselist-getcounti.md)               | Ruft die Anzahl der Elemente in der Liste ab.                                |
| [**Weiter**](cbaselist-next.md)                         | Ruft die nächste Position in der Liste ab.                                  |
| [**Zurück**](cbaselist-prev.md)                         | Ruft die vorherige Position in der Liste ab.                              |
| [**AddHead**](cbaselist-addhead.md)                   | Fügt am Anfang dieser Liste eine weitere Liste ein.                           |
| [**AddTail**](cbaselist-addtail.md)                   | Fügt am Ende dieser Liste eine weitere Liste an.                             |
| [**Addafter**](cbaselist-addafter.md)                 | Fügt eine Liste nach der angegebenen Position ein.                              |
| [**Addbefore**](cbaselist-addbefore.md)               | Fügt eine Liste vor der angegebenen Position ein.                             |
| [**MoveToTail**](cbaselist-movetotail.md)             | Teilt die Liste auf und fügt den Hauptteil an das Ende einer anderen Liste an. |
| [**MoveToHead**](cbaselist-movetohead.md)             | Teilt die Liste auf und fügt den Endteil am Anfang einer anderen Liste ein. |
| [**Rückwärts**](cbaselist-reverse.md)                   | Kehrt die Reihenfolge der Liste um.                                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DirectShow-Basisklassen](directshow-base-classes.md)
</dt> </dl>

 

 




