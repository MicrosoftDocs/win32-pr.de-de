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
ms.openlocfilehash: dd91252920c74d45e4218be3c3d03249a116bfcf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095418"
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

## <a name="remarks"></a>Bemerkungen

Der Konstruktor ruft die [**CMediaType::InitMediaType-Methode**](cmediatype-initmediatype.md) auf, um den Medientyp zu initialisieren.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 




