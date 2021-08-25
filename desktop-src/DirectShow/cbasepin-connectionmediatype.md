---
description: Die ConnectionMediaType-Methode ruft den Medientyp für die aktuelle Stecknadelverbindung ab, falls dies der Fall ist. Diese Methode implementiert die IPin::ConnectionMediaType-Methode.
ms.assetid: 57d100ba-4171-4caa-ab98-66a0a327a53b
title: CBasePin.ConnectionMediaType-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectionMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cdeed52a212a659ca280163ea9513f0cb4f373ea2686bfde00078ebccb183daa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916750"
---
# <a name="cbasepinconnectionmediatype-method"></a>CBasePin.ConnectionMediaType-Methode

Die **ConnectionMediaType-Methode** ruft den Medientyp für die aktuelle Stecknadelverbindung ab, falls dies der Fall ist. Diese Methode implementiert die [**IPin::ConnectionMediaType-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype)

## <a name="syntax"></a>Syntax


```C++
HRESULT ConnectionMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pmt* 
</dt> <dd>

Zeiger auf eine [**AM \_ MEDIA \_ TYPE-Struktur,**](/windows/win32/api/strmif/ns-strmif-am_media_type) die den Medientyp empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die werte in der folgenden Tabelle.



| Rückgabecode                                                                                           | Beschreibung                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                   |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>             |  NULL-Zeigerargument.<br/> |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Die Stecknadel ist nicht verbunden.<br/>      |



 

## <a name="remarks"></a>Hinweise

Wenn die Stecknadel verbunden ist, kopiert diese Methode den Medientyp in die [**AM \_ MEDIA \_ TYPE-Struktur,**](/windows/win32/api/strmif/ns-strmif-am_media_type) die von *pmt angegeben wird.* Der Aufrufer muss den Formatblock des Medientyps frei geben. Sie können die [**CoTaskMemFree-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) oder die [**FreeMediaType-Hilfsfunktion**](freemediatype.md) verwenden.

Wenn die Stecknadel nicht verbunden ist, 0 (null) diese Methode den von *pmt* angegebenen Speicherblock und gibt einen Fehlercode zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

