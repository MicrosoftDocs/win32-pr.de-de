---
description: Die getencryptionkey-Methode ruft den Verschlüsselungsschlüssel ab.
ms.assetid: a80d8660-d13e-483f-b1d7-ee2043ef5cab
title: 'Itconnection:: getencryptionkey-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a826dc8424222587f2838804ec035fb23c2e41d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359293"
---
# <a name="itconnectiongetencryptionkey-method"></a>Itconnection:: getencryptionkey-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **getencryptionkey** -Methode ruft den Verschlüsselungsschlüssel ab.

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

*ppkeytype* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen **BSTR** -Wert, der den Typ des Verschlüsselungsschlüssels enthält.

</dd> <dt>

*pfvalidkeydata* \[ vorgenommen\]
</dt> <dd>

Gibt die Gültigkeit der Verschlüsselungsschlüssel Daten an.

</dd> <dt>

*ppkeydata* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen **BSTR** -Wert, der die Verschlüsselungsschlüssel Daten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                                                 |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *ppkeytype-, pfvalidkeydata* -oder *ppkeydata* -Parameter ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>                              |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                                                |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                                               |



 

## <a name="remarks"></a>Bemerkungen

Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für die Parameter *ppkeytype* und *ppkeydata* zugewiesenen Arbeitsspeicher freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itconnection**](itconnection.md)
</dt> </dl>

 

