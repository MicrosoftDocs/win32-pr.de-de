---
description: Gibt eine NCRYPT \_ SSL \_ CIPHER \_ LENGTHS-Struktur zurück, die die Header- und Nachspannlängen des Eingabeprotokolls, der Verschlüsselungssammlung und des Schlüsseltyps enthält.
ms.assetid: 44d0d803-16d7-4bdf-9638-afbdaf9e1802
title: SslLookupCipherLengths-Funktion (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherLengths
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 3898b54946b9a1035ce8ec1fedabc218c750bff6579b39f195a1f60b378144f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905990"
---
# <a name="ssllookupcipherlengths-function"></a>SslLookupCipherLengths-Funktion

Die **SslLookupCipherLengths-Funktion** gibt eine [**NCRYPT \_ SSL \_ CIPHER \_ LENGTHS-Struktur**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) zurück, die die Header- und Nachspannlängen des Eingabeprotokolls, der Verschlüsselungssammlung und des Schlüsseltyps enthält.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslLookupCipherLengths(
  _In_  NCRYPT_PROV_HANDLE        hSslProvider,
  _In_  DWORD                     dwProtocol,
  _In_  DWORD                     dwCipherSuite,
  _In_  DWORD                     dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_LENGTHS *pCipherLengths,
  _In_  DWORD                     cbCipherLengths,
  _In_  DWORD                     dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle der SSL-Protokollanbieterinstanz [*(Secure Sockets Layer Protocol).*](/windows/desktop/SecGloss/s-gly)

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

Einer der [**CNG SSL Provider Key Type Identifier-Werte.**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) Legen Sie für Schlüsseltypen, bei denen es sich nicht um [*ECC (Elliptic Curve Cryptography)*](/windows/desktop/SecGloss/e-gly) handelt, diesen Parameter auf 0 (null) fest.

</dd> <dt>

*pCipherLengths* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer zum Empfangen der [**NCRYPT \_ SSL \_ CIPHER \_ LENGTHS-Struktur.**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**)

</dd> <dt>

*cbCipherLengths* \[ In\]
</dt> <dd>

Die Länge des Puffers in Bytes, auf den der *pCipherLengths-Parameter* zeigt.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert und muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. folgende.



| Rückgabecode/-wert                                                                                                                                                       | Beschreibung                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl>    | Der *hSslProvider-Parameter* enthält einen ungültigen Zeiger.<br/>                                                      |
| <dl> <dt>**NTE \_ INVALID \_ PARAMETER**</dt> <dt>0x80090027L</dt> </dl> | Der *pCipherLengths-Parameter* ist auf **NULL** festgelegt, oder die von *cbCipherLengths* angegebene Pufferlänge ist zu kurz.<br/> |
| <dl> <dt>**NTE \_ BAD \_ FLAGS**</dt> <dt>0x80090009L</dt> </dl>         | Der *dwFlags-Parameter* muss auf 0 (null) festgelegt werden.<br/>                                                                            |



 

## <a name="remarks"></a>Hinweise

Die **SslLookupCipherLengths-Funktion** wird für [*Transport Layer Security-Protokoll*](/windows/desktop/SecGloss/t-gly) (TLS) 1.1 oder höher aufgerufen, um die Header- und Nachspannlängen für das angeforderte Protokoll, die Verschlüsselungssammlung und den Schlüsseltyp abzufragen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

