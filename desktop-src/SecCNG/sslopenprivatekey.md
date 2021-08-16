---
description: Öffnet ein Handle für einen privaten Schlüssel.
ms.assetid: 2406be2c-121c-4475-b193-d370a88641da
title: SslOpenPrivateKey-Funktion (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenPrivateKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: bab1451ada84576ee33623dfdaa7d8dcad189e6d4ef8050b0b79fafaba11b49c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905649"
---
# <a name="sslopenprivatekey-function"></a>SslOpenPrivateKey-Funktion

Die **SslOpenPrivateKey-Funktion** öffnet ein Handle für einen [*privaten Schlüssel.*](/windows/desktop/SecGloss/p-gly)

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslOpenPrivateKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phPrivateKey,
  _In_  PCCERT_CONTEXT     pCertContext,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle für die SSL-Protokollanbieterinstanz [*(Secure Sockets Layer Protocol).*](/windows/desktop/SecGloss/s-gly)

</dd> <dt>

*phPrivateKey* \[ out\]
</dt> <dd>

Die Adresse eines Puffers, in den das Handle in den privaten Schlüssel geschrieben werden soll.

Wenn Sie die Verwendung des Schlüssels abgeschlossen haben, sollten Sie *phPrivateKey* freigeben, indem Sie die [**SslFreeObject-Funktion**](sslfreeobject.md) aufrufen.

</dd> <dt>

*pCertContext* \[ In\]
</dt> <dd>

Die Adresse des Zertifikats, aus dem der private Schlüssel abzurufen ist.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. folgende.



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Es ist nicht genügend Arbeitsspeicher verfügbar, um die erforderlichen Puffer zuzuordnen.<br/> |
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl>    | Das *hSslProvider-Handle* ist ungültig.<br/>                       |
| <dl> <dt>**NTE \_ INVALID \_ PARAMETER**</dt> <dt>0x80090027L</dt> </dl> | Der *parameter phPrivateKey* oder *pCertContext* ist **NULL.**<br/>   |



 

## <a name="remarks"></a>Hinweise

Der abgerufene private Schlüssel ist Teil eines [*öffentlichen/privaten Schlüsselpaars*](/windows/desktop/SecGloss/p-gly) innerhalb eines [*Zertifikats.*](/windows/desktop/SecGloss/c-gly) Diese Funktion extrahiert lediglich den privaten Schlüssel aus dem durch den *pCertContext-Parameter* angegebenen Zertifikat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

