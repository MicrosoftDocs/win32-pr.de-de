---
description: Erstellt einen kurzlebigen Schlüssel zur Verwendung während der Authentifizierung, die während des SSL-Handshakes (Secure Sockets Layer Protocol) auftritt.
ms.assetid: faad9b3b-e476-4e61-b978-bcb517ecaeb7
title: Sslkreatekurzlealkey-Funktion (sslprovider. h)
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
ms.openlocfilehash: 452b0166da367bb6b1530f5669e55b7ca909e13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347113"
---
# <a name="sslcreateephemeralkey-function"></a>Sslkreatekurzlealkey-Funktion

Die **sslkreatekurzlealkey** -Funktion erstellt einen kurzlebigen Schlüssel zur Verwendung während der Authentifizierung, die während des [*Secure Sockets Layer Protokoll*](/windows/desktop/SecGloss/s-gly) -Handshake (SSL) auftritt.

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

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle der SSL-Protokoll Anbieter Instanz.

</dd> <dt>

*phphemeralkey* \[ vorgenommen\]
</dt> <dd>

Das Handle des kurzlebigen Schlüssels.

</dd> <dt>

*dwprotocol* \[ in\]
</dt> <dd>

Einer der [**CNG-SSL-Anbieter Protokoll-Bezeichnerwerte**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwciphersuite* \[ in\]
</dt> <dd>

Einer der [**Cipher Suite-Bezeichnerwerte des CNG-SSL-Anbieters**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*dwkeytype* \[ in\]
</dt> <dd>

Einer der [**Schlüsseltyp-Bezeichnerwerte des CNG-SSL-Anbieters**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) . Legen Sie diesen Parameter für Schlüsseltypen, die keine [*Kryptografie (Elliptic Curve Kryptografie*](/windows/desktop/SecGloss/e-gly) , ECC) sind, auf NULL fest.

</dd> <dt>

*dwkeybitlen* \[ in\]
</dt> <dd>

Die Länge des Schlüssels in Bits.

</dd> <dt>

*pbparameams* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der Parameter für den Schlüssel enthalten soll, der erstellt werden soll. Wenn ein [*Diffie-Hellman (kurzlebiger) Key-Exchange-Algorithmus*](/windows/desktop/SecGloss/d-gly) (DHE) Verschlüsselungs Suite nicht verwendet wird, legen Sie den *pbparser* -Parameter auf **null** und den *cbparameams* -Parameter auf 0 (null) fest.

</dd> <dt>

*cbparametriams* \[ in\]
</dt> <dd>

Die Länge der Daten im *pbparameams* -Puffer in Bytes.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt> </dl>         | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Puffer zuzuordnen.<br/> |
| <dl> <dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt> </dl>    | Das *hsslprovider* -Handle ist ungültig.<br/>              |
| <dl> <dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt> </dl> | Einer der angegebenen Parameter ist ungültig.<br/>         |



 

## <a name="remarks"></a>Bemerkungen

Wenn eine dit-Verschlüsselungs Sammlung verwendet wird, übergibt die interne SSL-Implementierung Server- *p* -und *g* -Parameter an die **sslkreatekurzlealkey** -Funktion in den Parametern *pbpara AMS* und *cbparameame.*

Das Format der Daten im *pbparameams* -Puffer ist mit dem Format identisch, das beim Festlegen der [**bcrypt \_ dh- \_ Parameter**](cng-property-identifiers.md) Eigenschaft verwendet wird, und beginnt mit einer [**bcrypt \_ dh- \_ Parameter \_ Header**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) Struktur.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

