---
description: Die get \_ MachineAddress-Methode ruft die Computeradresse des ursprünglichen Hosts ab.
ms.assetid: 8a67cc9f-f9fc-4ec3-86f9-ffe34d075830
title: ITSdp::get_MachineAddress-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a4e4d849c17d6c371a6edc927679e2ba6af344fbf8515310eb22b27ba4abeab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012930"
---
# <a name="itsdpget_machineaddress-method"></a>ITSdp::get \_ MachineAddress-Methode

\[Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **get \_ MachineAddress-Methode** ruft die Computeradresse des ursprünglichen Hosts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_MachineAddress(
  [out] BSTR *ppMachineAddress
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppMachineAddress* \[ out\]
</dt> <dd>

Zeiger auf einen **BSTR,** der die Computeradresse des Konferenzhosts enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                        |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Der *ppMachineAddres-Parameter* ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/>     |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                       |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                      |



 

## <a name="remarks"></a>Hinweise

Die Anwendung muss [**SysFreeString verwenden,**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) um den für den *ppMachineAddress-Parameter* zugeordneten Arbeitsspeicher frei zu geben.

Der *ppMachineAddress-Parameter* kann entweder als DNS-Name ("JohnSmith.workinghard.microsoft.com") oder als IP-Adresse ("10.111.222.111") zurückgegeben werden.

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
</dt> <dt>

[**ITSdp::put \_ MachineAddress**](itsdp-put-machineaddress.md)
</dt> </dl>

 

