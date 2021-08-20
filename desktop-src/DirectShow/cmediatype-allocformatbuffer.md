---
description: Die AllocFormatBuffer-Methode weist Arbeitsspeicher für den Formatblock zu.
ms.assetid: 5ff716c7-f9cf-4b1c-9d3a-62ab955c1392
title: CMediaType.AllocFormatBuffer-Methode (Mtype.h)
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
ms.openlocfilehash: 2c53e739237f2d61a6c59c7fac96e1b97e6343fa6dd209bcf72700cefab7d599
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073984"
---
# <a name="cmediatypeallocformatbuffer-method"></a>CMediaType.AllocFormatBuffer-Methode

Die `AllocFormatBuffer` -Methode weist Arbeitsspeicher für den Formatblock zu.

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

Erforderliche Größe für den Formatblock in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Zeiger auf den neuen Block zurück. Andernfalls gibt NULL **zurück.**

## <a name="remarks"></a>Hinweise

Wenn die Methode erfolgreich einen neuen Formatblock zuteilen kann, wird der vorhandene Formatblock frei. Wenn die Zuordnung fehlschlägt, verlässt die Methode den vorhandenen Formatblock.

Die -Methode aktualisiert **die CbFormat-** und **pbFormat-Member** der **AM MEDIA \_ \_ TYPE-Struktur.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 




