---
description: Implementiert eine Zuweisung, die die IMemAllocator-Schnittstelle unterstützt.
ms.assetid: c40eccef-d915-4bf3-81b2-b20e000718fb
title: CMemAllocator-Klasse (Amfilter.h)
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
ms.openlocfilehash: bb94d5fae92d7494a4ac347591e9d571a7765d2be88072559fd74687eea87e97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915930"
---
# <a name="cmemallocator-class"></a>CMemAllocator-Klasse

![cmemallocator-Klassenhierarchie](images/filter10.png)

Implementiert eine Zuweisung, die die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) unterstützt.

Diese Klasse wird von [**CBaseAllocator ableiten.**](cbaseallocator.md) Weitere Informationen zu Zuweisungen finden Sie in der Dokumentation zu [**CBaseAllocator.**](cbaseallocator.md)



| Geschützte Membervariablen                              | BESCHREIBUNG                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [**m \_ pBuffer**](cmemallocator-m-pbuffer.md)           | Zeiger auf den Speicherblock, der die Puffer enthält.                   |
| Geschützte Methoden                                       | BESCHREIBUNG                                                              |
| [**Kostenlos**](cmemallocator-free.md)                      | Platzhaltermethode; wird während eines Decommit-Vorgangs aufgerufen.                  |
| [**ReallyFree**](cmemallocator-reallyfree.md)          | Gibt den Arbeitsspeicher für die Puffer frei.                                     |
| [**Alloc**](cmemallocator-alloc.md)                    | Weist Arbeitsspeicher für die Puffer zu.                                        |
| Öffentliche Methoden                                          | BESCHREIBUNG                                                              |
| [**CMemAllocator**](cmemallocator-cmemallocator.md)    | Konstruktormethode.                                                      |
| [**~ CMemAllocator**](cmemallocator--cmemallocator.md) | Destruktormethode.                                                       |
| [**CreateInstance**](cmemallocator-createinstance.md)  | Erstellt eine neue Instanz der **CMemAllocator-Klasse.**                   |
| IMemAllocator-Methoden                                   | BESCHREIBUNG                                                              |
| [**SetProperties**](cmemallocator-setproperties.md)    | Gibt die Anzahl der zu reservierenden Puffer und die Größe der einzelnen Puffer an. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Bereitstellen einer benutzerdefinierten Zuweisung](providing-a-custom-allocator.md)
</dt> </dl>

 

 




