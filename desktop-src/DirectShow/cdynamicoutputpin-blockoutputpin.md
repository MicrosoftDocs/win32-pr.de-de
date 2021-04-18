---
description: Die blockoutputpin-Methode blockiert die PIN.
ms.assetid: 49f6b8da-a8b2-482d-b70d-2c68a1b45a10
title: Cdynamicoutputpin. blockoutputpin-Methode (amfilter. h)
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
ms.openlocfilehash: 3998774550363b7d22e05ca491f1d76ba7f2ff2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371357"
---
# <a name="cdynamicoutputpinblockoutputpin-method"></a>Cdynamicoutputpin. blockoutputpin-Methode

Die- `BlockOutputPin` Methode blockiert die PIN. Während die PIN blockiert ist, wartet die [**cdynamicoutputpin:: startusingoutputpin**](cdynamicoutputpin-startusingoutputpin.md) -Methode auf die Blockierung der PIN. Der blockierte Zustand verhindert, dass die Ausgabe-PIN Beispiele bereitstellt, das Ausgabeformat ändert oder eine erneute Verbindung herstellt.

## <a name="syntax"></a>Syntax


```C++
void BlockOutputPin();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Halten Sie vor dem Aufrufen dieser Methode den kritischen Abschnitt [**cdynamicoutputpin:: m \_ blockstatus eLOCK**](cdynamicoutputpin-m-blockstatelock.md) . Diese Methode kann nicht aufgerufen werden, wenn ein streamingingthread die PIN verwendet, um Daten bereitzustellen oder um die Verbindung zu ändern. Um zu überprüfen, ob ein streamingthread die PIN verwendet, können Sie die [**cdynamicoutputpin:: streamingthreadusingoutputpin**](cdynamicoutputpin-streamingthreadusingoutputpin.md) -Methode aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdynamicoutputpin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




