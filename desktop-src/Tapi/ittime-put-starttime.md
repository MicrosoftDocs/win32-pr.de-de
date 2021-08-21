---
description: Die \_ StartTime-Methode put legt den Startzeitwert von 32-Bit-NTP (Network Time Protocol) fest. Die Sitzung gilt ab diesem Zeitpunkt als aktiv.
ms.assetid: c7c96265-4588-4f05-83b6-6ef54f02650b
title: ITTime::p ut_StartTime-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b0e1fe25f2518396ec507f88d0a89c5928f676b64d626c32307336b95ef21e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003228"
---
# <a name="ittimeput_starttime-method"></a>ITTime::p ut \_ StartTime-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **\_ StartTime-Methode put** legt den Startzeitwert von 32-Bit-NTP (Network Time Protocol) fest. Die Sitzung gilt ab diesem Zeitpunkt als aktiv.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_StartTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zeit* \[ In\]
</dt> <dd>

Startzeit für die Sitzung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *Tim* e-Parameter ist ungültig.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Diese Funktion kann Daten über das Kabel in unverschlüsselter Form senden. Daher kann eine Person, die im Netzwerk lauscht, die Daten lesen. Das Sicherheitsrisiko beim Senden der Daten in Klartext sollte vor der Verwendung dieser Methode berücksichtigt werden.

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

[**ITTime::get \_ StartTime**](ittime-get-starttime.md)
</dt> </dl>

 

 




