---
description: 'Gibt den CNG-Algorithmusbezeichner (Cryptography API: Next Generation) des Hash Algorithmus zurück, der für das Eingabe Protokoll, die Verschlüsselungs Sammlung und den Schlüsseltyp für die Pseudo Zufallsfunktion (Transport Layer Security Protocol) verwendet wird.'
ms.assetid: 8d20b2da-390e-458e-b122-f5ef3722ad87
title: Sslgetciphersuiteprf HashAlgorithm-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetCipherSuitePRFHashAlgorithm
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 452cb7b36b20697a95b2c2abae7d8cd3b4180050
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354869"
---
# <a name="sslgetciphersuiteprfhashalgorithm-function"></a>Sslgetciphersuiteprf HashAlgorithm-Funktion

Die **sslgetciphersuiteprf HashAlgorithm** -Funktion gibt den CNG-Algorithmus (Cryptography API: Next Generation) des [*Hash Algorithmus*](/windows/desktop/SecGloss/h-gly) zurück, der für das Eingabe Protokoll, die Verschlüsselungs Sammlung und den Schlüsseltyp für die " [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) (TLS) [*Pseudo Random Function*](/windows/desktop/SecGloss/p-gly) (PRF)" verwendet wird.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslGetCipherSuitePRFHashAlgorithm(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _Out_ WCHAR              szPRFHash[NCRYPT_SSL_MAX_NAME_SIZE],
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle der Protokoll Anbieter Instanz des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).

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

Einer der [**Schlüsseltyp-Bezeichnerwerte des CNG-SSL-Anbieters**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) . Legen Sie für Schlüsseltypen, bei denen es sich nicht um eine [*Kryptographie*](/windows/desktop/SecGloss/e-gly) (ECC) handelt, diesen Parameter auf 0 (null) fest.

</dd> <dt>

*szprf Hash* \[ vorgenommen\]
</dt> <dd>

Einer der [**CNG-Algorithmusbezeichner**](cng-algorithm-identifiers.md) für den Hash, der für die TLS-PRF verwendet wird.

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
| <dl> <dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt> </dl> | Der *szprfhash* -Parameter ist auf **null** festgelegt.<br/>                                     |
| <dl> <dt>**Ernte \_ Nicht \_ unterstützt**</dt> <dt>0x80090029l</dt> </dl>     | Die ausgewählte Funktion wird in der angegebenen Version der Schnittstelle nicht unterstützt.<br/> |
| <dl> <dt>**Ernte \_ Ungültige \_ Flags**</dt> <dt>0x80090009l</dt> </dl>         | Der *dwFlags* -Parameter muss auf 0 (null) festgelegt werden.<br/>                                      |



 

## <a name="remarks"></a>Bemerkungen

Diese **sslgetciphersuiteprfhashalgorithm** -Funktion wird für die Konversationen von TLS 1,2 oder höher aufgerufen, um den Hash Algorithmus abzufragen, der in der TLS-PRF verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

