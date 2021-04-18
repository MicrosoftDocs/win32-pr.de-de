---
description: 'Die Connect-Methode verbindet die PIN mit einer anderen Pin. Diese Methode implementiert die IPin:: Connect-Methode.'
ms.assetid: 8ea99d2f-09da-4b15-a3b0-04ceb7888bc1
title: Cbasepin. Connect-Methode (amfilter. h)
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
ms.openlocfilehash: ed8bcdab7e0909e59e7d9ec00645786f8ce48c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364529"
---
# <a name="cbasepinconnect-method"></a>Cbasepin. Connect-Methode

Die- `Connect` Methode verbindet die PIN mit einer anderen Pin. Diese Methode implementiert die [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT Connect(
         IPin          *pReceivePin,
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*preceivepin* 
</dt> <dd>

Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der empfangenden PIN.

</dd> <dt>

*PMT* 
</dt> <dd>

Ein Zeiger auf eine [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die den Medientyp für die Verbindung angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                                  | Beschreibung                                                                        |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Erfolg.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ bereits \_ verbunden**</dt> </dl>    | Die PIN ist bereits verbunden.<br/>                                           |
| <dl> <dt>**VFW \_ E \_ keine \_ akzeptablen \_ Typen**</dt> </dl> | Es konnte kein akzeptabler Medientyp gefunden werden.<br/>                                |
| <dl> <dt>**VFW \_ E \_ nicht \_ angehalten**</dt> </dl>          | Der Filter ist aktiv, und die PIN unterstützt keine dynamische erneute Verbindung.<br/> |
| <dl> <dt>**VFW \_ E- \_ Typ \_ nicht \_ akzeptiert**</dt> </dl>   | Der angegebene Medientyp ist nicht zulässig.<br/>                             |



 

## <a name="remarks"></a>Bemerkungen

Der *PMT* -Parameter kann **null** sein. Außerdem kann ein partieller Medientyp mit dem Wert GUID \_ NULL für den Haupttyp, den Untertyp oder das Format angegeben werden.

In der Basisklasse testet diese Methode, ob die PIN bereits verbunden ist und ob der Filter beendet wurde. Der Rest des Verbindungsprozesses wird an die [**cbasepin:: agreemediatype**](cbasepin-agreemediatype.md) -Methode delegiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




