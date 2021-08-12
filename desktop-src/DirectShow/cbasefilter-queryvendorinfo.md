---
description: Die QueryVendorInfo-Methode ruft eine Zeichenfolge mit Herstellerinformationen ab. Diese Methode implementiert die IBaseFilter::QueryVendorInfo-Methode.
ms.assetid: 083c0556-d516-4daf-8621-e158ea78b5a3
title: CBaseFilter.QueryVendorInfo-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryVendorInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff1cd8b966456df631a573ab2e8691b3be5d8bda47b21b042986204144e639b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659803"
---
# <a name="cbasefilterqueryvendorinfo-method"></a>CBaseFilter.QueryVendorInfo-Methode

Die `QueryVendorInfo` -Methode ruft eine Zeichenfolge mit Herstellerinformationen ab. Diese Methode implementiert die [**IBaseFilter::QueryVendorInfo-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo)

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryVendorInfo(
   LPWSTR *pVendorInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVendorInfo* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf eine Zeichenfolge mit Breitzeichen empfängt, die die Herstellerinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt E \_ NOTIMPL zurück.

## <a name="remarks"></a>Hinweise

Um Anbieterinformationen für einen Filter bereitzustellen, überschreiben Sie diese Methode. Wenn Sie diese Methode implementieren, verwenden Sie die **CoTaskMemAlloc-Funktion,** um Speicher für die Zeichenfolge zuzuordnen. Der Aufrufer ist für den Aufruf der **CoTaskMemFree-Funktion** verantwortlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




