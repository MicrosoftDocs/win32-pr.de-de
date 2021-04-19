---
description: Implementiert eine Zuweisung, die die imemzuordcator-Schnittstelle unterstützt.
ms.assetid: c40eccef-d915-4bf3-81b2-b20e000718fb
title: Cmemzuordcator-Klasse (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adf390b7abf8fcbdb017ecde04bde76bf4bc001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372425"
---
# <a name="cmemallocator-class"></a>Cmemzuordcator-Klasse

![cmemzuordcator-Klassenhierarchie](images/filter10.png)

Implementiert eine Zuweisung, die die [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle unterstützt.

Diese Klasse wird von [**cbasezucator**](cbaseallocator.md)abgeleitet. Weitere Informationen zu Zuordnungen finden Sie in der Dokumentation zu [**cbasezuweisung**](cbaseallocator.md).



| Geschützte Member-Variablen                              | BESCHREIBUNG                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [**m \_ pbuffer**](cmemallocator-m-pbuffer.md)           | Zeiger auf den Speicherblock, der die Puffer enthält.                   |
| Geschützte Methoden                                       | BESCHREIBUNG                                                              |
| [**Kostenlos**](cmemallocator-free.md)                      | Platzhalter Methode; wird während eines Decommit-Vorgangs aufgerufen.                  |
| [**Kostenlos**](cmemallocator-reallyfree.md)          | Gibt den Arbeitsspeicher für die Puffer frei.                                     |
| [**Zuordnungseinheits**](cmemallocator-alloc.md)                    | Belegt Speicher für die Puffer.                                        |
| Öffentliche Methoden                                          | BESCHREIBUNG                                                              |
| [**Cmemzuordcator**](cmemallocator-cmemallocator.md)    | Konstruktormethode.                                                      |
| [**~ Cmemzuordcator**](cmemallocator--cmemallocator.md) | Dekonstruktormethode.                                                       |
| [**CreateInstance**](cmemallocator-createinstance.md)  | Erstellt eine neue Instanz der **cmemzuordcator** -Klasse.                   |
| Imemzuordcator-Methoden                                   | BESCHREIBUNG                                                              |
| [**SetProperties**](cmemallocator-setproperties.md)    | Gibt die Anzahl der zuzuordnenden Puffer und die Größe der einzelnen Puffer an. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Bereitstellen einer benutzerdefinierten Zuweisung](providing-a-custom-allocator.md)
</dt> </dl>

 

 




