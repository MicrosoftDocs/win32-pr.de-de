---
description: Die cbaselist-Methode implementiert eine abtraktions Liste. Die cgenericlist-Klassen Vorlage, die von cbaselist abgeleitet wird, bietet eine Typüberprüfung und eine einfachere Schnittstelle als die cbaselist-Klasse.
ms.assetid: 372ee6f7-be0c-469f-92b3-673970ebd6da
title: Cbaselist-Klasse (wxlist. h)
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
ms.openlocfilehash: c6aa4a3c80cd583bd3cc83a2a0adedecb6caaf7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372266"
---
# <a name="cbaselist-class"></a>Cbaselist-Klasse

![cbaselist-Klassenhierarchie](images/list01.png)

Die **cbaselist** -Methode implementiert eine abtraktions Liste. Die [**cgenericlist**](cgenericlist.md) -Klassen Vorlage, die von **cbaselist** abgeleitet wird, bietet eine Typüberprüfung und eine einfachere Schnittstelle als die **cbaselist** -Klasse.

Die **cbaselist** -Klasse wird nach der **CObList** -Klasse in der MFC-Bibliothek (Microsoft Foundation Classes) modelliert. Positionen in der Liste werden durch eine Positions Struktur dargestellt. Der Aufrufer sollte nicht auf die internen Member der Positions Struktur zugreifen. behandeln Sie ihn als Zeiger auf einen Listen Knoten. Die Position eines Objekts in der Liste bleibt gültig, bis das Objekt gelöscht wird.

Die Liste erfordert keine Unterstützung durch die darin enthaltenen Objekte. Es führt keine Speicherverwaltung oder das Kopieren der Objekte durch. Objekte können mehrere Listen aufweisen.

Ungefähr die Hälfte der Methoden in dieser Klasse agieren auf einzelne Objekte. Diese Methoden haben das Suffix-I im Methodennamen. Die anderen Methoden wirken sich auf ganze Listen aus. Beispielsweise fügt die [**cbaselist:: AddAfter**](cbaselist-addafter.md) -Methode eine Liste an eine andere Liste an. Einzelobjekt Vorgänge geben Positionswerte oder **null** bei einem Fehler zurück. Listen Vorgänge geben **true** zurück, wenn erfolgreich, andernfalls **false** .



| Geschützte Member-Variablen                             | BESCHREIBUNG                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------|
| [**m- \_ Anzahl**](cbaselist-m-count.md)                  | Anzahl der Elemente in der Liste.                                              |
| [**m \_ pfirst**](cbaselist-m-pfirst.md)                | Zeiger auf den ersten Knoten in der Liste.                                    |
| [**m- \_ pLast**](cbaselist-m-plast.md)                  | Zeiger auf den letzten Knoten in der Liste.                                     |
| Geschützte Methoden                                      | BESCHREIBUNG                                                               |
| [**Getnexti**](cbaselist-getnexti.md)                 | Ruft das Element an der angegebenen Position ab und erhöht die Position.  |
| [**TIS**](cbaselist-geti.md)                         | Ruft das Element an der angegebenen Position ab.                             |
| [**Findi**](cbaselist-findi.md)                       | Ruft die erste Position ab, die das angegebene Element enthält.               |
| [**Removeheadi**](cbaselist-removeheadi.md)           | Entfernt das erste Element in der Liste.                                       |
| [**Removetaili**](cbaselist-removetaili.md)           | Entfernt das letzte Element in der Liste.                                        |
| [**Removei**](cbaselist-removei.md)                   | Entfernt das Element an der angegebenen Position.                               |
| [**Addtaili**](cbaselist-addtaili.md)                 | Fügt ein Element am Ende der Liste hinzu.                                      |
| [**Addheadi**](cbaselist-addheadi.md)                 | Fügt ein Element am Anfang der Liste hinzu.                                    |
| [**Addaf-i**](cbaselist-addafteri.md)               | Fügt ein Element nach der angegebenen Position ein.                             |
| [**Addbeforei**](cbaselist-addbeforei.md)             | Fügt ein Element vor der angegebenen Position ein.                            |
| Öffentliche Methoden                                         | BESCHREIBUNG                                                               |
| [**Cbaselist**](cbaselist-cbaselist.md)               | Konstruktormethode.                                                       |
| [**~ Cbaselist**](cbaselist--cbaselist.md)            | Dekonstruktormethode.                                                        |
| [**RemoveAll**](cbaselist-removeall.md)               | Entfernt alle Knoten aus der Liste.                                          |
| [**Gezeige adpositioni**](cbaselist-getheadpositioni.md) | Ruft die Position des ersten Elements in der Liste ab.                     |
| [**Gettailpositioni**](cbaselist-gettailpositioni.md) | Ruft die Position des letzten Elements der Liste ab.                      |
| [**Getgräfin**](cbaselist-getcounti.md)               | Ruft die Anzahl der Elemente in der Liste ab.                                |
| [**Weiter**](cbaselist-next.md)                         | Ruft die nächste Position in der Liste ab.                                  |
| [**Prev**](cbaselist-prev.md)                         | Ruft die vorherige Position in der Liste ab.                              |
| [**AddHead**](cbaselist-addhead.md)                   | Fügt eine weitere Liste am Anfang der Liste ein.                           |
| [**AddTail**](cbaselist-addtail.md)                   | Fügt am Ende dieser Liste eine andere Liste an.                             |
| [**AddAfter**](cbaselist-addafter.md)                 | Fügt eine Liste nach der angegebenen Position ein.                              |
| [**AddBefore**](cbaselist-addbefore.md)               | Fügt eine Liste vor der angegebenen Position ein.                             |
| [**"Muveum"**](cbaselist-movetotail.md)             | Teilt die Liste und fügt den Head-Teil an das Ende einer anderen Liste an. |
| [**In den Kopf**](cbaselist-movetohead.md)             | Teilt die Liste auf und fügt den Teil Fragment an der Spitze einer anderen Liste ein. |
| [**Umgekehr**](cbaselist-reverse.md)                   | Kehrt die Reihenfolge der Liste um.                                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Basisklassen](directshow-base-classes.md)
</dt> </dl>

 

 




