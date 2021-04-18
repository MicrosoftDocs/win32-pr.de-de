---
description: Die cgenericlist-Klassen Vorlage, die eine typspezifische Liste implementiert. Weitere Informationen finden Sie unter cbaselist.
ms.assetid: 69067530-3a7d-4731-8ac6-9d02dbba8440
title: Cgenericlist-Klasse (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6de3a2dde8d4549221ef4f13decab167fcf6d560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371626"
---
# <a name="cgenericlist-class"></a>Cgenericlist-Klasse

![cgenericlist-Klassenhierarchie](images/list01.png)

Die `CGenericList` Klassen Vorlage, die eine typspezifische Liste implementiert. Weitere Informationen finden Sie unter [**cbaselist**](cbaselist.md).

Um diese Vorlage zu verwenden, deklarieren Sie eine Variable vom Typ `CGenericList` mit einem Vorlagen Argument, das den Objekttyp in der Liste definiert. Die folgende Anweisung deklariert beispielsweise eine Liste von [**cbasefilter**](cbasefilter.md) -Objekten:


```
CGenericList<CBaseFilter> myFilterList("Filters"); 
```



Aus praktischer Gründen definiert wxlist. h die folgenden Listen Typen:

``` syntax
typedef CGenericList<CBaseObject> CBaseObjectList;
typedef CGenericList<IUnknown> CBaseInterfaceList;
```



| Öffentliche Methoden                                          | BESCHREIBUNG                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [**Cgenericlist**](cgenericlist-cgenericlist.md)       | Konstruktormethode.                                                      |
| [**~ Cgenericlist**](cgenericlist--cgenericlist.md)     | Dekonstruktormethode.                                                       |
| [**Gezeige-Position**](cgenericlist-getheadposition.md) | Ruft die Position des ersten Elements in der Liste ab.                    |
| [**Gettailposition**](cgenericlist-gettailposition.md) | Ruft die Position des letzten Elements der Liste ab.                     |
| [**GetCount**](cgenericlist-getcount.md)               | Ruft die Anzahl der Elemente in der Liste ab.                               |
| [**GetNext**](cgenericlist-getnext.md)                 | Ruft das Element an der angegebenen Position ab und erhöht die Position. |
| [**Erhalten**](cgenericlist-get.md)                         | Ruft das Element an der angegebenen Position ab.                            |
| [**Gezeige AD**](cgenericlist-gethead.md)                 | Ruft das Element am Anfang der Liste ab.                              |
| [**RemoveHead**](cgenericlist-removehead.md)           | Entfernt das erste Element in der Liste.                                      |
| [**Removetail**](cgenericlist-removetail.md)           | Entfernt das letzte Element in der Liste.                                       |
| [**Aufgeh**](cgenericlist-remove.md)                   | Entfernt das Element an der angegebenen Position.                              |
| [**AddBefore**](cgenericlist-addbefore.md)             | Fügt ein Element oder eine Liste vor der angegebenen Position ein.                   |
| [**AddAfter**](cgenericlist-addafter.md)               | Fügt ein Element oder eine Liste nach der angegebenen Position ein.                    |
| [**AddHead**](cgenericlist-addhead.md)                 | Fügt ein Element oder eine Liste am Anfang der Liste hinzu.                           |
| [**AddTail**](cgenericlist-addtail.md)                 | Fügt ein Element oder eine Liste an das Ende der Liste an.                          |
| [**Sich**](cgenericlist-find.md)                       | Ruft die erste Position ab, die das angegebene Element enthält.              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




