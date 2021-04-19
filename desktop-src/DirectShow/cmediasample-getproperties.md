---
description: 'Die GetProperties-Methode ruft die Eigenschaften des Beispiels ab. Diese Methode implementiert die IMediaSample2:: GetProperties-Methode.'
ms.assetid: c2a6d611-9c17-41fb-bb6d-f5b17f1c9966
title: Cmediasample. GetProperties-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06ee1022f298e2f5167d348777b33fc2f1703eef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369395"
---
# <a name="cmediasamplegetproperties-method"></a>Cmediasample. GetProperties-Methode

Die- `GetProperties` Methode ruft die Eigenschaften des Beispiels ab. Diese Methode implementiert die [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetProperties(
   DWORD cbProperties,
   BYTE  *pbProperties
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cbproperties* 
</dt> <dd>

Länge der abzurufenden Eigenschaften Daten in Bytes.

</dd> <dt>

*pbproperties* 
</dt> <dd>

Zeiger auf einen Puffer der Größe *cbproperties*.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                               | Beschreibung                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg.<br/>                   |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | **Null** -Zeigerargument.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediasample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




