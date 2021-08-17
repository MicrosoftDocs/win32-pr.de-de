---
description: Die GetEmailNames-Methode ruft ein Array von E-Mail-Namen ab, die dem Konferenzblob zugeordnet sind.
ms.assetid: e51f25d7-41e5-408e-930b-396c7ac24437
title: ITSdp::GetEmailNames-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f74ea369210a6ca32e47bb3359000195c544374b7352da96570f6d0f58f2af4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140263"
---
# <a name="itsdpgetemailnames-method"></a>ITSdp::GetEmailNames-Methode

\[Steuerelemente und Schnittstellen für Rendezvous-IP-Telefoniekonferenzen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **GetEmailNames-Methode** ruft ein Array von E-Mail-Namen ab, die dem Konferenzblob zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetEmailNames(
  [out] VARIANT *pAddresses,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAddresses* \[ out\]
</dt> <dd>

**VARIANT-Zeiger** auf ein SAFEARRAY der **BSTR-Auflistung** von E-Mail-Adressen.

</dd> <dt>

*pNames* \[ out\]
</dt> <dd>

**VARIANT-Zeiger** auf safearray von **BSTR-Auflistungsnamen.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                              |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Der *pAddresses-* oder *pNames-Parameter* ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/>           |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                             |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                            |



 

## <a name="remarks"></a>Hinweise

Die Listen, *auf die pAddresses* und *pNames* zeigen, haben die gleiche Länge.

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

 

 




