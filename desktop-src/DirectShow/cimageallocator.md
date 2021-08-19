---
description: Die CImageAllocator-Klasse implementiert eine Zuweisung, die geräteunabhängige GDI-Bitmaps (DIBs) verwaltet. Diese Klasse wird von der CBaseAllocator-Klasse ableiten. Es werden Medienbeispiele erstellt, die mithilfe der CImageSample-Klasse implementiert werden.
ms.assetid: edda34a5-3916-4a41-9e2f-a19f12df0947
title: CImageAllocator-Klasse (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 383b9c2ca992db66e7bf397e42dcb8aaaa4bdb66251ddfd67f4b5175d87058aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402582"
---
# <a name="cimageallocator-class"></a>CImageAllocator-Klasse

![cimageallocator-Klassenhierarchie](images/wutil04.png)

Die `CImageAllocator` -Klasse implementiert eine Zuweisung, die geräteunabhängige GDI-Bitmaps (DIBs) verwaltet. Diese Klasse wird von der [**CBaseAllocator-Klasse**](cbaseallocator.md) ableiten. Es werden Medienbeispiele erstellt, die mithilfe der [**CImageSample-Klasse implementiert**](cimagesample.md) werden.

Eine Zuweisung wird von zwei verbundenen Pins gemeinsam genutzt, befindet sich aber immer im Besitz eines der Filter in der Verbindung. Ein Filter, der verwendet, muss nachverfolgen, ob die Zuweisung allein oder `CImageAllocator` durch den anderen Filter bereitgestellt wurde. Wenn die Zuweisung selbst bereitgestellt wurde, kann sich der besitzende Filter darauf verlassen, dass alle Medienbeispiele aus der Zuweisung **CImageSample-Objekte** sind. Daher kann das **CImageSample-Objekt verwendet** werden, um Informationen über den DIB zu erhalten, der in einer [**DIBDATA-Struktur gespeichert**](dibdata.md) ist.

Der besitzende Filter sollte **NotifyMediaType aufrufen,** wenn sich der Medientyp ändert.



| Geschützte Membervariablen                                     | Beschreibung                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| [**m \_ pFilter**](cimageallocator-m-pfilter.md)                | Zeiger auf den besitzenden Filter.                                            |
| [**m \_ pMediaType**](cimageallocator-m-pmediatype.md)          | Zeiger auf den aktuellen Medientyp.                                       |
| Geschützte Methoden                                              | Beschreibung                                                              |
| [**Alloc**](cimageallocator-alloc.md)                         | Weist Arbeitsspeicher für die Puffer zu.                                        |
| [**CheckSizes**](cimageallocator-checksizes.md)               | Überprüft Zuweisungseigenschaften mit dem aktuellen Medientyp.              |
| [**CreateDIB**](cimageallocator-createdib.md)                 | Erstellt einen DIB.                                                           |
| [**CreateImageSample**](cimageallocator-createimagesample.md) | Erstellt ein Medienbeispiel. Virtuellen.                                         |
| [**Kostenlos**](cimageallocator-free.md)                           | Gibt den pufferspeicher frei.                                       |
| Öffentliche Methoden                                                 | Beschreibung                                                              |
| [**CImageAllocator**](cimageallocator-cimageallocator.md)     | Konstruktormethode.                                                      |
| [**NotifyMediaType**](cimageallocator-notifymediatype.md)     | Informiert das -Objekt über den aktuellen Medientyp.                            |
| IMemAllocator-Methoden                                          | Beschreibung                                                              |
| [**SetProperties**](cimageallocator-setproperties.md)         | Gibt die Anzahl der zu reservierenden Puffer und die Größe der einzelnen Puffer an. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDrawImage-Klasse**](cdrawimage.md)
</dt> </dl>

 

 




