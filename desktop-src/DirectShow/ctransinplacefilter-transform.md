---
description: Die Transform-Methode transformiert ein Beispiel direkt.
ms.assetid: 2268041b-70d4-48a9-9bb8-4ab921cce649
title: Ctransinplacefilter. Transform-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5b84f326807f730745268a217b6066dacb9aaa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372511"
---
# <a name="ctransinplacefiltertransform-method"></a>Ctransinplacefilter. Transform-Methode

Die- `Transform` Methode transformiert ein Beispiel direkt.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Transform(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                             | Beschreibung                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Stellen Sie dieses Beispiel nicht bereit.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                    |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode muss von der abgeleiteten Klasse implementiert werden. Transformieren Sie die Beispiel Daten an Ort und Stelle. Wenn der Filter zwei Zuweisungen verwendet, kopiert er die Daten aus dem Eingabe Beispiel in ein neues Beispiel und übergibt die Kopie an diese Methode.

Wenn der Filter dieses Beispiel nicht bereitstellt (z. b. zur Unterstützung der Qualitätskontrolle), sollte die Methode den Wert S false zurückgeben \_ .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransinplacefilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




