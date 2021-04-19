---
description: Ruft ein Handle für den Handshake-Hash ab, der für die Client Authentifizierung verwendet wird.
ms.assetid: 55007ce0-4bf1-4605-9b34-2931935762aa
title: Sslkreateclientauthhash-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4ac83d6d8aeea8429812d80b7bf66de7c87062a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345894"
---
# <a name="sslcreateclientauthhash-function"></a>Sslkreateclientauthhash-Funktion

Die **sslkreateclientauthhash** -Funktion Ruft ein Handle für den Handshake- [*Hash*](/windows/desktop/SecGloss/h-gly) ab, der für die Client Authentifizierung verwendet wird.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslCreateClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  LPCWSTR            pszHashAlgId,
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

Ein Zeiger auf eine **NCrypt- \_ Hash \_ handle** -Variable, um das Hashhandle zu empfangen.

</dd> <dt>

*dwprotocol* \[ in\]
</dt> <dd>

Einer der [**CNG-SSL-Anbieter Protokoll-Bezeichnerwerte**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwciphersuite* \[ in\]
</dt> <dd>

Einer der [**Cipher Suite-Bezeichnerwerte des CNG-SSL-Anbieters**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*pszhashalgid* \[ in\]
</dt> <dd>

Einer der [**CNG-Algorithmus-Bezeichner**](cng-algorithm-identifiers.md) Werte.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert und muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. die folgenden:



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt> </dl>    | Der *hsslprovider* -Parameter enthält einen ungültigen Zeiger.<br/>                |
| <dl> <dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt> </dl> | Der Parameter " *phhandshakehash* " ist auf **null** festgelegt.<br/>                               |
| <dl> <dt>**Ernte \_ Nicht \_ unterstützt**</dt> <dt>0x80090029l</dt> </dl>     | Die ausgewählte Funktion wird in der angegebenen Version der Schnittstelle nicht unterstützt.<br/> |
| <dl> <dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt> </dl>         | Nicht genügend Arbeitsspeicher zum Zuordnen von Puffern.<br/>                                          |
| <dl> <dt>**Ernte \_ Ungültige \_ Flags**</dt> <dt>0x80090009l</dt> </dl>         | Der *dwFlags* -Parameter muss auf 0 (null) festgelegt werden.<br/>                                      |



 

## <a name="remarks"></a>Bemerkungen

Die **sslkreateclientauthhash** -Funktion wird für die Konversationen von [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1,2 oder höher aufgerufen, um Hash Objekte zu erstellen, die zum Hashen von Hand Shake Nachrichten verwendet werden. Sie wird einmal für jeden möglichen [*Hash Algorithmus*](/windows/desktop/SecGloss/h-gly) aufgerufen, der in der Client Authentifizierungs Signatur verwendet werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

