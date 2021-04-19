---
description: Die get \_ SessionID-Methode ruft den 32-Bit-NTP (Network Time Protocol)-Wert ab, der als Sitzungs Bezeichner fungiert. Diese wird automatisch generiert, wenn die Sitzung erstellt wird.
ms.assetid: 5177f120-4b93-40bc-9481-aedf65a8dee9
title: 'Itsdp:: get_SessionId-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad593b61f4c935a220e59383ae170569f04af54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358378"
---
# <a name="itsdpget_sessionid-method"></a>Itsdp:: get \_ SessionID-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ SessionID** -Methode ruft den 32-Bit-NTP (Network Time Protocol)-Wert ab, der als Sitzungs Bezeichner fungiert. Diese wird automatisch generiert, wenn die Sitzung erstellt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SessionId(
  [out] DOUBLE *pSessionId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psessionid* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den Sitzungs Bezeichner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *psessionid* -Parameter ist ungültig.<br/>             |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *psessionid* -Parameter ist kein gültiger Zeiger.<br/>   |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert dieser Methode kann **ulong** lauten, Visual Basic den **ulong** -Typ jedoch nicht unterstützt. Ein **Double** ist der nächste kleinste Typ, der den gesamten erforderlichen Wertebereich umfasst.

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

 

 




