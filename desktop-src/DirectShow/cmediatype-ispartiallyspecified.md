---
description: Die ispartiallydefined-Methode bestimmt, ob der Medientyp teilweise definiert ist. Ein Medientyp ist partiell, wenn der Haupttyp, der Untertyp oder der Formattyp GUID \_ NULL ist.
ms.assetid: 26dd7a2b-b2f8-485f-a9af-31c3a9eb1def
title: Cmediatype. ispartiallyangegebene-Methode (mtype. h)
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
ms.openlocfilehash: 32c39942ab3f97d45ecf71ba841d56b7afd4be62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360942"
---
# <a name="cmediatypeispartiallyspecified-method"></a>Cmediatype. ispartiallyangegebene-Methode

Die- `IsPartiallySpecified` Methode bestimmt, ob der Medientyp teilweise definiert ist. Ein Medientyp ist *partiell* , wenn der Haupttyp, der Untertyp oder der Formattyp GUID \_ NULL ist.

## <a name="syntax"></a>Syntax


```C++
BOOL IsPartiallySpecified() const;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn der Medientyp teilweise angegeben ist. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) -Methode kann partielle Medientypen akzeptieren.

Die-Implementierung testet den Untertyp nicht tatsächlich. Wenn ein bestimmter Formattyp vorhanden ist, wird der Medientyp nicht als partiell betrachtet, auch wenn der Untertyp GUID \_ NULL ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediatype-Klasse**](cmediatype.md)
</dt> </dl>

 

 




