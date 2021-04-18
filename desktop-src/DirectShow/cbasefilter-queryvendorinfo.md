---
description: 'Die queryvendorinfo-Methode ruft eine Zeichenfolge ab, die Hersteller Informationen enthält. Diese Methode implementiert die ibasefilter:: queryvendorinfo-Methode.'
ms.assetid: 083c0556-d516-4daf-8621-e158ea78b5a3
title: Cbasefilter. queryvendorinfo-Methode (amfilter. h)
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
ms.openlocfilehash: 1786477c042bb1d9ecc6340056a771141d0a3c74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361061"
---
# <a name="cbasefilterqueryvendorinfo-method"></a>Cbasefilter. queryvendorinfo-Methode

Die- `QueryVendorInfo` Methode ruft eine Zeichenfolge ab, die Hersteller Informationen enthält. Diese Methode implementiert die [**ibasefilter:: queryvendorinfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryVendorInfo(
   LPWSTR *pVendorInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvendorinfo* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf eine breit Zeichen-Zeichenfolge mit den Hersteller Informationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "E \_ notimpl" zurück.

## <a name="remarks"></a>Bemerkungen

Überschreiben Sie diese Methode, um Hersteller Informationen für einen Filter bereitzustellen. Wenn Sie diese Methode implementieren, verwenden Sie die **CoTaskMemAlloc** -Funktion, um Arbeitsspeicher für die Zeichenfolge zuzuweisen. Der Aufrufer ist für das Aufrufen der **CoTaskMemFree** -Funktion verantwortlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




