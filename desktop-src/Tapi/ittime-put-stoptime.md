---
description: Die put \_ StopTime-Methode legt den Endzeitwert von NTP (Network Time Protocol) fest. Wenn die Endzeit 0 (null) ist, ist die Sitzung nicht gebunden.
ms.assetid: 6f07054c-5fb2-4ee4-9025-3acf9b51ddbd
title: ITTime::p ut_StopTime-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e3aa32615988e52ccaa845a8fb7ec52f2e863c7193ee393d7d184e2b3002f59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762382"
---
# <a name="ittimeput_stoptime-method"></a>ITTime::p ut \_ StopTime-Methode

\[Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **put \_ StopTime-Methode** legt den Endzeitwert von NTP (Network Time Protocol) fest. Wenn die Endzeit 0 (null) ist, ist die Sitzung nicht gebunden.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_StopTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zeit* \[ In\]
</dt> <dd>

Die Stoppzeit für die Sitzung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *Time-Parameter* ist ungültig.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Diese Funktion kann Daten unverschlüsselt über das Netzwerk senden. Aus diesem Grund kann eine Person, die im Netzwerk abhört, die Daten lesen. Das Sicherheitsrisiko des Sendens der Daten in Klartext sollte vor der Verwendung dieser Methode berücksichtigt werden.

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

[**ITTime::get \_ StopTime**](ittime-get-stoptime.md)
</dt> </dl>

 

 




