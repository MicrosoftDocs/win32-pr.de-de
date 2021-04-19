---
description: Die Methode "belegcformatbuffer" weist Speicher für den Format Block zu.
ms.assetid: 5ff716c7-f9cf-4b1c-9d3a-62ab955c1392
title: Cmediatype. zucformatbuffer-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.AllocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6a9314fd06734adcc367b7be34dc8d6d1b9d996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364028"
---
# <a name="cmediatypeallocformatbuffer-method"></a>Cmediatype. zucformatbuffer-Methode

Die- `AllocFormatBuffer` Methode ordnet Speicher für den Format Block zu.

## <a name="syntax"></a>Syntax


```C++
BYTE* AllocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*length* 
</dt> <dd>

Die für den Format Block erforderliche Größe (in Bytes).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung einen Zeiger auf den neuen Block zurück. Andernfalls wird **null** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn die Methode erfolgreich einen neuen Format Block zugeordnet hat, gibt Sie den vorhandenen Format Block frei. Wenn die Zuordnung fehlschlägt, verlässt die Methode den vorhandenen Format Block.

Die-Methode aktualisiert die Member **cbformat** und **pbformat** der **am \_ \_ Medientyp** -Struktur.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediatype-Klasse**](cmediatype.md)
</dt> </dl>

 

 




