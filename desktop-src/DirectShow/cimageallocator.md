---
description: Die cimagezuordcator-Klasse implementiert einen Zuweiser, der GDI-geräteunabhängige Bitmaps (Disb) verwaltet. Diese Klasse wird von der cbasezucator-Klasse abgeleitet. Es werden Medien Beispiele erstellt, die mithilfe der cimagesample-Klasse implementiert werden.
ms.assetid: edda34a5-3916-4a41-9e2f-a19f12df0947
title: Cimagezuordcator-Klasse (winutil. h)
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
ms.openlocfilehash: ea37dfe8cbbc7baf90e6065f0c54af1a60c3284b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354050"
---
# <a name="cimageallocator-class"></a>Cimagezuordcator-Klasse

![cimagezuordnerklassenhierarchie](images/wutil04.png)

Die- `CImageAllocator` Klasse implementiert einen Zuweiser, der GDI-geräteunabhängige Bitmaps (Disb) verwaltet. Diese Klasse wird von der [**cbasezucator**](cbaseallocator.md) -Klasse abgeleitet. Es werden Medien Beispiele erstellt, die mithilfe der [**cimagesample**](cimagesample.md) -Klasse implementiert werden.

Eine Zuweisung wird von zwei verbundenen Pins gemeinsam genutzt, gehört aber immer zu einem der Filter in der Verbindung. Ein Filter, der verwendet, `CImageAllocator` muss nachverfolgen, ob die Zuweisung von sich selbst oder über den anderen Filter bereitgestellt wurde. Wenn die Zuweisung von sich selbst bereitgestellt wurde, kann sich der besitzende Filter auf die Tatsache verlassen, dass alle Medien Beispiele aus der Zuweisung **cimagesample** -Objekte sind. Daher kann das **cimagesample** -Objekt verwendet werden, um Informationen über das DIB zu erhalten, das in einer [**dibdata**](dibdata.md) -Struktur gespeichert ist.

Der besitzende Filter sollte immer dann **notifymediatype** anrufen, wenn sich der Medientyp ändert.



| Geschützte Member-Variablen                                     | BESCHREIBUNG                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| [**m \_ pFilter**](cimageallocator-m-pfilter.md)                | Zeiger auf den besitzenden Filter.                                            |
| [**m \_ pmediatype**](cimageallocator-m-pmediatype.md)          | Zeiger auf den aktuellen Medientyp.                                       |
| Geschützte Methoden                                              | BESCHREIBUNG                                                              |
| [**Zuordnungseinheits**](cimageallocator-alloc.md)                         | Belegt Speicher für die Puffer.                                        |
| [**Prüf Größen**](cimageallocator-checksizes.md)               | Überprüft zuordnereigenschaften auf den aktuellen Medientyp.              |
| [**"Kreatedib"**](cimageallocator-createdib.md)                 | Erstellt ein DIB.                                                           |
| [**"Kreateimagesample"**](cimageallocator-createimagesample.md) | Erstellt ein Medien Beispiel. Virtu.                                         |
| [**Kostenlos**](cimageallocator-free.md)                           | Gibt den gesamten Puffer Arbeitsspeicher frei.                                       |
| Öffentliche Methoden                                                 | BESCHREIBUNG                                                              |
| [**Cimagezuordcator**](cimageallocator-cimageallocator.md)     | Konstruktormethode.                                                      |
| [**Notifymediatype**](cimageallocator-notifymediatype.md)     | Informiert das-Objekt über den aktuellen Medientyp.                            |
| Imemzuordcator-Methoden                                          | BESCHREIBUNG                                                              |
| [**SetProperties**](cimageallocator-setproperties.md)         | Gibt die Anzahl der zuzuordnenden Puffer und die Größe der einzelnen Puffer an. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrawimage-Klasse**](cdrawimage.md)
</dt> </dl>

 

 




