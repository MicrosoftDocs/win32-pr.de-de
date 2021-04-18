---
description: Konstruktormethode.
ms.assetid: 3ee67cfd-a968-4b7c-9c7b-1c28ddb9c343
title: Cmediasample. cmediasample-Konstruktor (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4513af3b01d39f311fd1b8ecc1cea8f086d89c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358322"
---
# <a name="cmediasamplecmediasample-constructor"></a>Cmediasample. cmediasample-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CMediaSample(
   TCHAR          *pName,
   CBaseAllocator *pAllocator,
   HRESULT        *phr,
   LPBYTE         pBuffer = NULL,
   LONG           length = 0
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Ignoriert.

</dd> <dt>

*pallocator* 
</dt> <dd>

Zeiger auf das [**cbasezucator**](cbaseallocator.md) -Objekt, das das Beispiel erstellt hat.

</dd> <dt>

*PHR* 
</dt> <dd>

Ignoriert.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Zeiger auf einen vom Aufrufer zugeordneten Speicherpuffer mit einer Größen *Länge*.

</dd> <dt>

*length* 
</dt> <dd>

Länge des Speicherpuffers.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der **HRESULT** -Wert, der im *PHR* -Parameter übergeben wird, wird von der Basisklasse nicht geändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediasample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




