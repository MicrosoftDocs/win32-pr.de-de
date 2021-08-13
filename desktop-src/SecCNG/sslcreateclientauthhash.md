---
description: Ruft ein Handle für den Handshakehash ab, der für die Clientauthentifizierung verwendet wird.
ms.assetid: 55007ce0-4bf1-4605-9b34-2931935762aa
title: SslCreateClientAuthHash-Funktion (Sslprovider.h)
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
ms.openlocfilehash: 96f1e7fa0de86439f89bf5c4c610bf5b46640533071260852c47321c5a1c6673
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907087"
---
# <a name="sslcreateclientauthhash-function"></a>SslCreateClientAuthHash-Funktion

Die **SslCreateClientAuthHash-Funktion** ruft ein Handle für den Handshakehash ab, der für die Clientauthentifizierung verwendet wird. [](/windows/desktop/SecGloss/h-gly)

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

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle der SSL-Protokollanbieterinstanz [*(Secure Sockets Layer Protocol).*](/windows/desktop/SecGloss/s-gly)

</dd> <dt>

*phHandshakeHash* \[ out\]
</dt> <dd>

Ein Zeiger auf eine **NCRYPT \_ HASH \_ HANDLE-Variable,** um das Hashhandle zu empfangen.

</dd> <dt>

*dwProtocol* \[ In\]
</dt> <dd>

Einer der [**CNG SSL Provider Protocol Identifier-Werte.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

</dd> <dt>

*dwCipherSuite* \[ In\]
</dt> <dd>

Einer der [**CNG SSL Provider Cipher Suite Identifier-Werte.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*pszHashAlgId* \[ In\]
</dt> <dd>

Einer der [**CNG-Algorithmusbezeichnerwerte.**](cng-algorithm-identifiers.md)

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert und muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. folgende.



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl>    | Der *hSslProvider-Parameter* enthält einen ungültigen Zeiger.<br/>                |
| <dl> <dt>**NTE \_ INVALID \_ PARAMETER**</dt> <dt>0x80090027L</dt> </dl> | Der *phHandshakeHash-Parameter* ist auf **NULL** festgelegt.<br/>                               |
| <dl> <dt>**NTE \_ NICHT \_ UNTERSTÜTZT**</dt> <dt>0x80090029L</dt> </dl>     | Die ausgewählte Funktion wird in der angegebenen Version der Schnittstelle nicht unterstützt.<br/> |
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Nicht genügend Arbeitsspeicher zum Zuordnen von Puffern.<br/>                                          |
| <dl> <dt>**NTE \_ BAD \_ FLAGS**</dt> <dt>0x80090009L</dt> </dl>         | Der *dwFlags-Parameter* muss auf 0 (null) festgelegt werden.<br/>                                      |



 

## <a name="remarks"></a>Hinweise

Die **SslCreateClientAuthHash-Funktion** wird für [*Transport Layer Security-Protokoll*](/windows/desktop/SecGloss/t-gly) (TLS) 1.2 oder höher aufgerufen, um Hashobjekte zu erstellen, die zum Hashen von Handshakenachrichten verwendet werden. Sie wird einmal für jeden möglichen [*Hashalgorithmus*](/windows/desktop/SecGloss/h-gly) aufgerufen, der in der Clientauthentifizierungssignatur verwendet werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

