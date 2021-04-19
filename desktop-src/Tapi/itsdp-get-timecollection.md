---
description: Die get \_ timecollection-Methode erhält einen Zeiger auf eine ittimecollection-Schnittstelle für die Konferenz.
ms.assetid: 1cfe3f5a-dcf7-480b-9b23-e17259d8ee9c
title: 'Itsdp:: get_TimeCollection-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1bac0f38f8c96762d4e36d8d3dfdff2136bdb86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368646"
---
# <a name="itsdpget_timecollection-method"></a>Itsdp:: get \_ timecollection-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ timecollection** -Methode erhält einen Zeiger auf eine [**ittimecollection**](ittimecollection.md) -Schnittstelle für die Konferenz.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_TimeCollection(
  [out] ITTimeCollection **ppTimeCollection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pptimecollection* \[ vorgenommen\]
</dt> <dd>

Zeiger auf [**ittimecollection**](ittimecollection.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                                                           | Bedeutung                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                            | Methode war erfolgreich.<br/>                                                                |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>                                    | Der *pptimecollection* -Parameter ist kein gültiger Zeiger.<br/>                         |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>                                   | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>                             |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>                                          | Unbekannter Fehler.<br/>                                                               |
| <dl> <dt>**HRESULT \_ aus \_ Fehler \_ Code ( \_ ungültige \_ Daten)**</dt> </dl> | Ein interner Fehler ist aufgetreten, normalerweise aufgrund des Fehlers einer vorherigen Methode.<br/> |
| <dl> <dt>**E \_ notimpl**</dt> </dl>                                       | Diese Methode ist noch nicht implementiert.<br/>                                              |



 

## <a name="remarks"></a>Bemerkungen

Ein [**ittimecollection**](ittimecollection.md) -Zeiger kann auch mithilfe von **QueryInterface** abgerufen werden.

TAPI Ruft die **adressf** -Methode für die [**ittimecollection**](ittimecollection.md) -Schnittstelle auf, die von **itsdp:: get \_ timecollection** zurückgegeben wurde. Die Anwendung muss Release auf der **ittimecollection** -Schnittstelle aufzurufen, um Ressourcen frei **zugeben** , die ihr zugeordnet sind.

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

[**Ittimecollection**](ittimecollection.md)
</dt> </dl>

 

 




