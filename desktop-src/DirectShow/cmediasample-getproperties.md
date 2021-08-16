---
description: Die GetProperties-Methode ruft die Eigenschaften des Beispiels ab. Diese Methode implementiert die IMediaSample2::GetProperties-Methode.
ms.assetid: c2a6d611-9c17-41fb-bb6d-f5b17f1c9966
title: CMediaSample.GetProperties-Methode (Amfilter.h)
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
ms.openlocfilehash: 856da0c73f3dd93d0c660f55aa0a9de35d87ab1b270df2179d7ad0b520e6d0a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074024"
---
# <a name="cmediasamplegetproperties-method"></a>CMediaSample.GetProperties-Methode

Die `GetProperties` -Methode ruft die Eigenschaften des Beispiels ab. Diese Methode implementiert die [**IMediaSample2::GetProperties-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetProperties(
   DWORD cbProperties,
   BYTE  *pbProperties
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cbProperties* 
</dt> <dd>

Länge der abzurufenden Eigenschaftsdaten in Bytes.

</dd> <dt>

*pbProperties* 
</dt> <dd>

Zeiger auf einen Puffer der Größe *cbProperties*.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                               | Beschreibung                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg.<br/>                   |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl> |  NULL-Zeigerargument.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaSample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




