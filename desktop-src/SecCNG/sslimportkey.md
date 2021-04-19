---
description: Importiert einen Schlüssel in den SSL-Protokoll Anbieter (Secure Sockets Layer Protocol).
ms.assetid: 42310799-384e-4396-a9d5-5f226ca25a86
title: Sslimportkey-Funktion (sslprovider. h)
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
ms.openlocfilehash: 8bf1b03fd5d51974db3676dcdbccc2a2b0fa4323
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349154"
---
# <a name="sslimportkey-function"></a>Sslimportkey-Funktion

Die **sslimportkey** -Funktion importiert einen Schlüssel in den SSL-Protokoll Anbieter ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).

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

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle für die SSL-Protokoll Anbieter Instanz.

</dd> <dt>

*phkey* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf das Handle des [*Kryptografieschlüssels*](/windows/desktop/SecGloss/c-gly) , der den importierten Schlüssel empfängt.

</dd> <dt>

*pszblobtype* \[ in\]
</dt> <dd>

Eine NULL-terminierte Unicode-Zeichenfolge, die einen Bezeichner enthält, der den Typ des [*BLOBs*](/windows/desktop/SecGloss/b-gly) angibt, der im *pbinput* -Puffer enthalten ist. Dies kann einer der folgenden Werte sein:



| Wert                                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <dt>**bcrypt \_ dh \_ Public \_ BLOB**</dt> </dl>    | Exportieren Sie einen Diffie-Hellman [*öffentlichen Schlüssel*](/windows/desktop/SecGloss/p-gly). Der *pboutput* -Puffer empfängt eine [**bcrypt \_ DH-Schlüssel- \_ \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) -Struktur, auf die die Schlüsseldaten unmittelbar folgen.<br/>                                                                                                                                                        |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <dt>**bcrypt \_ eccpublic- \_ BLOB**</dt> </dl>     | Exportieren eines [*öffentlichen Schlüssels*](/windows/desktop/SecGloss/p-gly)der [*elliptischen Kurve Kryptografie*](/windows/desktop/SecGloss/e-gly) (ECC). Der *pboutput* -Puffer empfängt eine [**bcrypt \_ ecckey- \_ blobstruktur**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) , die direkt auf die Schlüsseldaten folgt.<br/>                             |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <dt>**bcrypt \_ - \_ Schlüssel- \_ BLOB nicht transparent**</dt> </dl> | Exportieren Sie einen [*symmetrischen Schlüssel*](/windows/desktop/SecGloss/s-gly) in einem Format, das für einen einzelnen [*Kryptografiedienstanbieter*](/windows/desktop/SecGloss/c-gly) (CSP) spezifisch ist. Nicht transparente BLOBs sind nicht übertragbar und müssen mit demselben CSP importiert werden, der das BLOB generiert hat.<br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <dt>**bcrypt \_ rsapublic- \_ BLOB**</dt> </dl>     | Exportieren Sie einen öffentlichen [*RSA*](/windows/desktop/SecGloss/r-gly) -Schlüssel. Der *pboutput* -Puffer empfängt eine [**bcrypt \_ rsaKey- \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) -Struktur, auf die die Schlüsseldaten unmittelbar folgen.<br/>                                                                                                                                                                                 |



 

</dd> <dt>

*pbKeyBlob* \[ in\]
</dt> <dd>

Ein Zeiger auf den Puffer, der das [*Schlüsselblob*](/windows/desktop/SecGloss/k-gly)enthält.

</dd> <dt>

*cbKeyBlob* \[ in\]
</dt> <dd>

Die Größe des *pbKeyBlob* -Puffers in Bytes.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. die folgenden:



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt> </dl>         | Es ist nicht genügend Arbeitsspeicher verfügbar, um erforderliche Puffer zuzuordnen.<br/> |
| <dl> <dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt> </dl>    | Das *hsslprovider* -Handle ist ungültig.<br/>                       |
| <dl> <dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt> </dl> | Der *phkey* -Parameter ist **null**.<br/>                            |



 

## <a name="remarks"></a>Bemerkungen

Sie können die **sslimportkey** -Funktion verwenden, um Sitzungsschlüssel im Rahmen der Übertragung von Sitzungs Schlüsseln von einem Prozess in einen anderen zu importieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

