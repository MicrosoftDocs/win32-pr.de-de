---
description: Mit der changemediatype-Methode wird der Medientyp für die Verbindung dynamisch geändert.
ms.assetid: 38efdfdc-f636-4cad-b8d3-8c63a277644e
title: Cdynamicoutputpin. changemediatype-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89c15e3076a95f8fee3f2f2970fc59da5cf3bf4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352156"
---
# <a name="cdynamicoutputpinchangemediatype-method"></a>Cdynamicoutputpin. changemediatype-Methode

Die- `ChangeMediaType` Methode ändert den Medientyp für die Verbindung dynamisch. Die Änderung kann auftreten, während das Filter Diagramm ausgeführt wird. Nachdem diese Methode aufgerufen wurde, können keine Beispiele mit dem alten Medientyp übermittelt werden. Der Aufrufer muss sicherstellen, dass keine alten Beispiele ausstehend sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT ChangeMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PMT* 
</dt> <dd>

Zeiger auf eine [**am \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die den Medientyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                           | Beschreibung                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                                                                                                                      |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>                | Fehler. Möglicherweise hat der besitzende Filter [**cdynamicoutputpin:: setconfiginfo**](cdynamicoutputpin-setconfiginfo.md)nicht aufgerufen.<br/> |
| <dl> <dt>**VFW \_ E \_ nicht \_ verbunden**</dt> </dl> | Die PIN ist nicht verbunden.<br/>                                                                                                     |



 

## <a name="remarks"></a>Bemerkungen

Rufen Sie die [**cdynamicoutputpin:: startusingoutputpin**](cdynamicoutputpin-startusingoutputpin.md) -Methode auf, bevor Sie diese Methode aufrufen.

Diese Methode prüft zunächst, ob die downstreameingabepin das neue Format akzeptieren kann, ohne dass eine erneute Verbindung hergestellt Er fragt die Eingabe-PIN für die [**ipinconnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) -Schnittstelle ab. Wenn die eingabepin **ipinconnection** unterstützt, ruft die Methode die [**ipinconnection::D ynamicqueryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) -Methode mit dem vorgeschlagenen Medientyp auf. Wenn die Eingabe-PIN den neuen Medientyp annimmt, ruft die Methode die [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) -Methode auf und verhandelt die zuordneranforderungen erneut.

Wenn dagegen der Downstream-Pin **ipinconnection** nicht unterstützt, oder wenn der neue Medientyp abgelehnt wird, ruft die-Methode die [**cdynamicoutputpin::D ynamikreconnect**](cdynamicoutputpin-dynamicreconnect.md) -Methode auf, um eine dynamische erneute Verbindung auszuführen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdynamicoutputpin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




