---
description: Die CSource-Klasse ist eine Basisklasse zum Implementieren von Quell filtern. Ein von CSource abgeleiteter Filter enthält eine oder mehrere aus der csourcestream-Klasse abgeleitete Ausgabe Pins. Jede Ausgabepin erstellt einen Arbeits Thread, der die Medien Beispiele nach unten verschiebt.
ms.assetid: 25bd0334-4ad1-48ed-93f9-b36c13a280a3
title: CSource-Klasse (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4fcecbd1973c54e30c9bf1251bed174aa4a469f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368588"
---
# <a name="csource-class"></a>CSource-Klasse

![CSource-Klassenhierarchie](images/source01.png)

Die **CSource** -Klasse ist eine Basisklasse zum Implementieren von Quell filtern. Ein von **CSource** abgeleiteter Filter enthält eine oder mehrere aus der [**csourcestream**](csourcestream.md) -Klasse abgeleitete Ausgabe Pins. Jede Ausgabepin erstellt einen Arbeits Thread, der die Medien Beispiele nach unten verschiebt.

> [!Note]  
> Die **CSource** -Klasse unterstützt das Push-Modell für den Datenfluss. Diese Klasse wird nicht zum Erstellen von Datei Leser Filtern empfohlen. Datei Reader sollten das Pull-Modell über die [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle unterstützen. Weitere Informationen finden Sie unter [Datenfluss für Filter Entwickler](data-flow-for-filter-developers.md).

 



| Geschützte Member-Variablen                     | BESCHREIBUNG                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [**m- \_ ipins**](csource-m-ipins.md)            | Anzahl der Pins für den Filter.                                |
| [**m- \_ Paare**](csource-m-pastreams.md)    | Array von Pins.                                               |
| [**m \_ cstatus**](csource-m-cstatelock.md)  | Kritisches Abschnitts Objekt, das den Filter Zustand schützt.      |
| Öffentliche Methoden                                 | BESCHREIBUNG                                                  |
| [**CSource**](csource-csource.md)             | Konstruktormethode.                                          |
| [**~ CSource**](csource--csource.md)           | Dekonstruktormethode.                                           |
| [**Getpincount**](csource-getpincount.md)     | Ruft die Anzahl der Pins für den Filter ab.                  |
| [**Getpin**](csource-getpin.md)               | Ruft eine PIN ab.                                             |
| [**pstatus-Datei**](csource--pstatelock.md)      | Ruft einen Zeiger auf das kritische Abschnitts Objekt des Filters ab. |
| [**Addpin**](csource-addpin.md)               | Fügt dem Filter eine neue Ausgabe-PIN hinzu.                         |
| [**Removepin**](csource-removepin.md)         | Entfernt eine angegebene PIN aus dem Filter.                     |
| [**Findpinnumber**](csource-findpinnumber.md) | Ruft die Nummer einer angegebenen PIN für den Filter ab.       |
| Ibasefilter-Methoden                            | BESCHREIBUNG                                                  |
| [**Findpin**](csource-findpin.md)             | Ruft die PIN mit dem angegebenen Bezeichner ab.             |



 

## <a name="remarks"></a>Bemerkungen

Gehen Sie folgendermaßen vor, um eine Ausgabe-PIN zu implementieren:

-   Leiten Sie eine Klasse von [**csourcestream**](csourcestream.md)ab.
-   Überschreiben Sie die [**csourcestream:: getmediatype**](csourcestream-getmediatype.md) -Methode und möglicherweise die [**csourcestream:: checkmediatype**](csourcestream-checkmediatype.md) -Methode, die die Medientypen für die PIN überprüfen.
-   Implementieren Sie die [**cbaseoutputpin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) -Methode, die die Puffer Anforderungen der PIN zurückgibt.
-   Implementieren Sie die [**csourcestream:: FillBuffer**](csourcestream-fillbuffer.md) -Methode, die einen Medien Beispiel Puffer mit Daten füllt.

Gehen Sie folgendermaßen vor, um den Filter zu implementieren:

-   Leiten Sie eine Klasse von **CSource** ab.
-   Erstellen Sie im Konstruktor eine oder mehrere aus [**csourcestream**](csourcestream.md)abgeleitete Ausgabe Pins. Die Pins fügen sich automatisch dem Filter in den Konstruktormethoden hinzu und entfernen sich selbst in ihren demarkermethoden.

Um den Filter Zustand zwischen mehreren Threads zu synchronisieren, müssen Sie die [**CSource::p statelock**](csource--pstatelock.md) -Methode aufrufen. Diese Methode gibt einen Zeiger auf den kritischen Abschnitt des Filter Zustands zurück. Verwenden Sie die [**cautolock**](cautolock.md) -Klasse, um den kritischen Abschnitt zu halten. Von einer PIN aus können Sie wie folgt aus der [**cbasepin:: m \_ pFilter**](cbasepin-m-pfilter.md) -Element Variablen der PIN auf **pstatus-ck** zugreifen:


```
CAutoLock lock(m_pFilter->pStateLock());
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schreiben von Quell Filtern](writing-source-filters.md)
</dt> </dl>

 

 




