---
description: Berechnet den Hash, der in der fertigen Nachricht des SSL-Handshakes (Secure Sockets Layer Protocol) gesendet wird.
ms.assetid: 82dfeb1d-c141-40c9-b692-daad78ab6d55
title: SslComputeFinishedHash-Funktion (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeFinishedHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e0f23a58111bfcebbe668cd3b6c50a135da0dae240907f09a65d60ef1cebdda8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907141"
---
# <a name="sslcomputefinishedhash-function"></a>SslComputeFinishedHash-Funktion

Die **SslComputeFinishedHash-Funktion** berechnet den [*Hash,*](/windows/desktop/SecGloss/h-gly) der in der fertigen Nachricht des SSL-Handshakes [*(Secure Sockets Layer Protocol)*](/windows/desktop/SecGloss/s-gly) gesendet wird. Weitere Informationen zur SSL-Handshakesequenz finden Sie unter [Beschreibung des ssl-Handshakes (Secure Sockets Layer).](https://support.microsoft.com/kb/257591)

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslComputeFinishedHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle der SSL-Protokollanbieterinstanz.

</dd> <dt>

*hMasterKey* \[ In\]
</dt> <dd>

Das Handle des [*Hauptschlüsselobjekts.*](/windows/desktop/SecGloss/m-gly)

</dd> <dt>

*hHandshakeHash* \[ In\]
</dt> <dd>

Das Handle des Hashs der Handshakenachrichten.

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Hash für die Fertigmeldung empfängt.

</dd> <dt>

*cbOutput* \[ In\]
</dt> <dd>

Die Länge des *pbOutput-Puffers* in Bytes.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Eine der folgenden Konstanten.



| Wert                                                                                                                                                                                                                                                      | Bedeutung                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <dt>**NCRYPT \_ \_ \_ SSL-CLIENTFLAG-0x00000001**</dt> <dt></dt> </dl> | Gibt an, dass dies ein Clientaufruf ist.<br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <dt>**NCRYPT \_ SSL SERVER \_ \_ FLAG**</dt> <dt>0x00000002</dt> </dl> | Gibt an, dass dies ein Serveraufruf ist.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.



| Rückgabecode/-wert                                                                                                                                                                | BESCHREIBUNG                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>2148073510 (0x80090026)</dt> </dl> | Einer der angegebenen Handles ist ungültig.<br/> |



 

## <a name="remarks"></a>Hinweise

Die **SslComputeFinishedHash-Funktion** ist eine von drei Funktionen, die verwendet werden, um einen Hash zu generieren, der während des SSL-Handshakes verwendet wird.

1.  Die [**SslCreateHandshakeHash-Funktion**](sslcreatehandshakehash.md) wird aufgerufen, um ein Hashhandle abzurufen.
2.  Die [**SslHashHandshake-Funktion**](sslhashhandshake.md) wird beliebig oft mit dem Hashhandle aufgerufen, um dem Hash Daten hinzuzufügen.
3.  Die **SslComputeFinishedHash-Funktion** wird mit dem Hashhandle aufgerufen, um den Digest der Hashdaten abzurufen.

Der Hashwert wird durch Hashing des geheimen Hauptschlüssels mit einem Hash aller vorherigen gesendeten oder empfangenen Handshakenachrichten berechnet.

Der Wert von *cbOutput* bestimmt die Länge der Hashdaten. Wenn das [*tls 1.0-Protokoll (Transport Layer Security Protocol)*](/windows/desktop/SecGloss/t-gly) verwendet wird, sollte dies immer 12 (Bytes) sein. Weitere Informationen finden Sie unter [Die TLS-Protokollversion 1.0.](https://www.ietf.org/rfc/rfc2246.txt)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

