---
description: Dieser Operator überlädt den Zuweisungsoperator, um einen Medientyp zu kopieren.
ms.assetid: 5b94191d-b5e4-42b2-b0c5-8c2da2483c54
title: CMediaType.CMediaType::operator=-Methode (Mtype.h) – mtype-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b5960ac5f9dc3e685aa0b8b281989185580fd5b683392aaf93a0891d0ebaa35d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016263"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh"></a>CMediaType.CMediaType::operator=-Methode (Mtype.h)

Dieser Operator überlädt den Zuweisungsoperator, um einen Medientyp zu kopieren.

## <a name="syntax"></a>Syntax


```C++
CMediaType& CMediaType::operator=(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mtype* \[ Ref\]
</dt> <dd>

Verweis auf eine [**AM \_ MEDIA \_ TYPE-Struktur.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Verweis auf das -Objekt zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 




