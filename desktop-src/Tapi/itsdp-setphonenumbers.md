---
description: Mit der setphonenumbers-Methode wird ein Array von Telefonnummern festgelegt, die einem Konferenz-BLOB zugeordnet sind.
ms.assetid: 674c08df-7e91-4f19-9d65-4bc6e7af117b
title: 'Itsdp:: setphonenumbers-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30ec2820d8d033ac2eed9d9287c3ca52c9deb316
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367086"
---
# <a name="itsdpsetphonenumbers-method"></a>Itsdp:: setphonenumbers-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Mit der **setphonenumbers** -Methode wird ein Array von Telefonnummern festgelegt, die einem Konferenz-BLOB zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPhoneNumbers(
  [in] VARIANT Numbers,
  [in] VARIANT Names
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zahlen* \[ in\]
</dt> <dd>

SafeArray von **BSTR** s Auflisten von Telefonnummern.

</dd> <dt>

*Namen* \[ in\]
</dt> <dd>

SafeArray von **BSTR** s-Auflistungs Namen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der Parameter " *Numbers* " und " *Names* " ist ungültig.<br/>     |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Die Liste, auf die *Zahlen* und *Namen* zeigen, ist dieselbe Länge.

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
</dt> </dl>

 

 




