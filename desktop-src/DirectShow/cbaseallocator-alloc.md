---
description: Die Methode "Zuweisung" weist Speicher für die Puffer zu.
ms.assetid: a22c97ef-6a8d-4cad-b5a5-3e6b225f5c81
title: Cbasezucator. Zuordnungsmethode (amfilter. h)
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
ms.openlocfilehash: b7510a108e69eb218a894b67dd5b62d94bfdbe6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367415"
---
# <a name="cbaseallocatoralloc-method"></a>Cbasezucator. Zuordnungsmethode

Die- `Alloc` Methode weist Speicher für die Puffer zu.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Alloc();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück.



| Rückgabecode                                                                                       | Beschreibung                                      |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>           | Die Puffer Anforderungen wurden nicht geändert.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>              | Die Puffer Anforderungen wurden geändert.<br/>     |
| <dl> <dt>**VFW \_ E \_ sizenotset**</dt> </dl> | Die Puffer Anforderungen wurden nicht festgelegt.<br/>     |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode wird von der [**cbasezucator:: Commit**](cbaseallocator-commit.md) -Methode aufgerufen.

In der-Basisklasse weist diese Methode keinen Arbeitsspeicher zu. Es wird ein Fehler zurückgegeben, wenn die Puffer Anforderungen nicht festgelegt wurden, s \_ false, wenn die Anforderungen nicht geändert wurden, und s \_ OK, wenn sich die Anforderungen geändert haben.

Eine abgeleitete Klasse sollte diese Methode überschreiben, um die tatsächliche Speicher Belegung auszuführen. In der Regel führt die abgeleitete Klasse die folgenden Schritte aus:

1.  Nennen Sie die Basisklassen Implementierung, um zu bestimmen, ob der Arbeitsspeicher wirklich zugeordnet werden muss.
2.  Arbeitsspeicher zuweisen.
3.  Erstellen Sie [**cmediasample**](cmediasample.md) -Objekte, die Arbeitsspeicher Blöcke aus Schritt 2 enthalten.
4.  Fügen Sie jedes **cmediasample** -Objekt der Liste der kostenlosen Beispiele hinzu ([**cbasezucator:: m \_ lfree**](cbaseallocator-m-lfree.md)).

Ein Beispiel finden Sie unter [**cmemzuordcator:: Zuweisung**](cmemallocator-alloc.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasezucator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




