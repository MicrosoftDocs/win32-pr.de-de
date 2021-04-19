---
description: Erfahren Sie mehr über die cmediatype. cmediatype-Konstruktormethode (mtype. h). Diese Methode verwendet den Parameter "majortype".
ms.assetid: 89356578-0509-46c1-abd4-421688017f1d
title: Cmediatype. cmediatype-Konstruktor (mtype. h)-majortype-Parameter
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
ms.openlocfilehash: a99717e41424a99b3c1e79674426fb14c5b57b9d
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "106353409"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---majortype-parameter"></a>Cmediatype. cmediatype-Konstruktor (mtype. h)-majortype-Parameter

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

Zeiger auf eine **GUID** des Haupt Typs. Der Konstruktor initialisiert die GUID des Haupt Typs mit diesem Wert.

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

 

 




