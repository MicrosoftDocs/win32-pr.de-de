---
description: Die SetEmailNames-Methode legt ein Array von E-Mail-Adressen fest, die dem Konferenzblob zugeordnet sind.
ms.assetid: 1d6d5b01-bc0f-455f-8b23-bc0f409afde4
title: ITSdp::SetEmailNames-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23fa550c5750a3fad5d0b20ccdf2e032ed98c20a10b2f8e758ea7c9874e05a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140233"
---
# <a name="itsdpsetemailnames-method"></a>ITSdp::SetEmailNames-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **SetEmailNames-Methode** legt ein Array von E-Mail-Adressen fest, die dem Konferenzblob zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetEmailNames(
  [in] VARIANT Addresses,
  [in] VARIANT Names
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Adressen* \[ In\]
</dt> <dd>

SAFEARRAY der **BSTR-Auflistung** von E-Mail-Adressen.

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
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *Addresses-* oder *Names-Parameter* ist ungültig.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Die Listen, auf die *Adressen* und *Namen* verweisen, weisen die gleiche Länge auf.

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

 

 




