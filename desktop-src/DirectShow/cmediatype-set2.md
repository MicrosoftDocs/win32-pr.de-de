---
description: Die Set-Methode legt den Medientyp von einem anderen Medientyp fest.
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: Cmediatype. Set-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afe99c3f5ee10e6aacd3dadf69af320b110688af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358267"
---
# <a name="cmediatypeset-method-mtypeh"></a>Cmediatype. Set-Methode (mtype. h)

Die- `Set` Methode legt den Medientyp von einem anderen Medientyp fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT Set(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mtype* \[ atur\]
</dt> <dd>

Verweis auf eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " \_ OK" oder "E \_ outo" zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode kopiert den gesamten Medientyp aus *mtype*.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediatype-Klasse**](cmediatype.md)
</dt> </dl>

 

 




