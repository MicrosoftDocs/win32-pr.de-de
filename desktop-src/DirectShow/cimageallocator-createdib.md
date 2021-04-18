---
description: Die Methode "Methode" erstellt eine GDI-geräteunabhängige Bitmap (DIB). Das DIB wird in einem freigegebenen mempory-Block zugeordnet, der einen Kopiervorgang ausschließt, wenn der besitzende Filter das Image löscht.
ms.assetid: 8a9ab1cf-4104-48e9-ba6c-28d0f1a1d226
title: Cimagezuzuordcator. kreatedib-Methode (winutil. h)
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
ms.openlocfilehash: 316b7aeadfa442a8df4e80075380464758f3c6bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365506"
---
# <a name="cimageallocatorcreatedib-method"></a>Cimagezuzuordcator. kreatedib-Methode

Die `CreateDIB` -Methode erstellt eine GDI-geräteunabhängige Bitmap (DIB). Das DIB wird in einem freigegebenen mempory-Block zugeordnet, der einen Kopiervorgang ausschließt, wenn der besitzende Filter das Image löscht.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateDIB(
        LONG    InSize,
  [ref] DIBDATA &DibData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Insize* 
</dt> <dd>

Größe der Bitmap.

</dd> <dt>

*Dibdata* \[ atur\]
</dt> <dd>

Verweis auf eine [**dibdata**](dibdata.md) -Struktur. Die-Methode füllt diese-Struktur mit Informationen über das DIB aus.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder andernfalls einen Fehlercode zurück.

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

 

 




