---
description: Die IsPartiallySpecified-Methode bestimmt, ob der Medientyp teilweise definiert ist. Ein Medientyp ist partiell, wenn der Haupttyp, Untertyp oder Formattyp GUID \_ NULL ist.
ms.assetid: 26dd7a2b-b2f8-485f-a9af-31c3a9eb1def
title: CMediaType.IsPartiallySpecified-Methode (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsPartiallySpecified
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c2e7bdbbc43195222b4054f71ec05ebe3c8a7e15ac8c634d57fba61e45bf319
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084470"
---
# <a name="cmediatypeispartiallyspecified-method"></a>CMediaType.IsPartiallySpecified-Methode

Die `IsPartiallySpecified` -Methode bestimmt, ob der Medientyp teilweise definiert ist. Ein Medientyp ist *partiell,* wenn der Haupttyp, Untertyp oder Formattyp GUID \_ NULL ist.

## <a name="syntax"></a>Syntax


```C++
BOOL IsPartiallySpecified() const;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn der Medientyp teilweise angegeben ist. Andernfalls gibt **FALSE** zurück.

## <a name="remarks"></a>Hinweise

Die [**IPin::Verbinden-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) kann partielle Medientypen akzeptieren.

Der Untertyp wird von der Implementierung nicht tatsächlich getestet. Wenn ein angegebener Formattyp vorhanden ist, wird der Medientyp auch dann nicht als partiell betrachtet, wenn der Untertyp GUID \_ NULL ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 




