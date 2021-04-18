---
description: Mit der get \_ machineaddress-Methode wird die Computer Adresse des Ursprungs Hosts abgerufen.
ms.assetid: 8a67cc9f-f9fc-4ec3-86f9-ffe34d075830
title: 'Itsdp:: get_MachineAddress-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34968efa16f04cba8f99dbc0dc42b0cf4995a43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364885"
---
# <a name="itsdpget_machineaddress-method"></a>Itsdp:: get \_ machineaddress-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Mit der **get \_ machineaddress** -Methode wird die Computer Adresse des Ursprungs Hosts abgerufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_MachineAddress(
  [out] BSTR *ppMachineAddress
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppmachineaddress* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen **BSTR** -Wert, der die Computer Adresse des Konferenz Hosts enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                        |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *ppmachineaddres* s-Parameter ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>     |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                       |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                      |



 

## <a name="remarks"></a>Bemerkungen

Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *ppmachineaddress* -Parameter zugewiesenen Arbeitsspeicher freizugeben.

Der *ppmachineaddress* -Parameter kann entweder als DNS-Name ("johnsmith.workinghard.Microsoft.com") oder als IP-Adresse ("10.111.222.111") zurückgegeben werden.

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
</dt> <dt>

[**Itsdp::p UT \_ machineaddress**](itsdp-put-machineaddress.md)
</dt> </dl>

 

