---
description: Die DynamicReconnect-Methode führt eine dynamische erneute Verbindung mit einem neuen Medientyp aus. Die erneute Verbindung kann während der Ausführung des Filterdiagramms auftreten.
ms.assetid: 1fe9f1cc-1f5d-407e-8c80-fea6cd1cb16f
title: CDynamicOutputPin.DynamicReconnect-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DynamicReconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6abd453b328a22765a9649e69bbe0f5e3e4d4bc8e45148a0777fa23901447ab3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688840"
---
# <a name="cdynamicoutputpindynamicreconnect-method"></a>CDynamicOutputPin.DynamicReconnect-Methode

Die `DynamicReconnect` -Methode führt eine dynamische erneute Verbindung mit einem neuen Medientyp aus. Die erneute Verbindung kann während der Ausführung des Filterdiagramms auftreten.

## <a name="syntax"></a>Syntax


```C++
HRESULT DynamicReconnect(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pmt* 
</dt> <dd>

Zeiger auf eine [**AM \_ MEDIA \_ TYPE-Struktur,**](/windows/win32/api/strmif/ns-strmif-am_media_type) die den Medientyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                            | Beschreibung                                                                                                                                         |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                                                                                                                                 |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Fehler. Möglicherweise hat der besitzende Filter die [**CDynamicOutputPin::SetConfigInfo-Methode**](cdynamicoutputpin-setconfiginfo.md) nicht aufgerufen.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode muss vom gleichen Thread aufgerufen werden, der Daten an den Pin übermittelt. Sobald diese Methode aufgerufen wurde, können Stichproben mit dem alten Medientyp nicht übermittelt werden. Der Aufrufer muss sicherstellen, dass keine alten Stichproben ausstehen.

Rufen Sie [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) auf, bevor Sie diese Methode aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




