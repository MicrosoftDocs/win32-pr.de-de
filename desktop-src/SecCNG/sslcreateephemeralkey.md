---
description: Erstellt einen kurzlebigen Schlüssel zur Verwendung während der Authentifizierung, die während des SSL-Handshakes (Secure Sockets Layer Protocol) auftritt.
ms.assetid: faad9b3b-e476-4e61-b978-bcb517ecaeb7
title: SslCreateEphemeralKey-Funktion (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateEphemeralKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: a6a54de2865df805af51b054c22d455d52914a5b00514767d432ceda28c16a39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907097"
---
# <a name="sslcreateephemeralkey-function"></a>SslCreateEphemeralKey-Funktion

Die **SslCreateEphmeralKey-Funktion** erstellt einen kurzlebigen Schlüssel zur Verwendung während der Authentifizierung, die während des SSL-Handshakes (Secure Sockets Layer [*Protocol)*](/windows/desktop/SecGloss/s-gly) auftritt.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslCreateEphemeralKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phEphemeralKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _In_  DWORD              dwKeyBitLen,
  _In_  PBYTE              pbParams,
  _In_  DWORD              cbParams,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle der SSL-Protokollanbieterinstanz.

</dd> <dt>

*phEphemeralKey* \[ out\]
</dt> <dd>

Das Handle des kurzlebigen Schlüssels.

</dd> <dt>

*dwProtocol* \[ In\]
</dt> <dd>

Einer der [**CNG SSL Provider Protocol Identifier-Werte.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

</dd> <dt>

*dwCipherSuite* \[ In\]
</dt> <dd>

Einer der [**CNG SSL Provider Cipher Suite Identifier-Werte.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*dwKeyType* \[ In\]
</dt> <dd>

Einer der [**CNG SSL Provider Key Type Identifier-Werte.**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) Legen Sie diesen Parameter für Schlüsseltypen, die keine ECC [*(Elliptic Curve Cryptography)*](/windows/desktop/SecGloss/e-gly) sind, auf 0 fest.

</dd> <dt>

*dwKeyBitLen* \[ In\]
</dt> <dd>

Die Länge des Schlüssels in Bits.

</dd> <dt>

*pbParams* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der Parameter für den schlüssel enthält, der erstellt werden soll. Wenn keine Cipher Suite für den [*Diffie-Hellman-Schlüsselaustauschalgorithmus*](/windows/desktop/SecGloss/d-gly) (DHE) verwendet wird, legen Sie den *pbParams-Parameter* auf **NULL** und den *cbParams-Parameter* auf 0 (null) fest.

</dd> <dt>

*cbParams* \[ In\]
</dt> <dd>

Die Länge der Daten im *pbParams-Puffer* in Bytes.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, gibt sie einen Fehlerwert ungleich 0 (null) zurück.



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Es ist nicht genügend Arbeitsspeicher zum Zuordnen des Puffers verfügbar.<br/> |
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl>    | Das *hSslProvider-Handle* ist ungültig.<br/>              |
| <dl> <dt>**NTE \_ UNGÜLTIGER \_ PARAMETER**</dt> <dt>0x80090027L</dt> </dl> | Einer der angegebenen Parameter ist ungültig.<br/>         |



 

## <a name="remarks"></a>Hinweise

Bei Verwendung einer DHE-Verschlüsselungssammlung übergibt die interne SSL-Implementierung die Parameter *p* und *g* des Servers an die **SslCreateEphmeralKey-Funktion** in den *Parametern pbParams* und *cbParams.*

Das Format der Daten im *pbParams-Puffer* ist das gleiche wie beim Festlegen der [**BCRYPT \_ DH \_ PARAMETERS-Eigenschaft**](cng-property-identifiers.md) und beginnt mit einer [**BCRYPT \_ DH PARAMETER \_ \_ HEADER-Struktur.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

