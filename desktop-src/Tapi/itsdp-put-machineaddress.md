---
description: Die \_ Put MachineAddress-Methode legt die Computeradresse des ursprünglichen Hosts fest.
ms.assetid: f4af55b1-e20b-4fe8-a15e-a1a68d22f1b9
title: ITSdp::p ut_MachineAddress-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974286e846268686423d0ebdbbd083d07e9946401cb0192713b200b2354b89c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060798"
---
# <a name="itsdpput_machineaddress-method"></a>ITSdp::p ut \_ MachineAddress-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **\_ Put MachineAddress-Methode** legt die Computeradresse des ursprünglichen Hosts fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_MachineAddress(
  [in] BSTR pMachineAddress
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMachineAddress* \[ In\]
</dt> <dd>

Zeiger auf einen **BSTR,** der die Computeradresse des Konferenzhosts enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                       |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Der *pMachineAddress-Parameter* ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/>    |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                      |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                     |



 

## <a name="remarks"></a>Hinweise

Die Anwendung muss [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) verwenden, um Arbeitsspeicher für den *pMachineAddress-Parameter* zu belegen, und [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.

Der *pMachineAddress-Parameter* kann entweder ein DNS-Name ("JohnSmith.workinghard.microsoft.com") oder eine IP-Adresse ("10.111.222.111") sein.

Diese Funktion kann Daten über das Kabel in unverschlüsselter Form senden. Daher kann eine Person, die im Netzwerk lauscht, die Daten lesen. Das Sicherheitsrisiko beim Senden der Daten in Klartext sollte vor der Verwendung dieser Methode berücksichtigt werden.

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

[**ITSdp::get \_ MachineAddress**](itsdp-get-machineaddress.md)
</dt> </dl>

 

