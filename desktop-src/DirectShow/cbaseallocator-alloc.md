---
description: 'CBaseAllocator.Alloc-Methode: Die Alloc-Methode belegt Speicher für die Puffer.'
ms.assetid: a22c97ef-6a8d-4cad-b5a5-3e6b225f5c81
title: CBaseAllocator.Alloc-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 975f373136759a0950e5052413eccb501176e7876531208fd20380ee7d1fb10a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966710"
---
# <a name="cbaseallocatoralloc-method"></a>CBaseAllocator.Alloc-Methode

Die `Alloc` -Methode belegt Arbeitsspeicher für die Puffer.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Alloc();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück.



| Rückgabecode                                                                                       | Beschreibung                                      |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>           | Die Pufferanforderungen wurden nicht geändert.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>              | Die Pufferanforderungen haben sich geändert.<br/>     |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | Pufferanforderungen wurden nicht festgelegt.<br/>     |



 

## <a name="remarks"></a>Hinweise

Diese Methode wird von der [**CBaseAllocator::Commit-Methode**](cbaseallocator-commit.md) aufgerufen.

In der Basisklasse belegt diese Methode keinen Arbeitsspeicher. Es wird ein Fehler zurückgegeben, wenn die Pufferanforderungen nicht festgelegt wurden, S \_ FALSE, wenn sich die Anforderungen nicht geändert haben, und S \_ OK, wenn sich die Anforderungen geändert haben.

Eine abgeleitete Klasse sollte diese Methode überschreiben, um die tatsächliche Speicherbelegung durchzuführen. In der Regel führt die abgeleitete Klasse die folgenden Schritte aus:

1.  Rufen Sie die Basisklassenimplementierung auf, um zu bestimmen, ob der Arbeitsspeicher wirklich zugewiesen werden muss.
2.  Zuordnen von Arbeitsspeicher.
3.  Erstellen Sie [**CMediaSample-Objekte,**](cmediasample.md) die Speicherblöcke aus Schritt 2 enthalten.
4.  Fügen Sie jedes **CMediaSample-Objekt** der Liste der kostenlosen Beispiele hinzu ([**CBaseAllocator::m \_ lFree**](cbaseallocator-m-lfree.md)).

Ein Beispiel finden Sie unter [**CMemAllocator::Alloc**](cmemallocator-alloc.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseAllocator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




