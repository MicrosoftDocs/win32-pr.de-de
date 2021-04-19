---
description: 'Die EndOf-Methode benachrichtigt die PIN, dass keine weiteren Daten erwartet werden. Diese Methode implementiert die IPin:: EndOf Stream-Methode.'
ms.assetid: db9896eb-3db2-4d58-a787-4d80ce8f0d0e
title: Ctransforminputpin. EndOf Stream-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc39770f081499be720c433301823cbc60f37d17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354206"
---
# <a name="ctransforminputpinendofstream-method"></a>Ctransforminputpin. EndOf Stream-Methode

Die- `EndOfStream` Methode benachrichtigt die PIN, dass keine weiteren Daten erwartet werden. Diese Methode implementiert die [**IPin:: EndOf Stream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                           | Beschreibung                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                         |
| <dl> <dt>**S \_ false**</dt> </dl>               | Die PIN wird zurzeit geleert.<br/>       |
| <dl> <dt>**VFW \_ E \_ nicht \_ verbunden**</dt> </dl> | Die Ausgabe-PIN ist nicht verbunden.<br/> |
| <dl> <dt>**VFW \_ E \_ Lauf \_ Zeitfehler**</dt> </dl> | Laufzeitfehler.<br/>       |
| <dl> <dt>**VFW \_ E \_ falscher \_ Zustand**</dt> </dl>   | Die PIN wurde beendet.<br/>              |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**ctransformfilter:: EndOfStream**](ctransformfilter-endofstream.md) -Methode des Filters auf, um die Streamende Benachrichtigung zu übermitteln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




