---
description: Die get \_ StartTime-Methode ruft den 32-Bit-NTP-Startzeitwert (Network Time Protocol) ab. Die Sitzung gilt ab diesem Zeitpunkt als aktiv.
ms.assetid: 511e4486-4c73-4610-8e64-9c70acc98eab
title: ITTime::get_StartTime-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea2fcc7aedf94d65f828714a7ebe5e6bbbfd760514654b2b634b479f2fd4802b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060758"
---
# <a name="ittimeget_starttime-method"></a>ITTime::get \_ StartTime-Methode

\[Steuerelemente und Schnittstellen für Rendezvous-IP-Telefoniekonferenzen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **get \_ StartTime-Methode** ruft den 32-Bit-NTP-Startzeitwert (Network Time Protocol) ab. Die Sitzung gilt ab diesem Zeitpunkt als aktiv.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_StartTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTime* \[ out\]
</dt> <dd>

Zeiger auf die Startzeit für die Sitzung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Der *pTime-Parameter* ist kein gültiger Zeiger.<br/>        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITTime**](ittime.md)
</dt> <dt>

[**ITTime::put \_ StartTime**](ittime-put-starttime.md)
</dt> </dl>

 

 




