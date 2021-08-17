---
description: Ruft ein Hashhandle ab, das zum Hashen von Handshakenachrichten verwendet wird.
ms.assetid: 31390584-9d23-41d1-8604-b84a5e52ecde
title: SslCreateHandshakeHash-Funktion (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateHandshakeHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ea481a5b577c41eafddf9db8d80b4a3a1fe42d801bf96ed8cbc57127a4a8d91e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906827"
---
# <a name="sslcreatehandshakehash-function"></a>SslCreateHandshakeHash-Funktion

Die **SslCreateHandshakeHash-Funktion** ruft ein Hashhandle ab, das zum Hashen von Handshakenachrichten verwendet wird.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslCreateHandshakeHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle der SSL-Protokollanbieterinstanz [*(Secure Sockets Layer Protocol).*](/windows/desktop/SecGloss/s-gly)

</dd> <dt>

*phHandshakeHash* \[ out\]
</dt> <dd>

Ein Hashhandle, das an andere SSL-Anbieterfunktionen übergeben werden kann.

</dd> <dt>

*dwProtocol* \[ In\]
</dt> <dd>

Einer der [**CNG SSL Provider Protocol Identifier-Werte.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

> [!Note]  
> Diese Funktion wird nicht mit dem SSL 2.0-Protokoll verwendet.

 

</dd> <dt>

*dwCipherSuite* \[ In\]
</dt> <dd>

Einer der [**CNG SSL Provider Cipher Suite Identifier-Werte.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. folgende.



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Es ist nicht genügend Arbeitsspeicher zum Zuordnen des Hashpuffers vorhanden.<br/> |
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl>    | Das *hSslProvider-Handle* ist ungültig.<br/>                   |
| <dl> <dt>**NTE \_ INVALID \_ PARAMETER**</dt> <dt>0x80090027L</dt> </dl> | *PhHandshakeHash* ist NULL.<br/>                            |



 

## <a name="remarks"></a>Hinweise

Die **SslCreateHandshakeHash-Funktion** ist eine von drei Funktionen, die verwendet werden, um einen Hash zu generieren, der während des SSL-Handshakes verwendet wird.

1.  Die **SslCreateHandshakeHash-Funktion** wird aufgerufen, um ein Hashhandle abzurufen.
2.  Die [**SslHashHandshake-Funktion**](sslhashhandshake.md) wird beliebig oft mit dem Hashhandle aufgerufen, um dem Hash Daten hinzuzufügen.
3.  Die [**SslComputeFinishedHash-Funktion**](sslcomputefinishedhash.md) wird mit dem Hashhandle aufgerufen, um den Digest der Hashdaten abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

