---
description: Die Verbinden verbindet den Pin mit einem anderen Pin. Diese Methode implementiert die IPin::Verbinden-Methode.
ms.assetid: 8ea99d2f-09da-4b15-a3b0-04ceb7888bc1
title: CBasePin. Verbinden -Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a134b87e9c7c4d0f665ae37df7ec9cd0ecb3a37c0d0548f27835ead7b8ecca21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074794"
---
# <a name="cbasepinconnect-method"></a>CBasePin. Verbinden-Methode

Die `Connect` -Methode verbindet den Pin mit einem anderen Stecknadel. Diese Methode implementiert die [**IPin::Verbinden-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect)

## <a name="syntax"></a>Syntax


```C++
HRESULT Connect(
         IPin          *pReceivePin,
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Zeiger auf die IPin-Schnittstelle des [**empfangenden Pins.**](/windows/desktop/api/Strmif/nn-strmif-ipin)

</dd> <dt>

*Pmt* 
</dt> <dd>

Zeiger auf eine [**AM \_ MEDIA \_ TYPE-Struktur,**](/windows/win32/api/strmif/ns-strmif-am_media_type) die den Medientyp für die Verbindung angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die werte in der folgenden Tabelle.



| Rückgabecode                                                                                                  | Beschreibung                                                                        |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Erfolg.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ BEREITS \_ VERBUNDEN**</dt> </dl>    | Die Stecknadel ist bereits verbunden.<br/>                                           |
| <dl> <dt>**VFW \_ E \_ KEINE \_ ZULÄSSIGEN \_ TYPEN**</dt> </dl> | Ein zulässiger Medientyp wurde nicht finden.<br/>                                |
| <dl> <dt>**VFW \_ E \_ NICHT \_ BEENDET**</dt> </dl>          | Der Filter ist aktiv, und der Pin unterstützt keine dynamische wiederhergestellte Verbindung.<br/> |
| <dl> <dt>**VFW \_ \_ E-TYP \_ NICHT \_ AKZEPTIERT**</dt> </dl>   | Der angegebene Medientyp ist nicht akzeptabel.<br/>                             |



 

## <a name="remarks"></a>Hinweise

Der *pmt-Parameter* kann NULL **sein.** Sie kann auch einen partiellen Medientyp mit dem Wert GUID NULL für den Haupttyp, Untertyp oder \_ das Format angeben.

In der Basisklasse testet diese Methode, ob der Pin bereits verbunden ist und ob der Filter beendet wurde. Der Rest des Verbindungsprozesses wird an die [**CBasePin::AgreeMediaType-Methode delegiert.**](cbasepin-agreemediatype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




