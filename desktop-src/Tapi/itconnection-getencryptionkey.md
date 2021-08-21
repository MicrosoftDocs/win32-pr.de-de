---
description: Die GetEncryptionKey-Methode ruft den Verschlüsselungsschlüssel ab.
ms.assetid: a80d8660-d13e-483f-b1d7-ee2043ef5cab
title: ITConnection::GetEncryptionKey-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a237073d4842cd26797b046a4d973390ff5ef254b574bcafbc6f10abca932aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060978"
---
# <a name="itconnectiongetencryptionkey-method"></a>ITConnection::GetEncryptionKey-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **GetEncryptionKey-Methode** ruft den Verschlüsselungsschlüssel ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetEncryptionKey(
  [out] BSTR         *ppKeyType,
  [out] VARIANT_BOOL *pfValidKeyData,
  [out] BSTR         *ppKeyData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppKeyType* \[ out\]
</dt> <dd>

Zeiger auf einen **BSTR,** der den Typ des Verschlüsselungsschlüssels enthält.

</dd> <dt>

*pfValidKeyData* \[ out\]
</dt> <dd>

Gibt die Gültigkeit von Verschlüsselungsschlüsseldaten an.

</dd> <dt>

*ppKeyData* \[ out\]
</dt> <dd>

Zeiger auf einen **BSTR,** der die Verschlüsselungsschlüsseldaten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                                                 |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Der *parameter ppKeyType, pfValidKeyData* oder *ppKeyData* ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/>                              |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                                                |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                                               |



 

## <a name="remarks"></a>Hinweise

Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für die Parameter *ppKeyType* und *ppKeyData* belegten Arbeitsspeicher freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

