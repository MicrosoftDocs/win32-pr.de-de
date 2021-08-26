---
description: Die CreateDIB-Methode erstellt eine geräteunabhängige GDI-Bitmap (DIB). Der DIB wird in einem freigegebenen Memporyblock zugeordnet, wodurch ein Kopiervorgang entfernt wird, wenn der besitzende Filter das Bild blitt.
ms.assetid: 8a9ab1cf-4104-48e9-ba6c-28d0f1a1d226
title: CImageAllocator.CreateDIB-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateDIB
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94a629831ea50219b47500c0637cfeaebfbc95b1ee99a8b9d3872a655ab5485c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055480"
---
# <a name="cimageallocatorcreatedib-method"></a>CImageAllocator.CreateDIB-Methode

Die `CreateDIB` -Methode erstellt eine geräteunabhängige GDI-Bitmap (DIB). Der DIB wird in einem freigegebenen Memporyblock zugeordnet, wodurch ein Kopiervorgang entfernt wird, wenn der besitzende Filter das Bild blitt.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateDIB(
        LONG    InSize,
  [ref] DIBDATA &DibData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*InSize* 
</dt> <dd>

Größe der Bitmap.

</dd> <dt>

*DibData* \[ Ref\]
</dt> <dd>

Verweis auf eine [**DIBDATA-Struktur.**](dibdata.md) Die -Methode füllt diese Struktur mit Informationen zum DIB auf.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich, andernfalls ein Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CImageAllocator-Klasse**](cimageallocator.md)
</dt> <dt>

[**CImageAllocator::Alloc**](cimageallocator-alloc.md)
</dt> </dl>

 

 




