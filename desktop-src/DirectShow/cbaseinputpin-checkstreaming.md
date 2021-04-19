---
description: Bestimmt, ob die PIN Beispiele annehmen kann.
ms.assetid: bc66ab4c-99de-4031-bdac-b1430f736e20
title: Cbaseinputpin. checkstreaming-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba07d28ac93f7dc511390a851d3c737a833ef3f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355260"
---
# <a name="cbaseinputpincheckstreaming-method"></a>Cbaseinputpin. checkstreaming-Methode

Bestimmt, ob die PIN Beispiele annehmen kann.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CheckStreaming();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                           | Beschreibung                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                   |
| <dl> <dt>**S \_ false**</dt> </dl>               | Die PIN wird zurzeit geleert.<br/> |
| <dl> <dt>**VFW \_ E \_ Lauf \_ Zeitfehler**</dt> </dl> | Laufzeitfehler.<br/> |
| <dl> <dt>**VFW \_ E \_ falscher \_ Zustand**</dt> </dl>   | Die PIN wurde beendet.<br/>        |



 

## <a name="remarks"></a>Bemerkungen

Die abgeleitete Klasse kann diese Methode überschreiben, um weitere Überprüfungen auszuführen. In der über schreibenden Methode wird auch die Basisklassen Implementierung aufgerufen.

Die [**cbasinput PIN:: Receive**](cbaseinputpin-receive.md) -Methode ruft diese Methode auf. Sie sollten auch die [**cbasepin:: EndOfStream**](cbasepin-endofstream.md) -Methode überschreiben, um diese Methode aufzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseingeputpin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




