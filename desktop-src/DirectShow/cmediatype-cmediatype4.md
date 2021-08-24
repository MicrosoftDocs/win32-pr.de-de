---
description: 'CMediaType.CMediaType-Konstruktor (Mtype.h): Konstruktormethode.'
ms.assetid: 35198320-d028-42d4-823f-4f8346d8f977
title: CMediaType.CMediaType-Konstruktor (Mtype.h) – cmtype- und phr-Parameter
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
ms.openlocfilehash: 2f686d1338073c65ce3e5bc3871ae8f4a5b9102e78d7678d5bcf6f77a565397d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792950"
---
# <a name="cmediatypecmediatype-constructor-mtypeh"></a>CMediaType.CMediaType-Konstruktor (Mtype.h)

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

*cmtype* \[ Ref\]
</dt> <dd>

Verweis auf ein `CMediaType` -Objekt. Der -Konstruktor kopiert den Medientyp in das neue -Objekt, einschließlich des Formatblocks( sofern verfügbar).

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf eine Variable, die einen HRESULT-Wert empfängt. Dieser Parameter kann ein **NULL-Zeiger** sein. Andernfalls muss der Aufrufer den Wert auf S \_ OK festlegen, bevor der Konstruktor aufgerufen wird. Wenn der Konstruktor fehlschlägt, legt er den Wert auf einen Fehlercode fest.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Konstruktor ruft die [**CMediaType::InitMediaType-Methode**](cmediatype-initmediatype.md) auf, um den Medientyp zu initialisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 




