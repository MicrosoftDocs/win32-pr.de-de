---
description: Mit der ReallocFormatBuffer-Methode wird der Formatblock einer neuen Größe neu zugewiesen.
ms.assetid: 49bec677-09cc-4e1a-994a-13e873e61713
title: CMediaType.ReallocFormatBuffer-Methode (Mtype.h)
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
ms.openlocfilehash: 7bd4d7bd27c3698f1e30c690f755f445ffaffeff37c88f27d0a5c8ba58cd2d32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768170"
---
# <a name="cmediatypereallocformatbuffer-method"></a>CMediaType.ReallocFormatBuffer-Methode

Mit `ReallocFormatBuffer` der -Methode wird der Formatblock einer neuen Größe neu zugewiesen.

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

Für den Formatblock erforderliche neue Größe in Bytes. Muss größer sein als Null.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Zeiger auf den neuen Block zurück. Andernfalls wird entweder ein Zeiger auf den alten Formatblock oder **NULL zurückgegeben.**

## <a name="remarks"></a>Hinweise

Diese Methode weist einen neuen Formatblock zu. Sie kopiert so viel wie möglich aus dem vorhandenen Formatblock in den neuen Formatblock. Wenn der neue Block kleiner als der vorhandene Block ist, wird der vorhandene Formatblock abgeschnitten. Wenn der neue Block größer ist, ist der Inhalt des zusätzlichen Speicherplatzes nicht definiert. Sie sind nicht explizit auf 0 (null) festgelegt.

Die -Methode aktualisiert **die CbFormat-** und **pbFormat-Member** der **AM MEDIA \_ \_ TYPE-Struktur.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 




