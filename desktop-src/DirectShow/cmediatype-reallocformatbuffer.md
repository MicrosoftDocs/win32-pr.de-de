---
description: Die rezugecformatbuffer-Methode ordnet den Format Block neu einer neuen Größe zu.
ms.assetid: 49bec677-09cc-4e1a-994a-13e873e61713
title: Cmediatype. rezuzucformatbuffer-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.ReallocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22e861c61f01a7594d720833e2b3a4b923a1e183
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359261"
---
# <a name="cmediatypereallocformatbuffer-method"></a>Cmediatype. rezuzucformatbuffer-Methode

Die- `ReallocFormatBuffer` Methode ordnet den Format Block neu einer neuen Größe zu.

## <a name="syntax"></a>Syntax


```C++
BYTE* ReallocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*length* 
</dt> <dd>

Die für den Format Block erforderliche neue Größe in Byte. Muss größer sein als Null.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung einen Zeiger auf den neuen Block zurück. Andernfalls wird entweder ein Zeiger auf den alten Format Block oder **null** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode weist einen neuen Format Block zu. Er kopiert so viel des vorhandenen Format Blocks wie möglich in den neuen Format Block. Wenn der neue-Block kleiner als der vorhandene-Block ist, wird der vorhandene Format Block abgeschnitten. Wenn der neue Block größer ist, ist der Inhalt des zusätzlichen Speicherplatzes nicht definiert. Sie sind nicht explizit auf 0 (null) festgelegt.

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

 

 




