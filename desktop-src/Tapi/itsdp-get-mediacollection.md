---
description: Die get \_ mediacollection-Methode erhält einen Zeiger auf die itmediacollection-Schnittstelle für die Konferenz.
ms.assetid: 8109582a-74f0-47e8-91d1-0d89c3d3c331
title: 'Itsdp:: get_MediaCollection-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8812debf8c04fe022f24061660d6ea3bb5f162
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360366"
---
# <a name="itsdpget_mediacollection-method"></a>Itsdp:: get \_ mediacollection-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ mediacollection** -Methode erhält einen Zeiger auf die [**itmediacollection**](itmediacollection.md) -Schnittstelle für die Konferenz.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_MediaCollection(
  [out] ITMediaCollection **ppMediaCollection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppmediacollection* \[ vorgenommen\]
</dt> <dd>

Zeiger auf [**itmediacollection**](itmediacollection.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                                                           | Bedeutung                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                            | Methode war erfolgreich.<br/>                                                                |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>                                    | Der *ppmediacollection* -Parameter ist kein gültiger Zeiger.<br/>                        |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>                                   | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>                             |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>                                          | Unbekannter Fehler.<br/>                                                               |
| <dl> <dt>**HRESULT \_ aus \_ Fehler \_ Code ( \_ ungültige \_ Daten)**</dt> </dl> | Ein interner Fehler ist aufgetreten, normalerweise aufgrund des Fehlers einer vorherigen Methode.<br/> |
| <dl> <dt>**E \_ notimpl**</dt> </dl>                                       | Diese Methode ist noch nicht implementiert.<br/>                                              |



 

## <a name="remarks"></a>Bemerkungen

Ein [**itmediacollection**](itmediacollection.md) -Zeiger kann auch mithilfe von **QueryInterface** abgerufen werden.

TAPI Ruft die **adressf** -Methode für die [**itmediacollection**](itmediacollection.md) -Schnittstelle auf, die von **itsdp:: get \_ mediacollection** zurückgegeben wurde. Die Anwendung muss Release auf der **itmediacollection** -Schnittstelle aufzurufen, um Ressourcen frei **zugeben** , die ihr zugeordnet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itsdp**](itsdp.md)
</dt> <dt>

[**Itmediacollection**](itmediacollection.md)
</dt> </dl>

 

 




