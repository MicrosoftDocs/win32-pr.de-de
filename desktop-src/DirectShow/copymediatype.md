---
description: Die copymediatype-Funktion kopiert eine am- \_ \_ Medientyp Struktur in eine andere Struktur, einschließlich des Format Blocks.
ms.assetid: 5b47e197-abb5-4b2c-ad65-a506c5e239be
title: Copymediatype-Funktion (mtype. h)
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
ms.openlocfilehash: 2e37f277244ae9b82c395d7901917e1fc1e78b35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361585"
---
# <a name="copymediatype-function"></a>Copymediatype-Funktion

Die **copymediatype** -Funktion kopiert eine [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur in eine andere Struktur, einschließlich des Format Blocks.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI CopyMediaType(
         AM_MEDIA_TYPE *pmtTarget,
   const AM_MEDIA_TYPE *pmtSource
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmttarget* 
</dt> <dd>

Zeiger auf eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur. Die-Methode kopiert den Medientyp in diese-Struktur.

</dd> <dt>

*pmtsource* 
</dt> <dd>

Zeiger auf eine zu Kopier Elle [**\_ \_ Quelltyp-Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " \_ OK" oder "E \_ outo" zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ordnet den Speicher für den Format Block zu. Wenn der *pmttarget* -Parameter bereits einen zugeordneten Format Block enthält, tritt ein Speicherplatz auf. Um einen Speicherplatz zu vermeiden, rufen Sie " [**fremediatype**](freemediatype.md) " auf, bevor Sie diese Funktion aufrufen.

Nachdem die Methode zurückgegeben wurde, können Sie [**freemediatype**](freemediatype.md) auf *pmttarget* aufzurufen, um den Format Block freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medientyp Funktionen**](media-type-functions.md)
</dt> </dl>

 

 




