---
description: Die \_ Methode get SessionVersion ruft den 32-Bit-Wert (idealerweise Netzwerkzeitprotokoll oder NTP) ab, der als Sitzungsversion dient.
ms.assetid: 39c2aef4-24e3-4ea0-8b23-dff842f9ab84
title: ITSdp::get_SessionVersion-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7661fb5f133d214748991510d56387991872fa69243353b5144623a1ef19f91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476590"
---
# <a name="itsdpget_sessionversion-method"></a>ITSdp::get \_ SessionVersion-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **\_ Methode get SessionVersion** ruft den 32-Bit-Wert (idealerweise Netzwerkzeitprotokoll oder NTP) ab, der als Sitzungsversion dient. Obwohl dies beim Erstellen der Sitzung automatisch generiert wird, ist der Benutzer dafür verantwortlich, sie zu ändern, wenn der SDP geändert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SessionVersion(
  [out] DOUBLE *pSessionVersion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSessionVersion* \[ out\]
</dt> <dd>

Zeiger auf den Sitzungsversionsbezeichner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *pSessionVersion-Parameter* ist ungültig.<br/>           |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Der *pSessionVersion-Parameter* ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/>    |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                      |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                     |



 

## <a name="remarks"></a>Hinweise

Der Rückgabewert dieser Methode kann **ULONG** sein, aber Visual Basic unterstützt den **ULONG-Typ** nicht. Ein **DOUBLE** ist der nächstkleinste Typ, der den gesamten erforderlichen Wertebereich umfasst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp::put \_ SessionVersion**](itsdp-put-sessionversion.md)
</dt> </dl>

 

 




