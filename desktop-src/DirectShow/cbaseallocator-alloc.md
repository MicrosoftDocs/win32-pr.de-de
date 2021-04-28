---
description: 'CBaseAllocator.Alloc-Methode: Die Alloc-Methode weist den Puffern Arbeitsspeicher zu.'
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
ms.openlocfilehash: b53dc461a520b4e8c890a36fca6d73c2c836499f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096367"
---
# <a name="cbaseallocatoralloc-method"></a>CBaseAllocator.Alloc-Methode

Die `Alloc` -Methode weist Den Puffern Arbeitsspeicher zu.

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



 

## <a name="remarks"></a>Bemerkungen

Diese Methode wird von der [**CBaseAllocator::Commit-Methode**](cbaseallocator-commit.md) aufgerufen.

In der Basisklasse weist diese Methode keinen Arbeitsspeicher zu. Es wird ein Fehler zurückgegeben, wenn die Pufferanforderungen nicht festgelegt wurden, S FALSE, wenn sich die Anforderungen nicht geändert haben, und S OK, wenn sich \_ \_ die Anforderungen geändert haben.

Eine abgeleitete Klasse sollte diese Methode überschreiben, um die tatsächliche Speicherzuweisung durchzuführen. In der Regel führt die abgeleitete Klasse die folgenden Schritte aus:

1.  Rufen Sie die Basisklassenimplementierung auf, um zu bestimmen, ob für den Arbeitsspeicher tatsächlich eine Zuweisung benötigt wird.
2.  Zuordnen von Arbeitsspeicher.
3.  Erstellen [**Sie CMediaSample-Objekte,**](cmediasample.md) die Speicherelemente aus Schritt 2 enthalten.
4.  Fügen Sie **jedes CMediaSample-Objekt** zur Liste der kostenlosen Beispiele hinzu ([**CBaseAllocator::m \_ lFree**](cbaseallocator-m-lfree.md)).

Ein Beispiel finden Sie unter [**CMemAllocator::Alloc**](cmemallocator-alloc.md).

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseAllocator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




