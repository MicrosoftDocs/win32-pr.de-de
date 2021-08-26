---
description: Die BlockOutputPin-Methode blockiert den Pin.
ms.assetid: 49f6b8da-a8b2-482d-b70d-2c68a1b45a10
title: CDynamicOutputPin.BlockOutputPin-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.BlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9dc1f4cdafd732821398ee04e127c0525798dd6cc02f67f8af5d977b195a6a74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983360"
---
# <a name="cdynamicoutputpinblockoutputpin-method"></a>CDynamicOutputPin.BlockOutputPin-Methode

Die `BlockOutputPin` -Methode blockiert den Pin. Während der Pin blockiert ist, wartet die [**CDynamicOutputPin::StartUsingOutputPin-Methode**](cdynamicoutputpin-startusingoutputpin.md) darauf, dass die Blockierung des Pins aufgehoben wird. Der Status "Blockiert" verhindert, dass der Ausgabepin Stichproben liefert, sein Ausgabeformat ändert oder sich selbst erneut verbindet.

## <a name="syntax"></a>Syntax


```C++
void BlockOutputPin();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Halten Sie vor dem Aufrufen dieser Methode den [**kritischen Abschnitt CDynamicOutputPin::m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) bei. Rufen Sie diese Methode nicht auf, wenn ein Streamingthread den Pin verwendet, um Daten zu liefern oder die Verbindung zu ändern. Um zu überprüfen, ob ein Streamingthread den Pin verwendet, rufen Sie die [**CDynamicOutputPin::StreamingThreadUsingOutputPin-Methode**](cdynamicoutputpin-streamingthreadusingoutputpin.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




