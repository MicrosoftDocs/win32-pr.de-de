---
description: Die Transform-Methode transformiert ein Beispiel an Ort und Stelle.
ms.assetid: 2268041b-70d4-48a9-9bb8-4ab921cce649
title: CTransInPlaceFilter.Transform-Methode (Transip.h)
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
ms.openlocfilehash: 224052bc882792f57eedf9ea58842b953e5853012d3581ef14cad58467b614b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953399"
---
# <a name="ctransinplacefiltertransform-method"></a>CTransInPlaceFilter.Transform-Methode

Die `Transform` -Methode transformiert ein Beispiel an Ort und Stelle.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Transform(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSample* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                             | Beschreibung                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Übermitteln Sie dieses Beispiel nicht.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                    |



 

## <a name="remarks"></a>Hinweise

Die abgeleitete Klasse muss diese Methode implementieren. Transformieren Sie die Beispieldaten. Wenn der Filter zwei Zuweisungen verwendet, kopiert er die Daten aus dem Eingabebeispiel in ein neues Beispiel und übergibt die Kopie an diese Methode.

Wenn der Filter dieses Beispiel nicht bereitstellen soll (z. B. zur Unterstützung der Qualitätskontrolle), sollte die Methode S \_ FALSE zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransInPlaceFilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




