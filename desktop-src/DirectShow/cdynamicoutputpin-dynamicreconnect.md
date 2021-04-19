---
description: Die dynamikreconnect-Methode führt eine dynamische erneute Verbindung mit einem neuen Medientyp aus. Die erneute Verbindung kann auftreten, während das Filter Diagramm ausgeführt wird.
ms.assetid: 1fe9f1cc-1f5d-407e-8c80-fea6cd1cb16f
title: Cdynamicoutputpin. dynamikreconnect-Methode (amfilter. h)
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
ms.openlocfilehash: dd595748380a35f74e591283ed3d03273c683e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355258"
---
# <a name="cdynamicoutputpindynamicreconnect-method"></a>Cdynamicoutputpin. dynamikreconnect-Methode

Die- `DynamicReconnect` Methode führt eine dynamische erneute Verbindung mit einem neuen Medientyp aus. Die erneute Verbindung kann auftreten, während das Filter Diagramm ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT DynamicReconnect(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PMT* 
</dt> <dd>

Zeiger auf eine [**am \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die den Medientyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                            | Beschreibung                                                                                                                                         |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                                                                                                                                 |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Fehler. Möglicherweise hat der besitzende Filter die [**cdynamicoutputpin:: setconfiginfo**](cdynamicoutputpin-setconfiginfo.md) -Methode nicht aufgerufen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode muss vom gleichen Thread aufgerufen werden, der Daten an die PIN übergibt. Nachdem diese Methode aufgerufen wurde, können keine Beispiele mit dem alten Medientyp übermittelt werden. Der Aufrufer muss sicherstellen, dass keine alten Beispiele ausstehend sind.

Rufen Sie [**cdynamicoutputpin:: startusingoutputpin**](cdynamicoutputpin-startusingoutputpin.md) auf, bevor Sie diese Methode aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdynamicoutputpin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




