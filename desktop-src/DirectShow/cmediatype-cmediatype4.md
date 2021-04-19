---
description: Konstruktormethode.
ms.assetid: 35198320-d028-42d4-823f-4f8346d8f977
title: 'Cmediatype. cmediatype-Konstruktor (mtype. h): cmtype-Parameter und PHR-Parameter'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a40929bb6f53df7ce721e20eefba3019eb71cb0e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389064"
---
# <a name="cmediatypecmediatype-constructor-mtypeh"></a>Cmediatype. cmediatype-Konstruktor (mtype. h)

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CMediaType(
  [ref] const CMediaType &cmtype,
              HRESULT    *phr = NULL
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cmtype* \[ atur\]
</dt> <dd>

Verweis auf ein- `CMediaType` Objekt. Der-Konstruktor kopiert den Medientyp in das neue-Objekt, einschließlich des-Format Blocks, sofern vorhanden.

</dd> <dt>

*PHR* 
</dt> <dd>

Ein Zeiger auf eine Variable, die einen HRESULT-Wert empfängt. Dieser Parameter kann ein **null** -Zeiger sein. Andernfalls muss der Aufrufer den Wert vor dem \_ Aufrufen des Konstruktors auf S OK festlegen. Wenn der Konstruktor fehlschlägt, wird der Wert auf einen Fehlercode festgelegt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Konstruktor ruft die [**cmediatype:: initmediatype**](cmediatype-initmediatype.md) -Methode auf, um den Medientyp zu initialisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediatype-Klasse**](cmediatype.md)
</dt> </dl>

 

 




