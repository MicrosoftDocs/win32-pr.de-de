---
description: Importiert einen Schlüssel in den Secure Sockets Layer-Protokollanbieter (SSL).
ms.assetid: 42310799-384e-4396-a9d5-5f226ca25a86
title: SslImportKey-Funktion (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 00dbe668c28e234c0ed4fdc7950b6b9627ae5aaba46bbef4e17d1eb8cb213f85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906088"
---
# <a name="sslimportkey-function"></a>SslImportKey-Funktion

Die **SslImportKey-Funktion** importiert einen Schlüssel in den [*Secure Sockets Layer-Protokollanbieter*](/windows/desktop/SecGloss/s-gly) (SSL).

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslImportKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phKey,
  _In_  LPCWSTR            pszBlobType,
  _In_  PBYTE              pbKeyBlob,
  _In_  DWORD              cbKeyBlob,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle für die SSL-Protokollanbieterinstanz.

</dd> <dt>

*phKey* \[ out\]
</dt> <dd>

Ein Zeiger auf das Handle des kryptografischen [*Schlüssels,*](/windows/desktop/SecGloss/c-gly) um den importierten Schlüssel zu empfangen.

</dd> <dt>

*pszBlobType* \[ In\]
</dt> <dd>

Eine auf NULL terminierte Unicode-Zeichenfolge, die einen Bezeichner enthält, der den [*Blobtyp*](/windows/desktop/SecGloss/b-gly) angibt, der im *pbInput-Puffer enthalten* ist. Dies kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <dt>**ÖFFENTLICHES BCRYPT \_ \_ \_ DH-BLOB**</dt> </dl>    | Exportieren Sie Diffie-Hellman [*öffentlichen Schlüssel.*](/windows/desktop/SecGloss/p-gly) Der *pbOutput-Puffer* empfängt eine [**BCRYPT \_ DH KEY \_ \_ BLOB-Struktur**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) unmittelbar gefolgt von den Schlüsseldaten.<br/>                                                                                                                                                        |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <dt>**BCRYPT \_ \_ ECCPUBLIC-BLOB**</dt> </dl>     | Exportieren Sie einen öffentlichen ECC-Schlüssel [*(Elliptic Curve Cryptography).*](/windows/desktop/SecGloss/e-gly) [](/windows/desktop/SecGloss/p-gly) Der *pbOutput-Puffer* empfängt eine [**BCRYPT \_ ECLEKY-BLOB-Struktur \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) unmittelbar gefolgt von den Schlüsseldaten.<br/>                             |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <dt>**BLOB MIT \_ NICHT TRANSPARENTEM BCRYPT-SCHLÜSSEL \_ \_**</dt> </dl> | Exportieren Sie [*einen symmetrischen Schlüssel*](/windows/desktop/SecGloss/s-gly) in einem Format, das für einen einzelnen Kryptografiedienstanbieter (Cryptographic [*Service Provider,*](/windows/desktop/SecGloss/c-gly) CSP) spezifisch ist. Nicht transparente BLOBs sind nicht übertragbar und müssen mit demselben CSP importiert werden, der das BLOB generiert hat.<br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <dt>**BCRYPT \_ \_ RSAPUBLIC-BLOB**</dt> </dl>     | Exportieren sie einen [*öffentlichen RSA-Schlüssel.*](/windows/desktop/SecGloss/r-gly) Der *pbOutput-Puffer* empfängt eine [**BCRYPT \_ \_ RSAKEY-BLOB-Struktur**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) unmittelbar gefolgt von den Schlüsseldaten.<br/>                                                                                                                                                                                 |



 

</dd> <dt>

*pbKeyBlob* \[ In\]
</dt> <dd>

Ein Zeiger auf den Puffer, der den Schlüssel [*BLOB enthält.*](/windows/desktop/SecGloss/k-gly)

</dd> <dt>

*cbKeyBlob* \[ In\]
</dt> <dd>

Die Größe des *pbKeyBlob-Puffers* in Bytes.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, gibt sie einen Fehlerwert ungleich 0 (null) zurück.

Mögliche Rückgabecodes sind u. a. folgende:



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Es ist nicht genügend Arbeitsspeicher verfügbar, um erforderliche Puffer zu reservieren.<br/> |
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl>    | Das *hSslProvider-Handle* ist ungültig.<br/>                       |
| <dl> <dt>**NTE \_ UNGÜLTIGER \_ PARAMETER**</dt> <dt>0x80090027L</dt> </dl> | Der *phKey-Parameter* ist **NULL.**<br/>                            |



 

## <a name="remarks"></a>Hinweise

Sie können die **SslImportKey-Funktion** verwenden, um Sitzungsschlüssel als Teil des Prozesses zum Übertragen von Sitzungsschlüsseln von einem Prozess in einen anderen zu importieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

