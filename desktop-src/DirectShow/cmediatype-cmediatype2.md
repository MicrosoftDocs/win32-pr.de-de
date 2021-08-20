---
description: Erfahren Sie mehr über die CMediaType.CMediaType-Konstruktormethode (Mtype.h). Diese Methode verwendet den Parameter "majortype".
ms.assetid: 89356578-0509-46c1-abd4-421688017f1d
title: CMediaType.CMediaType-Konstruktor (Mtype.h) – Majortype-Parameter
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
ms.openlocfilehash: b1ebf3cec41c4180a4dcad4a5a7c273996f70bfdb6d052127ff71dd1b929238c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073994"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---majortype-parameter"></a>CMediaType.CMediaType-Konstruktor (Mtype.h) – Majortype-Parameter

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CMediaType(
   const GUID *majortype
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*majortype* 
</dt> <dd>

Zeiger auf eine **Haupttyp-GUID.** Der Konstruktor initialisiert die Haupttyp-GUID mit diesem Wert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Konstruktor ruft die [**CMediaType::InitMediaType-Methode**](cmediatype-initmediatype.md) auf, um den Medientyp zu initialisieren.

## <a name="requirements"></a>Anforderungen

| Anforderung                   | Wert                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header  | Mtype.h (include Streams.h)                                                                                     |
| Bibliothek | Strmbase.lib (Verkaufsbuilds); Strmbasd.lib (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 




