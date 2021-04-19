---
description: Ruft ein Hashhandle ab, das zum Hashen von Hand Shake Nachrichten verwendet wird.
ms.assetid: 31390584-9d23-41d1-8604-b84a5e52ecde
title: Sslkreatehandshakehash-Funktion (sslprovider. h)
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
ms.openlocfilehash: 8affda999278ce2d4a740293a7532643a6c564ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356663"
---
# <a name="sslcreatehandshakehash-function"></a>Sslkreatehandshakehash-Funktion

Die **sslkreatehandshakehash** -Funktion Ruft ein Hashhandle ab, das zum Hashen von Hand Shake Nachrichten verwendet wird.

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

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle der Protokoll Anbieter Instanz des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*phhandshakehash* \[ vorgenommen\]
</dt> <dd>

Ein Hash handle, das an andere SSL-Anbieter Funktionen übermittelt werden kann.

</dd> <dt>

*dwprotocol* \[ in\]
</dt> <dd>

Einer der [**CNG-SSL-Anbieter Protokoll-Bezeichnerwerte**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

> [!Note]  
> Diese Funktion wird nicht mit dem SSL 2,0-Protokoll verwendet.

 

</dd> <dt>

*dwciphersuite* \[ in\]
</dt> <dd>

Einer der [**Cipher Suite-Bezeichnerwerte des CNG-SSL-Anbieters**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. die folgenden:



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt> </dl>         | Zum Zuordnen des Hash Puffers ist nicht genügend Arbeitsspeicher verfügbar.<br/> |
| <dl> <dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt> </dl>    | Das *hsslprovider* -Handle ist ungültig.<br/>                   |
| <dl> <dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt> </dl> | Der *phhandshakehash* ist NULL.<br/>                            |



 

## <a name="remarks"></a>Bemerkungen

Die **sslkreatehandshakehash** -Funktion ist eine von drei Funktionen, die verwendet werden, um einen Hash zu generieren, der während des SSL-Handshakes verwendet wird.

1.  Die **sslkreatehandshakehash** -Funktion wird aufgerufen, um ein Hashhandle abzurufen.
2.  Die [**sslhashhandshake**](sslhashhandshake.md) -Funktion wird beliebig oft mit dem Hashhandle aufgerufen, um dem Hash Daten hinzuzufügen.
3.  Die [**sslcomputefinishedhash**](sslcomputefinishedhash.md) -Funktion wird mit dem Hashhandle aufgerufen, um den Digest der Hash Daten zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

