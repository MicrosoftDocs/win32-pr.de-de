---
description: 'Gibt den CNG-Algorithmusbezeichner (Cryptography API: Next Generation) des Hashalgorithmus zurück, der für die PSEUDO-Random-Funktion (PRF) des Transport Layer Security-Protokolls (TLS) für das Eingabeprotokoll, die Verschlüsselungssammlung und den Schlüsseltyp verwendet wird.'
ms.assetid: 8d20b2da-390e-458e-b122-f5ef3722ad87
title: SslGetCipherSuitePRFHashAlgorithm-Funktion (Sslprovider.h)
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
ms.openlocfilehash: f328f5e4746d3a66f614e8ccbbfe66bbf3475b7f7a1a98a8a68c11df96412bf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906162"
---
# <a name="sslgetciphersuiteprfhashalgorithm-function"></a>SslGetCipherSuitePRFHashAlgorithm-Funktion

Die **SslGetCipherSuitePRFHashAlgorithm-Funktion** gibt den CNG-Algorithmusbezeichner (Cryptography API: Next Generation) des Hashalgorithmus [](/windows/desktop/SecGloss/p-gly) zurück, der für die Transport Layer Security TLS-Pseudozufallsfunktion [*(TLS)*](/windows/desktop/SecGloss/t-gly) des Eingabeprotokolls, der Verschlüsselungssammlung und des Schlüsseltyps verwendet wird. [](/windows/desktop/SecGloss/h-gly)

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

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle der [*SSL-Secure Sockets Layer*](/windows/desktop/SecGloss/s-gly) (Protokollanbieterinstanz).

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

Einer der [**CNG SSL Provider Key Type Identifier-Werte.**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) Legen Sie für Schlüsseltypen, die keine [*ECC (Elliptic Curve Cryptography)*](/windows/desktop/SecGloss/e-gly) sind, diesen Parameter auf 0 (null) fest.

</dd> <dt>

*szPRFHash* \[ out\]
</dt> <dd>

Einer der [**CNG-Algorithmusbezeichner für**](cng-algorithm-identifiers.md) den Hash, der für die TLS-PRF verwendet wird.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert und muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, gibt sie einen Fehlerwert ungleich 0 (null) zurück.

Mögliche Rückgabecodes sind u. a. folgende:



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl>    | Der *hSslProvider-Parameter* enthält einen ungültigen Zeiger.<br/>                |
| <dl> <dt>**NTE \_ UNGÜLTIGER \_ PARAMETER**</dt> <dt>0x80090027L</dt> </dl> | Der *szPRFHash-Parameter* ist auf **NULL festgelegt.**<br/>                                     |
| <dl> <dt>**NTE \_ NICHT \_ UNTERSTÜTZT**</dt> <dt>0x80090029L</dt> </dl>     | Die ausgewählte Funktion wird in der angegebenen Version der -Schnittstelle nicht unterstützt.<br/> |
| <dl> <dt>**NTE \_ BAD \_ FLAGS**</dt> <dt>0x80090009L</dt> </dl>         | Der *dwFlags-Parameter* muss auf 0 (null) festgelegt werden.<br/>                                      |



 

## <a name="remarks"></a>Hinweise

Diese **SslGetCipherSuitePRFHashAlgorithm-Funktion** wird für TLS 1.2- oder höher-Konversationen aufgerufen, um den Hashalgorithmus abfragen zu können, der in der TLS-PRF verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

