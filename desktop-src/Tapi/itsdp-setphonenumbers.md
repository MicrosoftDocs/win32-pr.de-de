---
description: Die SetPhoneNumbers-Methode legt ein Array von Telefonnummern fest, die einem Konferenzblob zugeordnet sind.
ms.assetid: 674c08df-7e91-4f19-9d65-4bc6e7af117b
title: ITSdp::SetPhoneNumbers-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 733dfbe4752281abf4063f308a05aec73203d361e3c9c5dcebf413eb4ba2af72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140213"
---
# <a name="itsdpsetphonenumbers-method"></a>ITSdp::SetPhoneNumbers-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **SetPhoneNumbers-Methode** legt ein Array von Telefonnummern fest, die einem Konferenzblob zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPhoneNumbers(
  [in] VARIANT Numbers,
  [in] VARIANT Names
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zahlen* \[ In\]
</dt> <dd>

SAFEARRAY der **BSTR-Auflistung** von Telefonnummern.

</dd> <dt>

*Namen* \[ In\]
</dt> <dd>

SAFEARRAY der BSTR-Auflistungsnamen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *Numbers-* oder *Names-Parameter* ist ungültig.<br/>     |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Die Listen, auf die *Zahlen* und *Namen* verweisen, weisen die gleiche Länge auf.

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

 

 




