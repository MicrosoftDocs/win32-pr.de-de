---
description: Schreibt die Filterdaten in den angegebenen Stream.
ms.assetid: 1b405050-6cfd-4b69-b449-f00a6ecfac6a
title: Cpersiststream. Write Items-Methode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.WriteToStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 893d58986db92e50cbafefe74676481162808abf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361293"
---
# <a name="cpersiststreamwritetostream-method"></a>Cpersiststream. Write-Methode

Schreibt die Filterdaten in den angegebenen Stream.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT WriteToStream(
   IStream *pStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStream* 
</dt> <dd>

Zeiger auf eine **IStream** -Schnittstelle, die den Zielstream der Filterdaten angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück. Die abgeleitete Klasse sollte einen gültigen **HRESULT** -Wert zurückgeben.

## <a name="remarks"></a>Bemerkungen

Die Standardversion schreibt nichts. Sie kann überschrieben werden, um Daten zu schreiben, die für Ihre Klasse spezifisch sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PStream. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpersiststream-Klasse**](cpersiststream.md)
</dt> </dl>

 

 




