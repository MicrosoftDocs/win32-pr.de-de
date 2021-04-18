---
description: Die get \_ StartTime-Methode ruft den 32-Bit-NTP (Network Time Protocol)-Start Zeitwert ab. Die Sitzung gilt ab diesem Zeitpunkt als aktiv.
ms.assetid: 511e4486-4c73-4610-8e64-9c70acc98eab
title: 'Ittime:: get_StartTime-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 051096c6cbdab1960c67ddb2cbcaf57eccab9556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351268"
---
# <a name="ittimeget_starttime-method"></a>Ittime:: get \_ StartTime-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ StartTime** -Methode ruft den 32-Bit-NTP (Network Time Protocol)-Start Zeitwert ab. Die Sitzung gilt ab diesem Zeitpunkt als aktiv.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_StartTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PTIME* \[ vorgenommen\]
</dt> <dd>

Zeiger auf die Startzeit der Sitzung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *PTIME* -Parameter ist kein gültiger Zeiger.<br/>        |
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

[**Ittime**](ittime.md)
</dt> <dt>

[**Ittime::p UT- \_ StartTime**](ittime-put-starttime.md)
</dt> </dl>

 

 




