---
description: 'Die receiveconnection-Methode akzeptiert eine Verbindung von einer anderen Pin. Diese Methode implementiert die IPin:: receiveconnection-Methode.'
ms.assetid: f17e7d93-ac45-4b8a-98c6-0c76ec7117c9
title: Cbasepin. receiveconnection-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ReceiveConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d0a8134201af1d3c931121f59a20360020a53a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355973"
---
# <a name="cbasepinreceiveconnection-method"></a>Cbasepin. receiveconnection-Methode

Die- `ReceiveConnection` Methode akzeptiert eine Verbindung von einer anderen Pin. Diese Methode implementiert die [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReceiveConnection(
   IPin          *pConnector,
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pconnector* 
</dt> <dd>

Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Verbindungs-PIN.

</dd> <dt>

*PMT* 
</dt> <dd>

Zeiger auf eine [**am \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die den Medientyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                                | Beschreibung                                                                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                                                                |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>                  | **Null** -Zeigerargument.<br/>                                              |
| <dl> <dt>**VFW \_ E \_ bereits \_ verbunden**</dt> </dl>  | Die PIN ist bereits verbunden.<br/>                                           |
| <dl> <dt>**VFW \_ E \_ nicht \_ angehalten**</dt> </dl>        | Der Filter ist aktiv, und die PIN unterstützt keine dynamische erneute Verbindung.<br/> |
| <dl> <dt>**VFW \_ E- \_ Typ \_ nicht \_ akzeptiert**</dt> </dl> | Der angegebene Medientyp ist nicht zulässig.<br/>                             |



 

## <a name="remarks"></a>Bemerkungen

Die Ausgabe-PIN ruft diese Methode für die Eingabe-PIN auf. Wenn die Eingabe-PIN einen Fehlercode zurückgibt, schlägt die Verbindung fehl.

In der-Basisklasse führt diese Methode die folgenden Schritte aus:

-   Überprüft, ob die PIN bereits verbunden ist.
-   Überprüft, ob der Filter beendet wurde.
-   Ruft die [**cbasepin:: checkConnect**](cbasepin-checkconnect.md) -Methode auf, um zu überprüfen, ob die Verbindungs-Pin geeignet ist.
-   Ruft die [**cbasepin:: checkmediatype**](cbasepin-checkmediatype.md) -Methode auf, um zu testen, ob der Medientyp zulässig ist.

Wenn alle diese Schritte erfolgreich ausgeführt wurden, ruft die-Methode die [**cbasepin:: completeconnect**](cbasepin-completeconnect.md) -Methode und die [**setmediatype**](cbasepin-setmediatype.md) -Methode auf, um die Verbindung abzuschließen. Diese Methoden speichern den Medientyp und einen Zeiger auf die Ausgabe-PIN.

Wenn **checkConnect** oder **checkmediatype** fehlschlägt, ruft die Basisklasse die [**cbasepin:: breakconnect**](cbasepin-breakconnect.md) -Methode auf, um die Verbindung zu unterbrechen, und gibt dann einen Fehlercode aus zurück `ReceiveConnection` .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




