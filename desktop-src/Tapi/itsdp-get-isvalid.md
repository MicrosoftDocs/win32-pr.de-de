---
description: Die get \_ IsValid-Methode überprüft das SDP-Blob (Session Descriptor Protocol; siehe RFC 2327) auf Struktur- und Feldwerte.
ms.assetid: a3f849ac-bda9-4937-bf3b-bce8df20cbf0
title: ITSdp::get_IsValid-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1674b51c605354a021948a63a0e993578a3d0114e625acec2cb9e24238423c56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140293"
---
# <a name="itsdpget_isvalid-method"></a>ITSdp::get \_ IsValid-Methode

\[Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **get \_ IsValid-Methode** überprüft das SDP-Blob (Session Descriptor Protocol; siehe RFC 2327) auf Struktur- und Feldwerte.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_IsValid(
  [out] VARIANT_BOOL *pfIsValid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfIsValid* \[ out\]
</dt> <dd>

Gibt an, ob die Blobstruktur gültig ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *parameter pfIsValid* ist ungültig.<br/>              |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Der *pfIsValid-Parameter* ist kein gültiger Zeiger.<br/>    |
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

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




