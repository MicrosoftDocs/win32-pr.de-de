---
description: Die Methode "kreateimagesample" erstellt ein Medien Beispiel.
ms.assetid: dae71692-5cbc-4bc7-a363-41766ef17c58
title: Cimagezuzuordcator. kreateimagesample-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57463a7025ea816b6fe6bcaa8b964231458903de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361991"
---
# <a name="cimageallocatorcreateimagesample-method"></a>Cimagezuzuordcator. kreateimagesample-Methode

Die- `CreateImageSample` Methode erstellt ein Medien Beispiel.

## <a name="syntax"></a>Syntax


```C++
virtual CImageSample* CreateImageSample(
   LPBYTE pData,
   LONG   Length
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* 
</dt> <dd>

Zeiger auf einen Puffer der Größen *Länge*, der vom Aufrufer zugeordnet wird.

</dd> <dt>

*Länge* 
</dt> <dd>

Die Länge des Puffers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein [**cimagesample**](cimagesample.md) -Objekt zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode erstellt ein neues Medien Beispiel, das als **cimagesample** -Objekt implementiert wird. Die [**imediasample:: getpointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) -Methode des Beispiels gibt einen Zeiger auf den Puffer zurück, der im *pData* -Parameter angegeben ist.

Wenn Sie eine neue zuordnerklasse von [**cimagezuordcator**](cimageallocator.md) und eine neue Media-Beispiel Klasse von [**cimagesample**](cimagesample.md)ableiten, sollten Sie diese Methode überschreiben, um eine Instanz der Media Sample-Klasse zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagezuordcator-Klasse**](cimageallocator.md)
</dt> <dt>

[**Cimagezuordcator:: zuzuweisung**](cimageallocator-alloc.md)
</dt> </dl>

 

 




