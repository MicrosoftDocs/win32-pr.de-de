---
description: Die get \_ enumerationif-Methode gibt die ienumtime-Enumerationsschnittstelle zurück, die ittime auflistet.
ms.assetid: 31f6fa94-d047-4c53-96ae-8dd7e66a4e33
title: 'Ittimecollection:: get_EnumerationIf-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a698fca73e923597b2dff5b82e3258dd79306f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356414"
---
# <a name="ittimecollectionget_enumerationif-method"></a>Ittimecollection:: get \_ enumerationif-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ enumerationif** -Methode gibt die [**ienumtime**](ienumtime.md) -Enumerationsschnittstelle zurück, die [**ittime**](ittime.md)auflistet.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_EnumerationIf(
  [out] IEnumTime **pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PVal* \[ vorgenommen\]
</dt> <dd>

Zeiger auf die [**ienumtime**](ienumtime.md) -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *PVal* -Parameter ist kein gültiger Zeiger.<br/>         |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ist mit [**get \_ \_ netwenum**](ittimecollection-get--newenum.md) austauschbar, mit der Ausnahme, dass Sie [**ienumtime**](ienumtime.md) anstelle von **IUnknown** zurückgibt.

TAPI Ruft die **adressf** -Methode für die [**ienumtime**](ienumtime.md) -Schnittstelle auf, die von **ittimecollection:: get \_ enumerationif** zurückgegeben wurde. Die Anwendung muss Release auf der [**ienumtime**](ienumtime.md) -Schnittstelle aufzurufen, um Ressourcen frei **zugeben** , die ihr zugeordnet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ienumtime**](ienumtime.md)
</dt> <dt>

[**Ittimecollection**](ittimecollection.md)
</dt> <dt>

[**Ittime**](ittime.md)
</dt> </dl>

 

 




