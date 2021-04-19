---
description: Erfahren Sie mehr über die cmediatype. cmediatype-Konstruktormethode (mtype. h). Diese Methode verwendet die Parameter "mtype" und "PHR".
ms.assetid: b7d5264a-2a5f-4111-96bb-1ea2b13405be
title: 'Cmediatype. cmediatype-Konstruktor (mtype. h): mtype-Parameter und PHR-Parameter'
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
ms.openlocfilehash: 12ef9012e59dfce1f45d21aa720ae13bd660f2d8
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "106373553"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---mtype-and-phr-parameters"></a>Cmediatype. cmediatype-Konstruktor (mtype. h): mtype-Parameter und PHR-Parameter

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CMediaType(
  [ref] const AM_MEDIA_TYPE &mtype,
              HRESULT       *phr = NULL
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mtype* \[ atur\]
</dt> <dd>

Verweis auf eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur. Der-Konstruktor kopiert den Medientyp in das neue-Objekt, einschließlich des-Format Blocks, sofern vorhanden.

</dd> <dt>

*PHR* 
</dt> <dd>

Ein Zeiger auf eine Variable, die einen HRESULT-Wert empfängt. Dieser Parameter kann ein **null** -Zeiger sein. Andernfalls muss der Aufrufer den Wert vor dem \_ Aufrufen des Konstruktors auf S OK festlegen. Wenn der Konstruktor fehlschlägt, wird der Wert auf einen Fehlercode festgelegt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Konstruktor ruft die [**cmediatype:: initmediatype**](cmediatype-initmediatype.md) -Methode auf, um den Medientyp zu initialisieren.

## <a name="requirements"></a>Anforderungen

| Anforderung                   | Wert                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header  | Mtype. h (Include Streams. h)                                                                                     |
| Bibliothek | "Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediatype-Klasse**](cmediatype.md)
</dt> </dl>

 

 




