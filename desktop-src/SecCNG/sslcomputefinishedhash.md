---
description: Berechnet den Hash, der in der abgeschlossenen Nachricht des SSL-Handshakes (Secure Sockets Layer Protocol) gesendet wurde.
ms.assetid: 82dfeb1d-c141-40c9-b692-daad78ab6d55
title: Sslcomputefinishedhash-Funktion (sslprovider. h)
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
ms.openlocfilehash: 365f3c849b0a499d2bd875c8d234bbda1911eb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959433"
---
# <a name="sslcomputefinishedhash-function"></a>Sslcomputefinishedhash-Funktion

Die **sslcomputefinishedhash** -Funktion berechnet den [*Hash*](/windows/desktop/SecGloss/h-gly) , der in der fertigen Nachricht des SSL-Handshakes ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ) gesendet wurde. Weitere Informationen zur SSL-Handshake-Sequenz finden Sie unter [Beschreibung des Secure Sockets Layer (SSL) Handshake](https://support.microsoft.com/kb/257591).

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

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle der SSL-Protokoll Anbieter Instanz.

</dd> <dt>

*hmasterkey* \[ in\]
</dt> <dd>

Das Handle des [*Hauptschlüssel*](/windows/desktop/SecGloss/m-gly) Objekts.

</dd> <dt>

*hhandshakehash* \[ in\]
</dt> <dd>

Das Handle des Hashs der Handshake-Meldungen.

</dd> <dt>

*pboutput* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Hash für die Abschluss Meldung empfängt.

</dd> <dt>

*cboutput* \[ in\]
</dt> <dd>

Die Länge des *pboutput* -Puffers in Bytes.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Eine der folgenden Konstanten.



| Wert                                                                                                                                                                                                                                                      | Bedeutung                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <dt>**NCrypt \_ SSL \_ - \_ clientflag**</dt> <dt>0x00000001</dt> </dl> | Gibt an, dass es sich um einen Client Befehl handelt.<br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <dt>**NCrypt \_ SSL \_ - \_ Serverflag**</dt> <dt>0x00000002</dt> </dl> | Gibt an, dass es sich um einen Server-Rückruf handelt<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.



| Rückgabecode/-wert                                                                                                                                                                | BESCHREIBUNG                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>2148073510 (0x80090026)</dt> </dl> | Eines der angegebenen Handles ist ungültig.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die **sslcomputefinishedhash** -Funktion ist eine von drei Funktionen, die verwendet werden, um einen Hash zu generieren, der während des SSL-Handshake verwendet wird.

1.  Die [**sslkreatehandshakehash**](sslcreatehandshakehash.md) -Funktion wird aufgerufen, um ein Hashhandle abzurufen.
2.  Die [**sslhashhandshake**](sslhashhandshake.md) -Funktion wird beliebig oft mit dem Hashhandle aufgerufen, um dem Hash Daten hinzuzufügen.
3.  Die **sslcomputefinishedhash** -Funktion wird mit dem Hashhandle aufgerufen, um den Digest der Hash Daten zu erhalten.

Der Hashwert wird berechnet, indem ein Hashwert für den geheimen Hauptschlüssel mit einem Hash aller vorherigen gesendeten oder empfangenen Hand Shake Nachrichten vorliegt.

Der Wert von *cboutput* bestimmt die Länge der Hashdaten. Wenn das Protokoll " [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1,0" verwendet wird, sollte dies immer "12 (Bytes)" lauten. Weitere Informationen finden Sie in [der TLS-Protokoll Version 1,0](https://www.ietf.org/rfc/rfc2246.txt).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

