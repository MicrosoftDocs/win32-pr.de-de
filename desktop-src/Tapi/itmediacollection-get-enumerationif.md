---
description: Die get \_ enumerationif-Methode ruft einen Zeiger auf eine mediumenumerationsschnittstelle ab.
ms.assetid: d5f1e10f-e5ad-45e6-a5ec-024905603012
title: 'Itmediacollection:: get_EnumerationIf-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a7e7d85c1f7a433a31360fabc8b5dac71e68ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365681"
---
# <a name="itmediacollectionget_enumerationif-method"></a>Itmediacollection:: get \_ enumerationif-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ enumerationif** -Methode ruft einen Zeiger auf eine mediumenumerationsschnittstelle ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_EnumerationIf(
  [out] IEnumMedia **pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PVal* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die [**ienummedia**](ienummedia.md) -Schnittstelle für das gewünschte Element.

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

Diese Methode ist mit [**get \_ \_ netwenum**](itmediacollection-get--newenum.md) austauschbar, mit dem Unterschied, dass Sie [**ienummedia**](ienummedia.md) anstelle von **IUnknown** zurückgibt.

TAPI Ruft die **adressf** -Methode für die [**ienummedia**](ienummedia.md) -Schnittstelle auf, die von **itmediacollection:: get \_ enumerationlf** zurückgegeben wurde. Die Anwendung muss Release auf der **ienummedia** -Schnittstelle aufzurufen, um Ressourcen frei **zugeben** , die ihr zugeordnet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ienummedia**](ienummedia.md)
</dt> <dt>

[**Itmediacollection**](itmediacollection.md)
</dt> </dl>

 

 




