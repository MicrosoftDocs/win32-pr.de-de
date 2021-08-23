---
description: Die get \_ SessionId-Methode ruft den 32-Bit-NTP-Wert (Network Time Protocol) ab, der als Sitzungsbezeichner dient. Dies wird automatisch generiert, wenn die Sitzung erstellt wird.
ms.assetid: 5177f120-4b93-40bc-9481-aedf65a8dee9
title: ITSdp::get_SessionId-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67f7e8ea9bef17e5cb34ca23443b1f16f815c964c3cf76b9b122878e8662d051
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621540"
---
# <a name="itsdpget_sessionid-method"></a>ITSdp::get \_ SessionId-Methode

\[Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **get \_ SessionId-Methode** ruft den 32-Bit-NTP-Wert (Network Time Protocol) ab, der als Sitzungsbezeichner dient. Dies wird automatisch generiert, wenn die Sitzung erstellt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SessionId(
  [out] DOUBLE *pSessionId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSessionId* \[ out\]
</dt> <dd>

Zeiger auf den Sitzungsbezeichner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *pSessionId-Parameter* ist ungültig.<br/>             |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Der *pSessionId-Parameter* ist kein gültiger Zeiger.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Der Rückgabewert dieser Methode kann **ULONG** sein, aber Visual Basic unterstützt den **ULONG-Typ** nicht. Ein **DOUBLE** ist der kleinste Typ, der den gesamten erforderlichen Wertebereich umfasst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




