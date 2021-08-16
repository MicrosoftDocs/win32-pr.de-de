---
description: Die CopyMediaType-Funktion kopiert eine AM \_ MEDIA \_ TYPE-Struktur in eine andere Struktur, einschließlich des Formatblocks.
ms.assetid: 5b47e197-abb5-4b2c-ad65-a506c5e239be
title: CopyMediaType-Funktion (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CopyMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b193f64edb55a342546f26db1975080490f0e69b2caa91695b3bc63240750983
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634373"
---
# <a name="copymediatype-function"></a>CopyMediaType-Funktion

Die **CopyMediaType-Funktion** kopiert eine [**AM MEDIA \_ \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type) in eine andere Struktur, einschließlich des Formatblocks.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI CopyMediaType(
         AM_MEDIA_TYPE *pmtTarget,
   const AM_MEDIA_TYPE *pmtSource
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmtTarget* 
</dt> <dd>

Zeiger auf eine [**AM \_ MEDIA \_ TYPE-Struktur.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Die -Methode kopiert den Medientyp in diese Struktur.

</dd> <dt>

*pmtSource* 
</dt> <dd>

Zeiger auf eine zu kopierende [**AM \_ MEDIA TYPE-Quellstruktur. \_**](/windows/win32/api/strmif/ns-strmif-am_media_type)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder E \_ OUTOFMEMORY zurück.

## <a name="remarks"></a>Hinweise

Diese Funktion belegt den Arbeitsspeicher für den Formatblock. Wenn der *pmtTarget-Parameter* bereits einen zugeordneten Formatblock enthält, tritt ein Speicherverlust auf. Um einen Speicherverlust zu vermeiden, rufen [**Sie FreeMediaType**](freemediatype.md) auf, bevor Sie diese Funktion aufrufen.

Nachdem die Methode zurückgegeben wurde, rufen [**Sie FreeMediaType**](freemediatype.md) auf *pmtTarget* auf, um den Formatblock frei zu machen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Medientypfunktionen**](media-type-functions.md)
</dt> </dl>

 

 




