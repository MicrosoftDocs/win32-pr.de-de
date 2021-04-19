---
description: Die get \_ IsValid-Methode überprüft das Sitzungs Deskriptor-Protokoll (SDP; siehe RFC 2327) für Struktur-und Feldwerte.
ms.assetid: a3f849ac-bda9-4937-bf3b-bce8df20cbf0
title: 'Itsdp:: get_IsValid-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ca3cfdc1061e0a2830010ec39b2e6667c9341c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367212"
---
# <a name="itsdpget_isvalid-method"></a>Itsdp:: get \_ IsValid-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ IsValid** -Methode überprüft das Sitzungs Deskriptor-Protokoll (SDP; siehe RFC 2327) für Struktur-und Feldwerte.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_IsValid(
  [out] VARIANT_BOOL *pfIsValid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfisvalid* \[ vorgenommen\]
</dt> <dd>

Gibt an, ob die BLOB-Struktur gültig ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *pfisvalid* -Parameter ist ungültig.<br/>              |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *pfisvalid* -Parameter ist kein gültiger Zeiger.<br/>    |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

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

 

 




